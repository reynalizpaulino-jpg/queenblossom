# Gestión del proyecto mediante Kanban – Queen Blossom

## 1. Introducción

Durante el desarrollo de Queen Blossom se seleccionó la metodología ágil Kanban para organizar las actividades y dar seguimiento al avance del proyecto.

Esta metodología permite visualizar las tareas mediante un tablero dividido en columnas, facilitando la identificación de las actividades pendientes, las que están en proceso y las que ya fueron completadas.

Para gestionar el proyecto se seleccionó GitHub Projects, una herramienta que permite organizar las actividades y relacionarlas con los Issues del repositorio.

## 2. Metodología seleccionada

**Metodología:** Kanban.

**Herramienta:** GitHub Projects.

**Proyecto:** Queen Blossom.

Se seleccionó Kanban porque permite organizar las tareas de forma visual y realizar ajustes conforme avanza el desarrollo.

A diferencia de una planificación que obliga a completar todas las actividades en períodos fijos, Kanban permite mantener un flujo de trabajo continuo, dando prioridad a las tareas que necesitan mayor atención.

Este enfoque resulta adecuado para Queen Blossom porque permite llevar un control de la documentación, los diseños y las futuras actividades de programación.

## 3. Organización del tablero Kanban

El tablero de Queen Blossom se organizó inicialmente mediante cinco columnas.

### Backlog

Contiene las actividades identificadas que todavía no han sido programadas para comenzar.

Estas tareas forman parte del trabajo previsto y podrán priorizarse posteriormente.

### Por hacer

Incluye las actividades que ya fueron seleccionadas para trabajarse, pero que todavía no han comenzado.

### En progreso

Contiene las tareas que se están desarrollando actualmente.

Esta columna permite identificar las actividades que requieren seguimiento durante su realización.

### En revisión

Incluye los trabajos que han sido realizados y necesitan comprobarse antes de considerarse terminados.

La revisión permite verificar que las actividades cumplan con los requisitos establecidos.

### Finalizado

Contiene las tareas completadas y verificadas.

Una actividad debe pasar a esta columna cuando se haya comprobado que cumple con lo solicitado.

## 4. Actividades iniciales del proyecto

Durante la planificación de Queen Blossom se identificaron seis actividades principales.

| N.º | Actividad | Prioridad | Estado inicial |
|---|---|---|---|
| 1 | Documentación de requisitos | Alta | Por hacer |
| 2 | Diseño de la base de datos | Alta | Por hacer |
| 3 | Registro e inicio de sesión | Alta | Por hacer |
| 4 | Diseño de interfaz | Media | Backlog |
| 5 | Diseño del catálogo de productos | Media | Backlog |
| 6 | Carrito de compras | Media | Backlog |

Estos estados corresponden a la planificación inicial del proyecto y no necesariamente representan su situación actual.

## 5. Priorización de las actividades

Las primeras tres actividades se establecieron como prioritarias debido a su importancia para comenzar el desarrollo.

La documentación de requisitos permite identificar las necesidades y funciones del sistema.

El diseño de la base de datos permitirá organizar la información de usuarios, productos, carritos y pedidos.

Por su parte, el registro e inicio de sesión constituye una función importante para controlar el acceso de los usuarios a sus cuentas.

Las demás actividades se organizaron como parte del trabajo que se desarrollaría posteriormente.

## 6. Seguimiento mediante GitHub Issues

Los Issues permiten registrar tareas, historias de usuario, incidencias y mejoras relacionadas con Queen Blossom.

Cada Issue puede incluir una descripción, criterios de aceptación, prioridad y estado de seguimiento.

Durante la etapa de análisis se identificaron cinco historias de usuario relacionadas con las funcionalidades principales del sistema:

- HU-01. Visualizar catálogo de productos.
- HU-02. Registro e inicio de sesión.
- HU-03. Gestionar carrito de compras.
- HU-04. Buscar y filtrar productos.
- HU-05. Revisar resumen del pedido.

La relación entre las historias de usuario y los Issues permite mantener un seguimiento de las funciones que deben desarrollarse y comprobarse.

## 7. Actualización del tablero durante el proyecto

A medida que se completa una actividad, su estado debe actualizarse dentro de GitHub Projects.

Por ejemplo, cuando la documentación de requisitos esté terminada y verificada, la tarea correspondiente podrá trasladarse a Finalizado.

Las actividades que todavía necesiten implementación deberán permanecer en Por hacer o En progreso, dependiendo de su situación.

Cuando una tarea requiera comprobación, deberá ubicarse en En revisión.

Esta organización permite mostrar el avance real del proyecto y evita considerar terminadas actividades que todavía tienen trabajo pendiente.

## 8. Control de avances y cambios

El seguimiento mediante Kanban se complementa con el control de versiones de Git.

Cada vez que se realiza una modificación importante en la documentación o en los archivos del repositorio, se puede registrar mediante un commit.

Los mensajes de los commits permiten identificar qué cambios fueron realizados.

Esto facilita consultar el historial del proyecto y relacionar los avances documentados con las modificaciones registradas en GitHub.

## 9. Estado actual del proyecto

Queen Blossom se encuentra en una etapa de documentación, análisis y diseño técnico.

Durante la asignatura se han trabajado los requisitos funcionales y no funcionales, las historias de usuario, los modelos UML y la arquitectura propuesta.

El estado de cada tarea debe mantenerse actualizado en GitHub Projects, de acuerdo con los avances reales registrados.

**Enlace del tablero de GitHub Projects:**

[Ver tablero Kanban de Queen Blossom](https://github.com/users/reynalizpaulino-jpg/projects/1)

**Repositorio del sistema:**

[Queen Blossom – GitHub](https://github.com/reynalizpaulino-jpg/queenblossom)

El tablero permite consultar el estado de las actividades relacionadas con la documentación, el diseño y las funcionalidades del sistema. Las tareas deberán permanecer en sus respectivas columnas según el avance real del proyecto.

## 10. Próximas actividades

Las siguientes actividades técnicas permitirán continuar el desarrollo de Queen Blossom:

- Revisar y completar las tareas pendientes.
- Verificar los Issues relacionados con las funcionalidades principales.
- Continuar con la implementación del frontend y backend.
- Diseñar e integrar la base de datos.
- Realizar pruebas para comprobar el funcionamiento del sistema.

## 11. Conclusión

La metodología Kanban ha permitido establecer una forma sencilla y organizada de gestionar las actividades de Queen Blossom.

El uso de GitHub Projects facilita visualizar el avance del trabajo, mientras que los Issues permiten dar seguimiento a tareas específicas.

Estas herramientas contribuyen a mantener la organización del proyecto y servirán de apoyo durante las siguientes etapas de desarrollo.