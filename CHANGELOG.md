# Registro de cambios – Queen Blossom

Este documento reúne los avances y ajustes realizados durante la planificación y documentación del sistema digital Queen Blossom, desarrollado en la asignatura Ingeniería de Software I de la Universidad Abierta para Adultos (UAPA).

El objetivo es mantener un registro organizado de la evolución del proyecto y facilitar el seguimiento de los cambios realizados.

## [0.1.0] – Cierre documental de la Semana VIII

**Fecha:** 13 de octubre de 2026

**Estado:** Documentación y diseño técnico inicial.

### 1. Organización y planificación del proyecto

Se organizó el desarrollo inicial de Queen Blossom utilizando la metodología Kanban mediante GitHub Projects.

Se establecieron las columnas Backlog, Por hacer, En progreso, En revisión y Finalizado, con el propósito de dar seguimiento a las diferentes actividades.

También se identificaron seis tareas iniciales relacionadas con los requisitos, el diseño de la base de datos, el acceso de usuarios, la interfaz, el catálogo y el carrito de compras.

**Evidencia:** `docs/project-management/kanban.md`

### 2. Definición de requisitos y necesidades de los usuarios

Se documentaron cinco requisitos funcionales y cinco requisitos no funcionales para establecer las características principales de Queen Blossom.

También se elaboraron cinco historias de usuario relacionadas con la consulta de productos, el registro, el carrito, la búsqueda y el resumen del pedido.

Estos documentos sirven como referencia para las siguientes etapas del desarrollo.

**Evidencias:**
- `docs/requirements/functional-requirements.md`
- `docs/requirements/non-functional-requirements.md`
- `docs/requirements/user-stories.md`

### 3. Elaboración de modelos UML

Se trabajaron los modelos UML del sistema para representar las principales funcionalidades y la relación entre sus componentes.

Los diagramas incluyen casos de uso, clases, secuencia, actividades y colaboración.

Estos modelos ayudan a comprender el funcionamiento previsto de Queen Blossom antes de comenzar su implementación.

**Evidencia:** `docs/design/uml/`

### 4. Definición de la arquitectura del sistema

Se estableció una propuesta de arquitectura cliente-servidor con separación entre frontend, backend y base de datos.

Para el frontend se seleccionó una organización basada en componentes y se propuso React como tecnología de implementación.

Para el backend se seleccionó el patrón MVC, complementado con una capa de servicios. Se propuso Node.js con Express para el desarrollo futuro.

También se definió la comunicación mediante una API HTTP con respuestas JSON.

**Evidencias:**
- `docs/architecture/overview.md`
- `docs/architecture/frontend-backend.md`

### 5. Organización de la documentación y seguimiento técnico

Se preparó una estructura de documentación centralizada en `docs/`, con apartados para requisitos, UML, arquitectura, gestión del proyecto y versiones.

Se documentó el seguimiento de Issues, incluyendo funcionalidades prioritarias, criterios de aceptación y posibles riesgos técnicos.

Además, se preparó la documentación necesaria para el cierre de la versión inicial.

**Evidencias:**
- `README.md`
- `docs/project-management/issue-tracking.md`
- `docs/releases/v0.1.0.md` (una vez completado)

## Estado de la versión

La versión 0.1.0 representa el cierre documental inicial del proyecto.

Las actividades de implementación, integración y pruebas deberán continuar conforme al estado real del repositorio y del tablero de GitHub Projects.

## Historial de Git

Los cambios publicados en el repositorio pueden consultarse en el historial de commits de GitHub:

https://github.com/reynalizpaulino-jpg/queenblossom/commits

**Observación:** Los avances descritos corresponden al trabajo académico y a la documentación preparada. Las fechas individuales y los commits asociados deben comprobarse directamente en GitHub. Este registro no implica que todas las funcionalidades estén implementadas.

## Próxima versión

La siguiente etapa estará orientada a comenzar la implementación de los módulos principales y realizar las primeras pruebas de funcionamiento del sistema.