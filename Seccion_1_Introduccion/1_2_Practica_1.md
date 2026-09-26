
# Practica 1: Sistema de registro del alumno

## Escenario de caso 1
El distrito escolar ABC desea crear un sistema de registro e información del alumno en línea para recopilar información
relacionada con los alumnos. El sistema se debe diseñar como un proceso en línea para permitir que los nuevos alumnos se
registren en línea. También debe permitir que los alumnos existentes actualicen y revisen toda la información. Cree una lista de
los datos importantes que se deben recopilar y almacenar en la base de datos de registro de alumnos.

## Realización del ejercicio
Para este ejercicio, la idea es identificar qué información necesita almacenar el sistema para registrar, consultar y mantener actualizados los datos de los alumnos, procurando no recopilar datos innecesarios.

1. Datos importantes para el sistema de registro de alumnos

| Categoría                             | Datos que se pueden recopilar                                                                            |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| **Identificación del alumno**         | ID del alumno, nombre, apellido paterno, apellido materno, fecha de nacimiento, sexo/género              |
| **Datos de contacto**                 | Teléfono, correo electrónico, domicilio, ciudad, estado, código postal                                   |
| **Información académica**             | Grado, grupo, ciclo escolar, fecha de inscripción, programa o nivel educativo, turno                     |
| **Información de los padres/tutores** | Nombre del padre, madre o tutor, parentesco, teléfono, correo electrónico, domicilio                     |
| **Contacto de emergencia**            | Nombre, parentesco, teléfono y dirección del contacto de emergencia                                      |
| **Historial escolar**                 | Escuelas anteriores, grados cursados, calificaciones o historial académico, fecha de ingreso             |
| **Información administrativa**        | Estado de inscripción, fecha de alta, fecha de baja, motivo de baja                                      |
| **Información médica relevante**      | Alergias, condiciones médicas relevantes, medicamentos que deban considerarse durante la jornada escolar |
| **Información adicional**             | Necesidades educativas especiales, autorizaciones escolares y observaciones relevantes                   |

Para crear el sistema de registro e información del alumno del distrito escolar ABC, se deben recopilar y almacenar los datos necesarios para identificar al alumno, mantener actualizada su información y administrar correctamente su inscripción.

**Posibles tablas de la base de datos**

Los datos se podrían organizar en las siguientes tablas:

- **ALUMNOS** → información principal del estudiante.
- **CONTACTOS** → padres, tutores y contactos de emergencia.
- **DIRECCIONES** → domicilios de alumnos y tutores.
- **INSCRIPCIONES** → grado, grupo, ciclo escolar y estado de inscripción.
- **HISTORIAL_ACADEMICO** → cursos, calificaciones y antecedentes escolares.
- **INFORMACION_MEDICA** → información médica necesaria para la atención del alumno.

Los principales datos que se deben almacenar son:

1. **Datos personales:** identificador único del alumno, nombre completo, fecha de nacimiento y sexo/género.
2. **Datos de contacto:** domicilio del alumno, teléfono, correo electrónico del padre o tutor .
3. **Información académica:** grado, grupo, nivel educativo, turno, ciclo escolar y fecha de inscripción.
4. **Información de padres o tutores:** nombre, parentesco, teléfono, correo electrónico y domicilio.
5. **Contacto de emergencia:** nombre, parentesco y datos de contacto de una persona que pueda ser localizada en caso de emergencia.
6. **Historial académico:** escuelas anteriores, grados cursados y calificaciones o antecedentes académicos relevantes.
7. **Información administrativa:** estado de la inscripción, fecha de alta, fecha de baja y, cuando corresponda, motivo de baja.
8. **Información médica relevante:** alergias, condiciones médicas y otra información necesaria para atender adecuadamente al alumno durante su estancia en la escuela.
9. **Información adicional:** necesidades educativas especiales, autorizaciones y observaciones relevantes.

La base de datos debe asignar a cada alumno un identificador único para evitar duplicidad de registros. Además, debe permitir actualizar la información conforme cambien los datos del alumno, manteniendo controles de acceso para proteger la información personal y académica.



#### Esta es la evidencia que corresponde a la <a href="/Seccion_1_Introduccion/1_2_Practicas.md">tarea</a> de la lección <a href="/Seccion_1_Introduccion/1_2_Introduccion_a_las_BasesdeDatos.md">1-2: Introducción a la base de datos</a> del curso  Database Foundations de Oracle Academy.

![alt text](../Img/OracleLogo2.png)