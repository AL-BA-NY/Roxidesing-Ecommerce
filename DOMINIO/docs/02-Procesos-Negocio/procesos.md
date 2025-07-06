## Explicación del Diagrama de Flujo del Modelo de Negocio

Este diagrama representa el flujo de proceso en el sistema propuesto para la empresa **Roxy Design**, que se dedica a la venta de bisutería a través de una plataforma en línea. A continuación, se describe el proceso paso a paso.

### Descripción de los elementos
---
#### Proceso del Afiliado (Usuario)

**Registro de usuario**: El proceso inicia con el registro del usuario.
Inicio de sesión: El usuario accede al sistema.

**Visualizar productos**: El usuario puede ver los productos disponibles.
Agregar productos al carrito: El usuario selecciona y añade productos a su carrito de compras.

**Confirmar pedido**: El usuario finaliza su selección y confirma el pedido.

---

####Proceso del Administrador

**Revisar pedido:** El administrador recibe y revisa el pedido realizado por el afiliado.
**Decisión: ¿Pedido aprobado?:** Se evalúa si el pedido es aprobado o no.

 --Si el pedido es aprobado (Sí):
	- Generar referencia de pago.
	- Registrar pago (del cliente).
	- Generar recibo electrónico.

- Si el pedido no es aprobado (No):
	- Rechazar pedido.
	- Editar carrito de compras (el usuario puede modificar su carrito).
	- Confirmar pedido (el usuario vuelve a confirmar el pedido después de la edición).
