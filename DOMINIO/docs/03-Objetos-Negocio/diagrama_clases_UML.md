## Modelo de Objetos de Negocio – Diagrama de Clases UML

Este modelo representa los objetos principales del sistema de ventas en línea de RoxyDesign, así como sus relaciones internas. Es la base lógica que guía la estructura de datos del proyecto.

---

### Clases del sistema

#### 1. Usuario
Representa al cliente que utiliza la plataforma para realizar compras.  

- **Atributos:** id, nombre, correo, contraseña.

**Métodos**:
-  iniciarSesion()
-  cerrarSesion()

---

#### 2. Afiliado
Un tipo de usuario que interactúa con tiendas y productos.

**Atributos:**
- dirección
- teléfono

**Métodos:**
- actualizarPerfil()
- verPedidos()
- editarCarrito()
- gestionarProductos()
- revisarPedidos()
- accederATienda()
- registrarPago()

**Relaciones:**

- "accede a" una Tienda.
- "recibe" un Pedido.
- "tiene" un Carrito.

---

#### 3 Administrador
Otro tipo de usuario con permisos de gestión.

**Métodos:** 
- iniciarSesion()
- revisarPedido()
- confirmarPedido()
-  modificarInventario()

**Relaciones:**
"revisa" un Pedido.

---

#### 4. Tienda


Representa un establecimiento o vendedor.

**Atributos:**
- id
- nombre
- descripcion
- precio
- stock
- imagen
  
**Métodos:**

- agregarProducto()
- verInventario()


**Relaciones:**

- "contiene" Productos.
- "ofrece" ItemCarrito.

---

#### 5. Carrito
Almacena los ítems que un usuario desea comprar.

**Atributos:**

- id
- total.

**Métodos:**
- calcularTotal()
- vaciar()
- agregarItem()
  
**Relaciones:**
- "contiene" ItemCarrito.

---

### Flujo de relaciones

1.El Afiliado inicia sesión y accede a una Tienda.

2.Selecciona Productos y los agrega al Carrito.

3.Realiza un Pedido desde el carrito.

4.El Pedido requiere un Pago, que el afiliado registra.

5.Tras el pago, se genera un Recibo.

6.El Administrador revisa y confirma el pedido.

---

### Importancia del modelo

Este modelo de clases permite organizar la estructura del sistema de forma clara, facilitando la implementación del backend, la lógica de negocio y la conexión con la base de datos. Cada clase representa una entidad del mundo real y sus relaciones reflejan el comportamiento esperado dentro de la tienda en línea.
