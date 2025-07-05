## Modelo de Objetos de Negocio – Diagrama de Clases UML

Este modelo representa los objetos principales del sistema de ventas en línea de RoxyDesign, así como sus relaciones internas. Es la base lógica que guía la estructura de datos del proyecto.

---

### Clases del sistema

#### 1. Usuario
Representa al cliente que utiliza la plataforma para realizar compras.  
**Atributos:**
- nombre
- correo
- contraseña

**Relaciones:**
- Un usuario tiene un carrito asociado.
- Un usuario puede generar múltiples pedidos.

---

#### 2. Carrito
Contenedor temporal de productos seleccionados por el usuario antes de confirmar una compra.  
**Atributos:**
- id
- items[] (lista de productos)

**Relaciones:**
- Está vinculado a un usuario.
- Se conecta con productos agregados al carrito.

---

#### 3. Producto
Elemento que se ofrece en la tienda para ser comprado.  
**Atributos:**
- id
- nombre
- precio
- stock

**Relaciones:**
- Los productos pueden ser añadidos al carrito.
- También son parte de los pedidos confirmados.

---

#### 4. Pedido
Representa una compra realizada por el usuario.  
**Atributos:**
- id
- estado (pendiente, aprobado, rechazado)
- fecha

**Relaciones:**
- Está vinculado a un usuario.
- Contiene productos seleccionados desde el carrito.
- Al ser aprobado, genera un recibo.

---

#### 5. Recibo
Documento generado automáticamente cuando un pedido es aprobado.  
**Atributos:**
- id
- total
- fecha

**Relaciones:**
- Cada recibo está asociado a un pedido confirmado.

---

### Flujo de relaciones

1. El usuario crea una cuenta e inicia sesión.
2. Navega por el catálogo y agrega productos al carrito.
3. Confirma el pedido y este queda registrado con estado "pendiente".
4. El administrador revisa el pedido y puede aprobarlo o rechazarlo.
5. Si el pedido es aprobado, se genera un recibo automáticamente.

---

### Importancia del modelo

Este modelo de clases permite organizar la estructura del sistema de forma clara, facilitando la implementación del backend, la lógica de negocio y la conexión con la base de datos. Cada clase representa una entidad del mundo real y sus relaciones reflejan el comportamiento esperado dentro de la tienda en línea.
