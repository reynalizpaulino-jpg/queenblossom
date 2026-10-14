# Queen Blossom

**Sistema de gestión y venta de productos mediante una plataforma web.**

**Proyecto académico:** Ingeniería de Software I  
**Institución:** Universidad Abierta para Adultos (UAPA)  
**Versión documental:** 0.1.0  
**Estado:** Documentación y diseño técnico inicial.

## 1. Descripción del proyecto

Queen Blossom es un sistema digital diseñado para facilitar la presentación y venta de productos mediante una tienda virtual.

La plataforma permitirá a los clientes consultar un catálogo de productos, registrarse, iniciar sesión, buscar artículos, gestionar un carrito de compras y revisar un resumen del pedido antes de confirmar la compra.

Este proyecto se ha desarrollado durante la asignatura Ingeniería de Software I, aplicando conocimientos relacionados con el análisis de requisitos, las historias de usuario, el modelado UML, la arquitectura de software y la gestión de proyectos mediante GitHub.

## 2. Problema que busca resolver

Muchos negocios necesitan contar con una plataforma digital que les permita presentar sus productos de manera organizada y facilitar el proceso de compra de sus clientes.

Queen Blossom busca responder a esta necesidad mediante una tienda virtual que reúna la información de los productos y permita realizar las principales actividades de compra desde un mismo lugar.

De esta manera, se pretende mejorar la organización de los productos y ofrecer una experiencia sencilla para los usuarios.

## 3. Objetivo general

Diseñar y desarrollar una plataforma web para la gestión y venta de productos, que permita a los clientes consultar artículos, administrar un carrito de compras y revisar sus pedidos de manera organizada y segura.

## 4. Funcionalidades principales

Durante la etapa de análisis se identificaron cinco requisitos funcionales.

| Código | Funcionalidad | Descripción |
|---|---|---|
| RF-01 | Catálogo de productos | Mostrar nombre, imagen, precio y descripción de los artículos. |
| RF-02 | Registro e inicio de sesión | Permitir que los usuarios creen una cuenta y accedan de forma segura. |
| RF-03 | Carrito de compras | Agregar, eliminar y modificar cantidades de productos. |
| RF-04 | Búsqueda y filtros | Facilitar la localización de productos. |
| RF-05 | Resumen del pedido | Mostrar artículos, cantidades y total antes de confirmar la compra. |

Estas funcionalidades se encuentran documentadas y servirán como base para la implementación del sistema.

## 5. Arquitectura del sistema

Para Queen Blossom se propone una arquitectura cliente-servidor con separación entre frontend, backend y base de datos.

### 5.1. Frontend

El frontend utilizará una arquitectura basada en componentes, con React como tecnología propuesta.

Sus principales responsabilidades serán:

- Presentar las pantallas y el catálogo de productos.
- Mostrar los formularios de registro e inicio de sesión.
- Permitir la búsqueda y selección de artículos.
- Mostrar y actualizar visualmente el carrito.
- Comunicarse con el backend mediante servicios API.

La organización propuesta incluirá páginas, componentes reutilizables, servicios y recursos estáticos.

### 5.2. Backend

El backend utilizará una arquitectura MVC (Modelo-Vista-Controlador), complementada con una capa de servicios.

Se propone utilizar Node.js con Express para su futura implementación.

**Modelos:** representarán las entidades y permitirán gestionar los datos de usuarios, productos, carritos y pedidos.

**Controladores:** recibirán las solicitudes HTTP y coordinarán las operaciones correspondientes.

**Servicios:** contendrán las reglas del negocio, como la validación de información y el cálculo de los totales.

**Representación de datos:** el backend devolverá respuestas JSON mediante una API, mientras que el frontend se encargará de presentar visualmente la información.

### 5.3. Base de datos

La base de datos almacenará la información relacionada con las principales entidades del sistema:

- Usuario.
- Producto.
- Carrito.
- ItemCarrito.
- Pedido.

La tecnología de almacenamiento se definirá durante la etapa de implementación.

### 5.4. Comunicación entre frontend y backend

La comunicación se realizará mediante solicitudes HTTP a una API que intercambiará información en formato JSON.

Por ejemplo, cuando un cliente agregue un producto al carrito, el frontend enviará una solicitud al backend. El controlador recibirá la petición y utilizará el servicio correspondiente para validar y procesar la operación.

Posteriormente, el backend devolverá una respuesta y el frontend actualizará la información presentada en pantalla.

Esta organización permitirá separar las responsabilidades de cada parte del sistema.

**Documentación técnica:**

- [Arquitectura general](docs/architecture/overview.md)
- [Organización del frontend y backend](docs/architecture/frontend-backend.md)

## 6. Herramientas y tecnologías

| Herramienta | Propósito |
|---|---|
| Git | Control de versiones de los archivos del proyecto. |
| GitHub | Almacenamiento y seguimiento del repositorio. |
| GitHub Issues | Registro y seguimiento de actividades técnicas. |
| GitHub Projects | Organización del trabajo mediante Kanban. |
| Visual Paradigm Online | Modelado de los diagramas UML. |
| Markdown | Elaboración de la documentación técnica. |
| React | Tecnología propuesta para el frontend. |
| Node.js y Express | Tecnologías propuestas para el backend. |

