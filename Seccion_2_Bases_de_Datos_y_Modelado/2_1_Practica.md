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

### Analisis
**Caso 1: Book.com**

#### Identificación de tablas y campos.

A partir del escenario, podemos proponer las siguientes tablas para la base de datos de Book.com.

**A. Libros, autores y editores**

1. LIBRO

Información de cada libro del catálogo.

| **Campo** | **Descripción** |
|-------|-------------|
|ISBN (PK) | Identificador único del libro |
| Titulo | Título del libro |
| Anio | Año de publicación |
| Precio | Precio de venta  
|Editor_ID (FK)	| Editor que publica el libro |
        
2. AUTOR
    
|**Campo** | **Descripción** |
|------|-------------|
|Autor_ID (PK) | Identificador único del autor |
|Nombre	| Nombre del autor |
|Direccion | Dirección del autor |
|URL | Página web personal |

3. EDITOR

| **Campo** | **Descripción** |
|-------|-------------|
|Editor_ID (PK)| Identificador único del editor |
|Nombre | Nombre del editor |
| Direccion| Dirección del editor|
| Telefono|	Número de teléfono|
| URL|	Sitio web del editor|

**Consideración importante**: un libro puede tener varios autores y un autor puede escribir varios libros. Por ello, conviene crear una tabla intermedia LIBRO_AUTOR en lugar de guardar los autores directamente en la tabla LIBRO.

**B. Almacenes e inventario**

4. ALMACEN

| **Campo** | **Descripción** |
|------|------------|
|Almacen_ID (PK)|	Código del almacén
|Direccion| Dirección física
|Telefono|	Número de teléfono|

5. INVENTARIO

| **Campo** | **Descripción** |
|------|------------|
|Almacen_ID (PK, FK) |	Almacén correspondiente
|ISBN (PK, FK) | Libro almacenado|
|Cantidad|	Número de copias disponibles en stock|

La tabla INVENTARIO es necesaria porque existe una relación de muchos a muchos entre libros y almacenes:
- Un almacén puede guardar muchos libros.
- Un mismo libro puede estar almacenado en varios almacenes.
- La cantidad de copias debe registrarse para cada combinación de almacén y libro.
La clave primaria compuesta (Almacen_ID, ISBN) permite mantener una cantidad independiente para cada libro en cada almacén.

**C. Clientes y carritos de compra**

6. CLIENTE

| **Campo** | **Descripción** |
|------|------------|
|Cliente_ID (PK)| Identificador único del cliente|
|Nombre| Nombre del cliente|
|Direccion|	Dirección del cliente|
|Email|	Correo electrónico|
|Telefono|	Número de teléfono|


7. CARRITO_COMPRA

| **Campo** | **Descripción** |
|------|------------|
|Shopping_Cart_ID (PK) | Identificador del carrito
|Cliente_ID (FK)|	Cliente propietario
|Fecha_Creacion|	Fecha de creación
|Estado | Abierto, convertido en pedido o abandonado|


8. DETALLE_CARRITO

| **Campo** | **Descripción** |
|------|------------|
|Shopping_Cart_ID (PK, FK)| Carrito de compra|
|ISBN (PK, FK)|	Libro seleccionado|
|Cantidad|	Copias solicitadas|

La tabla DETALLE_CARRITO resuelve la relación de muchos a muchos entre los carritos y los libros.

Por ejemplo, un carrito puede contener tres copias de un libro y dos copias de otro. La cantidad se almacena en el detalle, evitando crear un registro independiente por cada copia.

**D. Pedidos, direcciones y pagos**

Cuando el cliente confirma el carrito, es necesario registrar la transacción. Para ello, proponemos las siguientes tablas adicionales.

9. PEDIDO

| **Campo** | **Descripción** |
|------|------------|
|Pedido_ID (PK)	| Identificador del pedido|
|Cliente_ID (FK)|	Cliente que realiza la compra|
|Shopping_Cart_ID (FK)|	Carrito de origen, si corresponde|
|Fecha_Pedido|	Fecha de realización|
|Direccion_Facturacion|	Dirección de facturación registrada para el pedido|
|Direccion_Envio|	Dirección de envío registrada para el pedido|
|Opcion_Envio_ID (FK)|	Opción de envío seleccionada|
|Total|	Importe total del pedido|
|Estado	| Pendiente, pagado, enviado, cancelado, etc.|


10. DETALLE_PEDIDO


| **Campo** | **Descripción** |
|------|------------|
Pedido_ID (PK, FK)	Pedido correspondiente
ISBN (PK, FK)	Libro solicitado
Cantidad	Número de copias compradas
Precio_Unitario	Precio aplicado en la compra


11. DIRECCION_CLIENTE


| **Campo** | **Descripción** |
|------|------------|
Direccion_ID (PK)	Identificador de la dirección
Cliente_ID (FK)	Propietario de la dirección
Calle	Calle y número
Ciudad	Ciudad
Estado_Provincia	Estado o provincia
Codigo_Postal	Código postal
Pais	País


12. OPCION_ENVIO

| **Campo** | **Descripción** |
|------|------------|
Opcion_Envio_ID (PK)	Identificador de la opción
Nombre	Tipo de envío
Costo	Costo del envío
Tiempo_Estimado	Tiempo estimado de entrega


13. PAGO


| **Campo** | **Descripción** |
|------|------------|
|Pago_ID (PK)|	Identificador del pago
|Pedido_ID (FK)|	Pedido asociado
|Fecha_Pago|	Fecha de la transacción
|Metodo_Pago|	Tarjeta u otro método
|Referencia_Transaccion|	Referencia del proveedor de pagos
|Importe|	Importe pagado
|Estado_Pago|	Pendiente, aprobado o rechazado


14. NOTIFICACION


| **Campo** | **Descripción** |
|------|------------|
|Notificacion_ID (PK)|	Identificador de la notificación|
|Pedido_ID (FK)| Pedido relacionado|
|Email_Destino|	Correo del cliente|
|Fecha_Envio| Fecha y hora de envío|
|Estado| Enviada, pendiente o fallida|

> Nota de diseño: para mantener la información histórica, es preferible conservar en el pedido una copia de las direcciones seleccionadas en el momento de la compra, aunque el cliente posteriormente modifique su dirección. En un diseño físico, las direcciones de facturación y envío pueden normalizarse en una tabla relacionada con el pedido.

Asimismo, por seguridad, no conviene almacenar directamente el número completo de la tarjeta bancaria. Es preferible utilizar un proveedor de pagos y guardar su referencia o token, además del estado de la transacción.



![alt text](../Img/image.png)