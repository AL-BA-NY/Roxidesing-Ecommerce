# 📊 Matriz de Objetos vs. Procesos

## Descripción

Esta matriz describe las **relaciones entre los procesos de negocio y los objetos de negocio** que intervienen en cada uno.  
Cada ✓ indica que un objeto participa o es afectado por el proceso correspondiente.

---

## 🔍 Explicación de los elementos

### ✔️ Procesos de negocio

- **Registro de usuarios:** Permite crear un nuevo usuario en el sistema.
- **Visualizar catálogo:** Muestra los productos disponibles para la compra.
- **Agregar al carrito:** Permite seleccionar productos y agregarlos a un carrito temporal.
- **Confirmar pedido:** Convierte los artículos del carrito en un pedido confirmado.
- **Validación (admin):** Proceso exclusivo del administrador para validar pedidos u operaciones.
- **Generar recibo:** Crea un recibo después de confirmar el pedido.
- **Modificar inventario:** Permite al administrador ajustar las existencias de productos.

### ✔️ Objetos de negocio

- **Usuario:** Representa a las personas registradas en la aplicación.
- **Producto:** Los artículos que se ofrecen en el catálogo.
- **Carrito:** Estructura temporal que guarda los productos seleccionados antes de confirmar la compra.
- **Pedido:** Documento que contiene el resumen de la compra.
- **Recibo:** Documento generado después del pedido, que sirve como comprobante.

---

## 🎯 Importancia de la matriz

Esta matriz permite visualizar **cómo cada proceso del negocio impacta sobre los objetos del dominio**, facilitando el análisis del flujo de datos en la aplicación y la asignación de responsabilidades a los procesos del sistema.
