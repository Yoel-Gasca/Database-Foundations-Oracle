# Practica 2: Sistema de gestión de bibliotecas

## Escenario de caso 2
La comunidad XYZ desea crear un sistema de gestión de bibliotecas. El objetivo es que la base de datos administre todas las transacciones de la biblioteca. La base de datos debe almacenar todos los datos relevantes para la gestión de los libros, la gestión de clientes, y las actividades diarias de la biblioteca. Cree una lista de los datos importantes que se deben recopilar y almacenar en la base de datos de gestión de bibliotecas.

## Realización del ejercicio
En este caso conviene separar la información en **libros**, **ejemplares**, **clientes**, **préstamos** y **actividades**/**transacciones**, porque un mismo libro puede tener varios ejemplares y cada ejemplar puede tener diferentes movimientos.

1. Datos importantes para el sistema de gestión de bibliotecas

| Categoría                  | Datos que se pueden recopilar                                                                                                             |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Información del libro**  | ISBN, título, autor, editorial, año de publicación, género/categoría, idioma                                                              |
| **Ejemplares**             | ID del ejemplar, ISBN/libro al que pertenece, ubicación, estado físico, disponibilidad                                                    |
| **Autores**                | ID del autor, nombre completo, nacionalidad, fecha de nacimiento                                                                          |
| **Clientes/usuarios**      | ID del cliente, nombre completo, teléfono, correo electrónico, domicilio, fecha de registro, estado de la cuenta                          |
| **Préstamos**              | ID del préstamo, cliente, ejemplar prestado, fecha de préstamo, fecha límite de devolución, fecha real de devolución, estado del préstamo |
| **Devoluciones**           | Fecha de devolución, condición del ejemplar, retraso, observaciones                                                                       |
| **Reservaciones**          | Cliente, libro solicitado, fecha de solicitud, fecha de vencimiento de la reserva y estado                                                |
| **Multas**                 | ID de la multa, cliente, préstamo relacionado, motivo, importe, fecha de generación, estado de pago y fecha de pago                       |
| **Personal de biblioteca** | ID del empleado, nombre, puesto y datos de acceso al sistema                                                                              |
| **Actividades diarias**    | Altas de libros, bajas, préstamos, devoluciones, renovaciones, reservas y pagos de multas                                                 |
| **Auditoría**              | Usuario que realizó la operación, tipo de operación, fecha y hora de la operación                                                         |

Para crear el sistema de gestión de bibliotecas de la comunidad XYZ, se deben recopilar y almacenar los datos necesarios para administrar los libros, los usuarios, los ejemplares y todas las transacciones que se realizan diariamente

**Posible estructura de la base de datos**

Para diseñar posteriormente el modelo relacional, se  tendrían entidades como:

- LIBROS
- AUTORES
- EDITORIALES
- CATEGORIAS
- EJEMPLARES
- CLIENTES
- PRESTAMOS
- DEVOLUCIONES
- RESERVAS
- MULTAS
- EMPLEADOS

Los principales datos que se deben almacenar son:

1. **Datos de los libros:** ISBN, título, autor, editorial, año de publicación, género o categoría e idioma.
2. **Datos de los ejemplares:** identificador del ejemplar, libro al que pertenece, ubicación, estado físico y disponibilidad.
3. **Datos de los autores:** identificador, nombre completo y otros datos relevantes del autor.
4. **Datos de los clientes:** identificador del cliente, nombre completo, teléfono, correo electrónico, domicilio, fecha de registro y estado de la cuenta.
5. **Datos de los préstamos:** identificador del préstamo, cliente, ejemplar, fecha de préstamo, fecha límite de devolución, fecha de devolución y estado del préstamo.
6. **Datos de las devoluciones:** fecha de devolución, condición del ejemplar, retrasos y observaciones.
7. **Datos de las reservaciones:** cliente, libro solicitado, fecha de solicitud, fecha de vencimiento y estado de la reserva.
8. **Datos de las multas:** identificador de la multa, préstamo relacionado, motivo, importe, fecha de generación, estado y fecha de pago.
9. **Datos del personal de la biblioteca:** identificador del empleado, nombre, puesto y datos necesarios para controlar el acceso al sistema.
10. **Datos de las actividades y transacciones:** préstamos, devoluciones, renovaciones, reservas, altas y bajas de ejemplares y pagos de multas.
11. **Datos de auditoría:** usuario que realizó cada operación, tipo de operación, fecha y hora.

La base de datos debe relacionar adecuadamente esta información para poder conocer qué libros y ejemplares existen, qué clientes están registrados, qué libros se encuentran prestados o disponibles, qué préstamos están pendientes y qué multas o reservas existen.

Además, cada libro, ejemplar, cliente y transacción debe contar con un identificador único para evitar duplicidad y facilitar las consultas y operaciones del sistema.


#### Esta es la evidencia que corresponde a la <a href="/Seccion_1_Introduccion/1_2_Practicas.md">tarea</a> de la lección <a href="/Seccion_1_Introduccion/1_2_Introduccion_a_las_BasesdeDatos.md">1-2: Introducción a la base de datos</a> del curso  Database Foundations de Oracle Academy.

![alt text](../Img/OracleLogo2.png)