![alt text](../Img/image.png)

# Proyecto de diseño de base de datos
## Base de datos de la tienda Oracle Baseball League

**Escenario del proyecto**:
Usted es una pequeña empresa de consultoría especializada en el desarrollo de bases de datos. Le acaban de adjudicar un contrato para desarrollar un modelo de datos para un sistema de aplicaciones de bases de datos de una pequeña tienda denominada Oracle Baseball League (OBL). 

La tienda ofrece servicios de venta de conjuntos de béisbol para toda la comunidad. OBL tiene dos tipos de cliente; hay personas que pueden adquirir artículos como pelotas, zapatillas, guantes, camisas, camisetas serigrafiadas y pantalones.Además, los clientes pueden representar a un equipo cuando adquieren uniformes y equipación conjunta.

Los equipos y los clientes individuales son libres de comprar cualquier artículo de la lista de inventario, pero los equipos obtienen un descuento en el precio de lista según el número de jugadores. Cuando un cliente realiza un pedido, registramos los artículos de ese pedido en nuestra base de datos.

El equipo de OBL cuenta con tres representantes de ventas que oficialmente solo atienden a equipos, pero se sabe que gestionan las quejas de los clientes individuales.

## Sección 2, lección 3, ejercicio 2: Entidades y atributos

**Identificación de atributos (objetivo 2 de S2L3)**
Para entender mejor el sistema, se celebró una reunión con el manager de la tienda Oracle Baseball League. A continuación se ofrecen detalles de la transcripción de la conversación mantenida:

**Transcripción de la reunión**

**Entrevistador**: En la información proporcionada, ha indicado que existen dos tipos de cliente: individual y equipo. ¿Qué información guarda sobre los clientes y cómo distingue los dos tipos de cliente?

**Manager**: De todos los clientes, realizamos un seguimiento del nombre, la dirección, el número de teléfono, la dirección de correo electrónico y, dado el caso, el equipo al que pertenecen. También se realiza un seguimiento del saldo actual del cliente en nuestro sistema.

**Entrevistador**: Ha dicho que los clientes pueden realizar un pedido de cualquier artículo de la lista de inventario. ¿Qué tipos de artículos pueden comprar?

**Manager**: Los clientes individuales pueden adquirir artículos como pelotas, zapatillas, guantes, camisas, camisetas serigrafiadas y pantalones. Además, los equipos pueden realizar pedidos de toda la equipación, así como de pelotas, camisetas de calentamiento y para jugar, y obtener un descuento sobre la lista de precio según el número de jugadores de dicho equipo. Cuando un equipo compra artículos de la tienda, es necesario que el cliente registrado de ese equipo realice el pedido.

**Entrevistador**: ¿Tiene alguna información específica sobre artículos vendidos que desea registrar en el sistema?

**Manager**: Los clientes nunca compran artículos sin verlos, así que siempre hay una descripción y un precio disponible. El seguimiento de los artículos de inventario forma parte del negocio, así como la descripción y el precio. Realizamos un seguimiento del nombre, color (si procede), tamaño (si procede) y categoría del artículo. Hay tres categorías de artículos que utilizamos: ropa, equipación y otros. Para nuestro inventario, también realizamos un seguimiento del coste unitario del mayorista, así como del número de unidades disponibles; cuando no disponemos de unidades, se registra un cero en el sistema.

**Entrevistador**: ¿Cómo registra los artículos que han pedido los clientes?

**Manager**: Cuando un cliente realiza un pedido, registramos los siguientes detalles de la compra: la fecha, los artículos comprados, el tamaño del artículo, el color, el número de unidades y el precio de cada unidad. También nos gustaría guardar el precio total del pedido para todos los artículos solicitados.

**Entrevistador**: Existen tres representantes de ventas en la empresa, ¿cuál es su función?

**Manager**: Cada cliente de equipo tiene asignado un representante de ventas como vendedor que trabaja a comisión; no se permite que dos vendedores atiendan al mismo cliente. Aunque los representantes de ventas solo atienden a los equipos, es sabido que atienden quejas de los clientes individuales.

**Entrevistador**: ¿Cómo registra los detalles de los representantes de ventas en el sistema?

**Manager**: Para cada uno de los tres representantes de ventas, realizamos un seguimiento de su nombre, dirección, teléfono, dirección de correo electrónico, comisión total y tipo de comisión.
Analizando el texto del escenario especificado, identifique las posibles entidades que se utilizarán para almacenar información sobre las entidades identificadas previamente. Los atributos suelen encontrarse al identificar los sustantivos
que describen otros nombres (nuestras entidades).

Posibles entidades
- Customer
- Team
- Sales Representative
- Order
- Item
- Inventory List