Las tecnologías de implementación se presentan como parte del diseño propuesto y no como funcionalidades que ya se encuentren programadas.

## 7. Metodología de trabajo

Para organizar las actividades de Queen Blossom se seleccionó la metodología ágil Kanban, utilizando GitHub Projects como herramienta de planificación y seguimiento.

El tablero permite visualizar las tareas y conocer su avance mediante cinco estados:

1. **Backlog:** actividades identificadas que todavía no han sido programadas.
2. **Por hacer:** tareas pendientes de comenzar.
3. **En progreso:** actividades que se encuentran en desarrollo.
4. **En revisión:** trabajos realizados que necesitan ser comprobados.
5. **Finalizado:** actividades completadas y verificadas.

Los Issues se utilizan para dar seguimiento a historias de usuario, incidencias, riesgos, mejoras y tareas pendientes del proyecto.

### Tablero Kanban

[Consultar tablero de Queen Blossom en GitHub Projects](https://github.com/users/reynalizpaulino-jpg/projects/1)

### Seguimiento de Issues

[Consultar los Issues del repositorio](https://github.com/reynalizpaulino-jpg/queenblossom/issues)

### Documentación relacionada

- [Gestión del proyecto mediante Kanban](docs/project-management/kanban.md)
- [Seguimiento técnico de Issues](docs/project-management/issue-tracking.md)
- [Registro de cambios y avances](CHANGELOG.md)

El estado de cada actividad debe mantenerse actualizado según los avances reales del proyecto. Las funciones todavía no implementadas no deben considerarse finalizadas únicamente porque su documentación esté completa.

## 8. Documentación del proyecto

La documentación técnica se encuentra organizada en la carpeta `docs/`, utilizando una estructura que facilita consultar los diferentes trabajos realizados.

### Requisitos

- [Requisitos funcionales](docs/requirements/functional-requirements.md)
- [Requisitos no funcionales](docs/requirements/non-functional-requirements.md)
- [Historias de usuario](docs/requirements/user-stories.md)

### Diseño UML

- [Diagramas UML](docs/design/uml/)

Se incluyen los diagramas de casos de uso, clases, secuencia, actividades y colaboración.

### Arquitectura

- [Arquitectura general](docs/architecture/overview.md)
- [Organización del frontend y backend](docs/architecture/frontend-backend.md)

### Gestión del proyecto

- [Planificación Kanban](docs/project-management/kanban.md)
- [Seguimiento de Issues](docs/project-management/issue-tracking.md)

### Control de versiones

- [Registro de cambios](CHANGELOG.md)
- [Nota técnica de versión 0.1.0](docs/releases/v0.1.0.md)
- [Historial de commits](https://github.com/reynalizpaulino-jpg/queenblossom/commits)

## 9. Avances principales

Durante el desarrollo académico del proyecto se han trabajado cinco avances importantes:

1. Organización inicial del trabajo mediante GitHub Projects y Kanban.
2. Definición de los requisitos funcionales y no funcionales.
3. Elaboración de historias de usuario.
4. Creación de modelos UML y definición de la arquitectura propuesta.
5. Organización de la documentación y preparación del cierre técnico.

Estos avances se describen en el archivo `CHANGELOG.md`.

## 10. Estado actual del proyecto

Queen Blossom se encuentra en la etapa inicial de análisis, planificación y diseño técnico.

La documentación incluye los requisitos del sistema, las historias de usuario, los modelos UML, la arquitectura propuesta y los documentos de gestión.

La implementación de las funcionalidades, su integración con una base de datos y las pruebas correspondientes deberán verificarse o realizarse durante las siguientes etapas.

Por esta razón, la versión documental 0.1.0 no representa una aplicación completamente funcional.

## 11. Próximos pasos

Las siguientes actividades técnicas estarán orientadas a:

- Configurar la estructura inicial del frontend y backend.
- Diseñar e integrar la base de datos.
- Implementar el catálogo de productos.
- Desarrollar el registro e inicio de sesión.
- Implementar la gestión del carrito de compras.
- Integrar la búsqueda y el resumen del pedido.
- Realizar pruebas funcionales y de seguridad.
- Mantener actualizado el seguimiento mediante Issues y GitHub Projects.

## 12. Nota técnica de versión

La versión documental 0.1.0 reúne los trabajos de análisis y diseño realizados durante Ingeniería de Software I.

Incluye la documentación de requisitos, modelos UML, arquitectura y seguimiento técnico, y establece las actividades pendientes para continuar con la implementación.

Para conocer el contenido detallado de esta versión, consultar:

[Nota técnica de versión 0.1.0](docs/releases/v0.1.0.md)

## 13. Información académica

**Proyecto:** Queen Blossom  
**Asignatura:** Ingeniería de Software I  
**Institución:** Universidad Abierta para Adultos (UAPA)  
**Tipo de proyecto:** Tienda virtual  
**Finalidad:** Académica  

---

**Queen Blossom – Documentación técnica y planificación inicial del sistema.**