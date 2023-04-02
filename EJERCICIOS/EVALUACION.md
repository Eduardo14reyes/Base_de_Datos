## Práctica 1.

1. Introducción a base de datos

Objetivo: Identificar el nivel de comprensión de los conceptos de base de datos,
mediante preguntas abiertas.
 
Preguntas:

1. ¿Cuáles son las cinco funciones principales del administrador de bases de datos?  

Diseño de bases de datos: El DBA es responsable del diseño y la implementación de la base de datos. Esto incluye la definición de la estructura de datos, las relaciones entre las tablas y la selección del motor de base de datos más adecuado para satisfacer las necesidades de la organización.

Configuración y mantenimiento de la base de datos: El DBA es responsable de asegurarse de que la base de datos esté configurada correctamente y que funcione de manera óptima. Esto implica la realización de tareas de mantenimiento, como la copia de seguridad y la recuperación de datos, la gestión del rendimiento y la optimización de la base de datos.

Gestión de seguridad: El DBA es responsable de garantizar que la base de datos esté segura y protegida contra amenazas externas e internas. Esto implica la implementación de medidas de seguridad, como la gestión de permisos y la autenticación de usuarios, la monitorización de la actividad de la base de datos y la identificación y resolución de posibles vulnerabilidades.

Resolución de problemas: El DBA es responsable de identificar y resolver cualquier problema que surja en la base de datos, como errores de rendimiento, problemas de integridad de datos o fallos del sistema. Esto implica la realización de tareas de diagnóstico, la identificación de la causa raíz del problema y la implementación de soluciones para resolverlo.

Planificación y gestión de cambios: El DBA es responsable de planificar y gestionar cualquier cambio que se realice en la base de datos, como la implementación de nuevas características o la actualización del software de la base de datos. Esto implica la realización de pruebas de integración, la implementación de cambios de manera controlada y la comunicación con otros miembros del equipo para garantizar una implementación exitosa.
(valor 1.5)

2. Indíque cinco responsabilidades del sistema gestor de bases de datos
Almacenamiento y recuperación de datos: el sistema gestor de bases de datos es responsable de almacenar y recuperar los datos de manera eficiente. Esto implica la creación y gestión de estructuras de almacenamiento, la organización de los datos en tablas o archivos y la implementación de mecanismos de recuperación en caso de fallos.

Mantenimiento de la integridad de los datos: el sistema gestor de bases de datos es responsable de garantizar que los datos almacenados sean precisos, completos y consistentes. Para ello, debe implementar restricciones de integridad (como claves primarias y foráneas) y mecanismos de validación de datos.

Control de acceso y seguridad: el sistema gestor de bases de datos debe controlar el acceso a los datos y garantizar su seguridad. Esto implica la autenticación de usuarios, la gestión de permisos y la implementación de mecanismos de protección de datos sensibles.

Gestión de transacciones: el sistema gestor de bases de datos es responsable de garantizar la consistencia de los datos en caso de operaciones concurrentes. Esto implica la gestión de transacciones (conjuntos de operaciones que deben ejecutarse como una unidad atómica) y la implementación de mecanismos de control de concurrencia.

Optimización de consultas y rendimiento: el sistema gestor de bases de datos es responsable de optimizar las consultas realizadas sobre los datos para mejorar el rendimiento del sistema. Esto implica la generación de planes de ejecución eficientes y la implementación de índices y otros mecanismos de optimización. (valor 1.5)

3. En una BD al usuario del sistema se le brindarán recursos para realizar diversas
operaciones sobre estos archivos, tales como:  Consultas: el usuario puede realizar consultas para obtener información específica de los datos almacenados en la base de datos. Las consultas pueden ser simples o complejas y pueden incluir criterios de búsqueda.

Inserción de datos: el usuario puede agregar nuevos datos a la base de datos mediante la inserción de registros o la actualización de registros existentes.

Actualización de datos: el usuario puede actualizar los datos existentes en la base de datos para corregir errores o para agregar nueva información.

Eliminación de datos: el usuario puede eliminar datos de la base de datos cuando ya no sean necesarios o relevantes.

Generación de informes: el usuario puede crear informes y estadísticas sobre los datos almacenados en la base de datos para su uso en la toma de decisiones y análisis de negocio.

Gestión de usuarios y permisos: el usuario también puede gestionar los usuarios y los permisos de acceso a la base de datos, permitiendo o restringiendo el acceso a los datos según sea necesario.

Respaldo y recuperación: el usuario puede realizar copias de seguridad de la base de datos para proteger los datos y asegurar su recuperación en caso de fallos en el sistema. También puede restaurar la base de datos a partir de las copias de seguridad. (valor 1.5)

4. ¿Qué es un Sistema de Información? 
5. Un sistema de información es un conjunto de componentes interrelacionados que trabajan juntos para recopilar, procesar, almacenar y distribuir información con el fin de apoyar la toma de decisiones, la coordinación y el control en una organización.(valor 1.5)

## Práctica 2.

2. Diseño de un modelo relacional

Objetivo: Representar desde un modelo entidad relación un problema


Ejercicio:

Tenemos que diseñar una base de datos sobre proveedores y disponemos de la siguiente
información:

Realiza el modelo entidad relación. (valor 6)

Tenemos esta información sobre una cadena editorial:

● La editorial tiene varias sucursales, con su domicilio, teléfono y un código de
sucursal.

● Cada sucursal tiene varios empleados, de los cuales tendremos su nombre,
apellidos, NIF y teléfono. Un empleado trabaja en una única sucursal.

● En cada sucursal se publican varias revistas, de las que almacenaremos su título,
número de registro, periodicidad y tipo.

● Una revista puede ser publicada por varias sucursales.

● La editorial tiene periodistas (que no trabajan en las sucursales) que pueden
escribir artículos para varias revistas. Almacenaremos los mismos datos que para
los empleados, añadiendo su especialidad.

● También es necesario guardar las secciones fijas que tiene cada revista, que
constan de un título y una extensión.

● Para cada revista, almacenaremos información de cada ejemplar, que incluirá la
fecha, número de páginas y el número de ejemplares vendidos.


Entidades:

Editorial
Sucursal
Atributos:

Editorial: N/A
Sucursal: código_sucursal, domicilio, telefono
Relaciones:

La editorial tiene varias sucursales (1:N)
Diagrama ER:

lua
Copy code
      +---------------------+
      |     Editorial       |
      +---------------------+
      |                     |
      |                     |
      +---------------------+
               |
               |
               |
               |
      +---------------------+
      |      Sucursal       |
      +---------------------+
      | codigo_sucursal (PK)|
      |     domicilio       |
      |      telefono       |
      | id_editorial (FK)   |
      +---------------------+
Este modelo ER muestra una relación uno a muchos entre la entidad Editorial y la entidad Sucursal, donde una editorial puede tener varias sucursales, pero cada sucursal solo puede pertenecer a una editorial. 
