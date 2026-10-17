![alt text](../Img/image.png)

# Fundamentos de bases de datos
## 2.1: Bases de datos relacionales
### Prácticas

**Ejercicio 1: Analizar las funciones de una base de datos relacional**

**Visión general**
En esta práctica, analizará las funciones de las bases de datos de varias tablas a partir de un conjunto de ejemplos.

### Tareas
1. Identifique las posibles tablas y campos asociados del escenario proporcionado. Book.com es una tienda virtual en línea en Internet donde los clientes pueden examinar el catálogo y seleccionar los productos que deseen.

    - Cada libro tiene un título, ISBN, año y precio. La tienda también conserva la información del autor y del editor de cualquier libro.
    - Para los autores, la base de datos conserva el nombre, la dirección y la URL de su página inicial.
    - Para los editores, la base de datos conserva el nombre, la dirección, el número de teléfono y la URL de su sitio web.
    - La tienda tiene varios almacenes, cada uno de los cuales tiene un código, una dirección y un número de teléfono.
    - El almacén tiene en stock muchos libros. Un libro puede estar en stock en varios almacenes.
    - La base de datos registra el número de copias de un libro almacenadas en stock en varios almacenes.
    - La librería conserva el nombre, la dirección, el ID de correo electrónico y el número de teléfono de sus clientes.
    - Un cliente es propietario de varios carritos de la compra. El carrito de la compra se identifica mediante un Shopping_Cart_ID y contiene varios libros.
    - Algunos carritos de la compra pueden contener más de una copia del mismo libro. La base de datos registra el número de
    copias de cada libro que hay en cualquier carrito de la compra.
    - En ese momento, se necesitará más información para completar la transacción. Normalmente, se le pedirá al cliente que rellene o seleccione una dirección de facturación, una dirección de envío, una opción de envío e información de pago como el número de tarjeta de crédito. Se enviará una notificación por correo electrónico al cliente en cuanto se realice el pedido.

2. ABC Ltd planea automatizar su sistema de pedidos de venta y de control de stock. Un estudio de viabilidad recomienda encarecidamente que se instale un sistema de base de datos relacional. Los detalles de ventas y de control de stock de ABC son los siguientes:
    - Los clientes envían pedidos de productos. Cada pedido puede contener solicitudes de cantidades variables de uno o más productos de la gama de ABC. ABC mantiene un archivo de stock que muestra los detalles de cada uno de los productos y el proveedor preferido, la cantidad en stock, el nivel de nuevos pedidos y otros detalles.
    - ABC entrega los productos que tiene en el stock en respuesta al pedido del cliente y se genera una factura por los artículos enviados. Los artículos que no están en stock se incluyen en una lista de pedidos pendientes y estos artículos normalmente se vuelven a pedir al proveedor preferido. En ocasiones, los artículos se piden a orígenes alternativos.
    - En respuesta a las facturas que se envían a los clientes de ABC, estos envían los pagos. El pago puede corresponder a una factura, aparte de una factura, a varias facturas o a facturas parciales.
    - Identifique las tablas y campos asociados del escenario anterior.


![alt text](../Img/image.png)