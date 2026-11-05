![alt text](../Img/image.png)

# Fundamentos de bases de datos
## 2-6: Modelado de relaciones entre entidades (ERD)
### Prácticas

**Ejercicio 1: Identificar los componentes del ERD**

**Visión general**

En esta práctica, identificará los componentes en un determinado ERD simple.

### Tareas
1. Identifique las posibles entidades y los atributos del escenario determinado. Una compañía tiene varios departamentos. Cada departamento tiene un supervisor y al menos un empleado. Los empleados se deben asignar por lo menos a un departamento, pero posiblemente, también a varios. Se debe asignar al menos un empleado a un proyecto, pero puede que un empleado esté de vacaciones y no se asigne a ningún proyecto. Los campos de datos importantes son los nombres de los departamentos, proyectos, supervisores y empleados, así como el número de supervisor y de empleado y un número de proyecto único.

2. Interprete el escenario de negocio especificado. Dibuje las entidades HAIRSTYLIST y CLIENT. Muestre los atributos asociados a cada entidad y especifique si son obligatorios u opcionales. Identifique los UID. Siga las convenciones sobre creación de diagramas tratadas. Indique el lenguaje de ERD de las relaciones.

"En nuestro salón, tenemos varios estilistas. Todos ellos son empleados asalariados, por lo que se mantiene un registro de su nombre, apellidos, dirección, número de teléfono, número de la seguridad social y salario. Durante el transcurso de un día, un estilista puede atender a varios clientes. En un día con menos actividad, puede que un estilista no tenga que atender a nadie. Tenemos varios clientes sin cita previa y cada uno se asigna un estilista. Solo les pedimos su nombre. También tenemos clientes que llaman para concertar una cita. En estos casos, les pedimos su nombre, apellidos y número de teléfono. También les preguntamos si desean que les atienda un determinado peluquero. Si no tienen ninguna preferencia, les asignamos uno. Por supuesto, podrán cambiar a otro estilista en su siguiente visita al salón. Estamos interesados en realizar un seguimiento de las citas diarias, es decir, qué estilista trabaja con qué cliente un determinado día".

3. Interprete el escenario de negocio especificado. Dibuje las entidades TEACHER y COURSE y CLASS. Muestre los atributos debajo de cada entidad. Especifique si son obligatorios u opcionales. Identifique los UID. Indique el lenguaje de ERD de las relaciones.

"Tenemos varios profesores en la escuela. A un profesor se le pueden asignar hasta tres clases por semestre. Si un profesor está de vacaciones sabáticas, no impartirá clases ese semestre. Mantenemos un registro del nombre, los apellidos, la dirección, el número de teléfono y la dirección de correo electrónico del profesor. 

Nuestra escuela ofrece muchos cursos, tales como: Modelado de datos, Introducción a SQL, Trigonometría, Física y Biología. Cada curso tiene un código. Por ejemplo: Modelado de datos sería DM001, Trigonometría sería TR004, etc. Durante cada semestre, un mismo curso se puede impartir en varias clases, por lo que podría haber dos clases de Física, tres clases de Biología, etc. Cada clase solo la puede impartir un profesor. Asignamos un ID único para cada clase, además de realizar un seguimiento del día en que se imparte, el horario y el aula"


![alt text](../Img/image.png)