![alt text](../Img/image.png)

# 1.4 Proyecto: Desarrollo del diseño de base de datos de la tienda Oracle Baseball League

## Requisitos de negocio

## A. Reglas de negocio
1. OBL comercializa artículos relacionados con el béisbol.
2. Existen dos tipos de clientes: individuales y equipos.
3. Ambos tipos de clientes pueden comprar cualquier artículo del inventario.
4. Cada pedido debe registrar los artículos solicitados y sus cantidades.
5. Los equipos reciben descuentos según el número de jugadores que los integran.
6. Los artículos tienen un precio de lista que sirve como referencia para calcular los descuentos.
7. OBL cuenta con tres representantes de ventas que oficialmente atienden a los equipos.
8. Los representantes también gestionan las quejas de los clientes individuales.

## B. Suposiciones
1. Cada cliente, artículo, pedido y representante tendrá un identificador único.
2. Un pedido puede incluir varios artículos y un artículo puede aparecer en distintos pedidos.
3. Cada equipo tendrá registrado su número de jugadores.
4. Existirá una política de descuentos que determinará los beneficios según el tamaño del equipo.
5. Se conservarán los precios aplicados a los pedidos para mantener un historial correcto de las compras.
6. Las quejas podrán registrarse y asociarse con el representante responsable.

## C. Problemas
1. No se especifican los porcentajes ni los rangos de descuentos aplicables a los equipos.
2. No se detallan los datos que deben almacenarse para cada tipo de cliente.
3. No se define cómo se registran los jugadores que integran cada equipo.
4. No se explica cómo se gestionan las modificaciones y cancelaciones de pedidos.
5. Existe una diferencia entre las funciones oficiales de los representantes y las actividades que realizan al atender quejas de clientes individuales.
6. No se describe el proceso para registrar, asignar y dar seguimiento a las quejas.
7. No se especifica si el sistema debe controlar las existencias del inventario.

## D. Necesidades de negocio
La base de datos debe permitir administrar clientes individuales y equipos, mantener el inventario de artículos, registrar pedidos y sus detalles, calcular los descuentos correspondientes a los equipos y dar seguimiento a la actividad de los representantes de ventas y a las quejas de los clientes.

Estas reglas, suposiciones y problemas servirán como base para definir las entidades, los atributos, las claves primarias y foráneas y las relaciones del modelo de datos.

#### Esta es la evidencia que corresponde al <a href="/Seccion_1_Introduccion/1_4_Project.md">Proyecto</a> de la lección <a href="/Seccion_1_Introduccion/1_4_Requisitos_de_negocio.md"> 1.4 Requisitos de negocio </a> del curso  Database Foundations de Oracle Academy.

![alt text](../Img/image.png)