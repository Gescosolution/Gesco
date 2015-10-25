# Gesco

Software para la gestión de proyectos. Publicado bajo licencia GNU GENERAL PUBLIC LICENSE Version 2.

Este proyecto participa en el Certamen de Proyectos Libres de la Universidad de Granada 2015-2016. Las bases del mismo se encuentran [aquí](https://docs.google.com/document/d/16UsdUV_XXuPUh-Imz4PSgh-2ES_YaAJpZ8fNrbTVpMA/edit).

# Miembros:

- Abel Josué Francisco Agra: [@jfrancisco4490](https://github.com/jfrancisco4490)
- Fernando Llodra Belda: [@fllodrab](https://github.com/fllodrab)
- Germán Martínez Maldonado: [@germaaan](https://github.com/germaaan)
- Roberto Morcillo Jiménez: [@robermorji](https://github.com/robermorji)
- Francisco Navarro González: [@fnavarrogonzalez](https://github.com/fnavarrogonzalez)

# Enlaces:

- [Web de la aplicación](http://gescosolution.github.io/Gesco/)
- [Twitter](https://twitter.com/gescosolutionCC)

# Descripción:

Consiste en un sistema web para supervisar y gestionar la información y avances asociados a los proyectos que se desarrollan en una determinada empresa. En principio, la empresa puede tener múltiples oficinas y/o empresas filiales, en cada una de las cuales se llevan a cabo proyectos muy diversos en términos de temática, duración, alcance, etc. El sistema permitirá a los gerentes de la empresa consultar el estado y progreso de los proyectos que se están realizando en cualquier oficina de forma unificada (es decir, si en la oficina 1 los proyectos se definen de una manera y en la oficina 2 de otra, el gerente debe poder ver todos estos proyectos de manera estándar en el sistema).

Por otra parte, los líderes de proyecto de cada oficina podrán definir o crear nuevos proyectos en la plataforma, editarlos, definir tareas en cada proyecto, asignar dichas tareas a miembros de su equipo de trabajo, y, finalmente, cerrar un proyecto.

También se quiere incluir a los miembros del equipo de trabajo en la plataforma, por lo cual, estos deben poder indicar el avance que han logrado en aquellas tareas que el líder les haya asignado. Cada miembro del equipo de trabajo puede subir a la plataforma diversos archivos relacionados con las tareas que ha desarrollado en el proyecto (diagramas, documentos, etc.).

En teoría, como es una empresa con numerosas oficinas, probablemente tenga un sistema centralizado de autenticación, seguridad y manejo de roles; por ello, el sistema debe poder integrarse a la plataforma existente, a fin de que pueda consultar los usuarios que ya están registrados y el rol que tienen en la empresa, y así determinar qué funcionalidades pueden o no pueden activar en el sistema de supervisión de proyectos.

Los gerentes, en principio, no deberían poder editar el estado de los proyectos. Simplemente deben poder hacer consultas sobre los mismos, lo cual incluye la generación de gráficos y otros reportes estadísticos que deben ser definidos.

Finalmente, y dado que cada oficina o empresa filial puede tener sus propias bases de datos independientes, el sistema debe unificar la presentación de datos al gerente, de tal forma que no aparezcan incongruencias al presentar la información procedente de diversas fuentes de datos. Los líderes y miembros de equipos de trabajo solo pueden acceder a la información de los proyectos en los que se encuentran asignados y en la oficina a la que pertenecen.

A continuación se listan algunos requerimientos básicos del sistema:

- Controlar el acceso al sistema, consultando en la plataforma de autenticación de usuarios y manejo de roles ya definida en la empresa.
- Limitar el acceso que tiene el usuario a la información y funcionalidades en el sistema, principalmente en términos de su rol en la empresa y la oficina a la que pertenece.
- Gestionar los datos e información de los proyectos (definir un nuevo proyecto, editar su información básica, y cerrar un proyecto concluido).
- Gestionar las tareas en que se dividen los proyectos (definir una nueva tarea, editar su progreso o avance, cerrar una tarea).
- Asignar tareas a miembros del equipo de trabajo o desarrollo del proyecto.
- Subir archivos, documentos y otros recursos asociados al desarrollo de una tarea en el proyecto.
- Generar informes estadísticos, gráficos y otras consultas específicas para uso de los gerentes de la empresa.
- Estandarizar la presentación de información de los proyectos, cuando ésta provenga de diversas fuentes de datos.

# Motivación

La principal motivación para iniciar este proyecto fue que consideramos que podríamos estar ante una idea original que podría tener aceptación en el mundo empresarial, y aunque no tenemos un cliente establecido, es fácilmente aplicable a cualquier tipo de empresa que tenga una estructura de un tamaño medio.

Además, otro de los objetivos es obtener diversos conocimientos que nos serán necesarios para poder llevar a cabo el proyecto, conocimientos que si no fuera por esta situación quizás no le pondríamos la dedicación necesaria, pero que sin lugar a duda serán muy útiles en nuestro futuro trabajo.

# Procedimiento de realización

Aunque el proyecto se va a presentar como un “todo”, se busca desarrollarlo de la forma más modular posible, así que inicialmente vamos a dividirlo en los siguientes módulos de los que se encargará cada uno de los miembros del:

- Gestión de usuarios y acceso al sistema ([Gesco-UserManagement](https://github.com/Gescosolution/Gesco-UserManagement)): [Abel Josué Francisco Agra](https://github.com/jfrancisco4490)
- Gestión de la comunicación interna ([GescoChat](https://github.com/Gescosolution/GescoChat)): [Fernando Llodra Belda](https://github.com/fllodrab)
- Gestión de información y generación de informes desde base de datos ([Gesco-DatabaseManagement](https://github.com/Gescosolution/Gesco-DatabaseManagement)): [Germán Martínez Maldonado](https://github.com/germaaan)
- Gestión de tareas de proyectos ([Planning-task](https://github.com/Gescosolution/Planning-task)): [Roberto Morcillo Jiménez](https://github.com/robermorji)
- Generación de control de presupuestos([Financial-Management](https://github.com/fnavarrogonzalez/Financial-Management)): [Francisco Navarro González](https://github.com/fnavarrogonzalez)

Cada uno de los módulos tiene su propio repositorio y será añadido como un submódulo Git. El objetivo final es que cuando todos los módulos hayan sido completamente desarrollados, integrarlos todos en esta aplicación para que se pueda hacer un uso conjunto de todas sus funcionalidades desde una única aplicación.

# Relación con la asignatura

Inicialmente la aplicación principal del proyecto en sí misma no tendría una relación específica con la asignatura al margen de usar **Git** como herramienta de control de versiones, el repositorio de **GitHub** en el que está almacenado el código y los **submódulos Git** como los que se han añadido cada uno de los repositorio de los módulos de los integrandes del grupo.

Sin embargo, al igual que en el caso de cada uno de los módulos, cuando todos se junten en la aplicación principal está también deberá incluir y pasas sus pruebas unitarias, realizar la integración continua y poder ser desplegado de forma automática.
