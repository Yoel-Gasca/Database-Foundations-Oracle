
![alt text](../Img/image.png)

# Fundamentos de bases de datos
## 1-4: Requisitos de negocio
### Prácticas
**Ejercicio 1: Requisitos de negocio**

Visión general:
- En esta práctica, analizará el escenario de caso proporcionado e identificará las reglas de negocio.

### Tareas
1. LibBook es una biblioteca digital de éxito que alquila CD y proporciona acceso a Internet para examinar su repositorio de artículos y revistas. Con el crecimiento del negocio, LibBook necesita mejorar su sistema de información para adaptarse a los cambios propuestos en el negocio. LibBook atrae a nuevos miembros con facilidad y el número de miembros crece rápidamente. Sin embargo, el número de miembros no es estable, lo que supone un motivo de preocupación. La idea principal es introducir
el concepto de inscripción en LibBook. Los miembros pagarán una cuota de miembro y, en un principio, habrá tres tipos de miembros (corporativo, alumno, particular) aunque se pueden introducir otros más adelante. La inscripción para alumnos es gratuita. Los miembros corporativos y de profesorado deben pagar una cuota pero se les otorgan privilegios. El tipo de miembro solo se puede cambiar si se aporta una justificación válida. 

**Su tarea consiste en identificar las reglas de negocio y las restricciones asociadas a partir del escenario del caso descrito.**

**Reglas de negocio identificadas**

A partir del escenario de LibBook se pueden identificar las siguientes reglas de negocio y restricciones:

1. LibBook debe contar con un proceso de inscripción para registrar a sus miembros.
2. Cada miembro debe tener un tipo de membresía.
3. Inicialmente se consideran tres tipos de miembros: corporativo, alumno y particular.
4. El diseño debe permitir agregar nuevos tipos de membresía en el futuro.
5. La inscripción para los alumnos es gratuita, por lo que su cuota debe ser igual a cero.
6. Los miembros corporativos deben pagar una cuota de membresía.
7. Los miembros de profesorado deben pagar una cuota y recibir privilegios adicionales.
8. Los miembros corporativos y de profesorado deben tener privilegios asociados a su tipo de membresía.
9. Un miembro no puede cambiar libremente su tipo de membresía.
10. Para cambiar el tipo de membresía se debe proporcionar una justificación válida.
11. Los cambios de tipo de membresía deben registrarse para mantener un historial de las modificaciones.
12. Las cuotas deben estar relacionadas con el tipo de membresía correspondiente.
13. El sistema debe permitir administrar el estado de las membresías, debido a que el número de miembros puede cambiar con el tiempo.
14. El sistema debe estar diseñado de manera flexible para soportar nuevos tipos de miembros, cuotas y privilegios en el futuro.

**Restricciones identificadas**

Una restricción importante es que el tipo de membresía vigente de un miembro debe ser único en un momento determinado. Sin embargo, un miembro puede cambiar de tipo a lo largo del tiempo siempre que exista una justificación válida y el cambio sea registrado.

También existe una inconsistencia en el escenario: inicialmente se mencionan los tipos corporativo, alumno y particular, pero posteriormente se menciona al profesorado como un tipo que debe pagar una cuota. Esta situación debe aclararse antes de implementar la base de datos para determinar si profesorado constituye un cuarto tipo de miembro o si se trata de un error en la descripción del caso.


2. El hospital Star Care es un hospital con varias especialidades que atiende las necesidades de diferentes pacientes. A cada
médico registrado en este hospital se le asigna un ID único que empieza por las letras "DC". El hospital garantiza que los médicos
asociados tienen un mínimo de siete años de experiencia laboral. Cada paciente se debe registrar en el hospital en su primera
visita. Cuando llega un paciente, se le asigna un número de paciente único que empieza por las letras "PT".
**Su tarea consiste en identificar las reglas de negocio y las restricciones asociadas a partir del escenario del caso descrito.**

**Restricciones identificadas**
En el escenario del hospital Star Care se pueden identificar las siguientes reglas de negocio:

1. Todos los médicos asociados al hospital deben estar registrados en el sistema.
2. Cada médico debe tener un identificador único.
3. El identificador de cada médico debe comenzar con las letras "DC".
4. El identificador del médico no puede repetirse entre los médicos registrados.
5. Todo médico asociado al hospital debe contar con un mínimo de siete años de experiencia laboral.
6. El sistema no debe permitir registrar como médico asociado a una persona que tenga menos de siete años de experiencia.
7. Todo paciente debe registrarse en el hospital durante su primera visita.
8. Cada paciente debe recibir un número de paciente único.
9. El número de paciente debe comenzar con las letras "PT".
10. El número asignado a un paciente debe mantenerse para sus futuras visitas y no debe generarse un nuevo número en cada visita.
11. Los identificadores de médicos y pacientes deben cumplir con los formatos establecidos para permitir diferenciarlos.
12. El sistema debe permitir registrar las diferentes especialidades médicas que ofrece el hospital.

**Restricciones identificadas**
Las principales restricciones de integridad son que el ID del médico debe ser único, comenzar con "DC" y corresponder a un médico con al menos siete años de experiencia. De igual manera, el número de paciente debe ser único y comenzar con "PT".

Además, el registro del paciente debe realizarse en su primera visita y posteriormente el mismo identificador debe utilizarse para las visitas subsecuentes.

Estas reglas permitirán establecer posteriormente restricciones de la base de datos, como claves primarias, valores únicos, validaciones de formato y restricciones sobre los años de experiencia.

#### Esta es la evidencia que corresponde a la <a href="/Seccion_1_Introduccion/1_4_Practicas.md">tarea</a> de la lección <a href="/Seccion_1_Introduccion/1_4_Requisitos_de_negocio.md"> 1.4 Requisitos de negocio </a> del curso  Database Foundations de Oracle Academy.

![alt text](../Img/image.png)
