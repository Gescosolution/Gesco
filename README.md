# Gesco

Software para la gestión de proyectos. Publicado bajo licencia GNU GENERAL PUBLIC LICENSE Version 2.

# Miembros:

- Abel Francisco Agra: [@jfrancisco4490](https://github.com/jfrancisco4490)
- Fernando Llodra Belda: [@fllodrab](https://github.com/fllodrab)
- Germán Martínez Maldonado: [@germaaan](https://github.com/germaaan)
- Roberto Morcillo Jiménez: [@robermorji](https://github.com/robermorji)
- Francisco Navarro González: [@fnavarrogonzalez](https://github.com/fnavarrogonzalez)

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

Aunque el proyecto se va a presentar como un “todo”, se busca desarrollarlo de la forma más modular posible, así por ejemplo definiríamos los siguientes grandes módulos de nuestra aplicación:

- Acceso al sistema
- Gestión de archivos e información
- Gestión de tareas de proyectos
- Generación de informes

Como comentábamos en la descripción del proyecto todo el sistema se va a basar en una plataforma web, por lo que el lenguaje elegido para el desarrollo es **PHP** porque es un lenguaje fácil de utilizar, potente y que además provee de unos mecanismos para gestionar fácilmente bases de datos; también junto a PHP usaremos el framework **[Symfony](https://github.com/symfony/symfony)**, que es uno de los frameworks para crear aplicaciones web más potentes que podemos encontrar para este lenguaje.

Además, vamos a seguir una metodología de desarrollo continuo como es **DevOps**; esto implica que el desarrollo principal de la aplicación del proyecto debe ser una desarrollo basado en pruebas, por lo que desarrollaremos pruebas unitarias para cada una de las funcionalidades de la aplicación, para también basándonos en el funcionamiento de dichas pruebas incorporar un sistema de integración continua que verifique a cada cambio que la estabilidad del programa sigue siendo la que debe ser y que no se han introducido errores que derivarían en problemas durante la ejecución de la aplicación. Las pruebas unitarias se pueden realizar con **[PHPUNIT](https://github.com/sebastianbergmann/phpunit)** y la integración continua usaremos **[Travis CI](https://github.com/travis-ci/travis-ci)**.

Según vayamos consiguiendo que la aplicación sea funcional, solo quedará desplegarla en un PaaS como puede ser Azure (aprovechando que tenemos acceso a cuentas durante 6 meses), pero antes de desplegar la aplicación en el servidor tendremos que provisionarlo con todos los recursos software necesarios. El provisionamiento se puede hacer con **[Ansible](https://github.com/ansible/ansible)** mientras que el despliegue automático se puede hacer con **[Rocketeer](https://github.com/rocketeers/rocketeer)**.

# Relación con la asignatura

La aplicación principal del proyecto en sí misma no tendría una relación específica con la asignatura al margen de ser una plataforma web, es por eso que aplicarle todos los aspectos que implican un desarrollo continuo como son desarrollo basado en pruebas, integración continua, provisionamiento software o despliegue automático (temas básicos de la asignatura), es lo que hará que este sea un buen proyecto para realizar.
