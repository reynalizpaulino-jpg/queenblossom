# Historias de usuario – Queen Blossom

## 1. Introducción

Las historias de usuario permiten identificar las principales necesidades de las personas que utilizarán Queen Blossom. Estas historias describen de manera sencilla qué función necesita el cliente y para qué la utilizará.

Durante la etapa de análisis del proyecto se definieron cinco historias de usuario relacionadas con las principales funcionalidades de la tienda virtual.

Cada historia está vinculada con un requisito funcional y cuenta con criterios de aceptación que servirán para comprobar su funcionamiento cuando el sistema sea desarrollado.

## 2. Historias de usuario

### HU-01. Visualizar catálogo de productos

**Como** cliente,  
**quiero** visualizar un catálogo con nombre, imagen, precio y descripción de los productos,  
**para** comparar las opciones disponibles.

**Requisito relacionado:** RF-01  
**Prioridad:** Alta

**Criterios de aceptación:**
- El sistema muestra los productos disponibles.
- Cada producto presenta su nombre, imagen, precio y descripción.
- El cliente puede consultar el catálogo de manera sencilla.

### HU-02. Registro e inicio de sesión

**Como** usuario,  
**quiero** registrarme e iniciar sesión,  
**para** acceder de forma segura a mi cuenta dentro de Queen Blossom.

**Requisito relacionado:** RF-02  
**Prioridad:** Alta

**Criterios de aceptación:**
- El usuario puede crear una cuenta completando los campos obligatorios.
- El sistema valida la información ingresada.
- El usuario puede iniciar sesión con credenciales válidas.
- El sistema rechaza los intentos de acceso con datos incorrectos.

### HU-03. Gestionar carrito de compras

**Como** cliente,  
**quiero** agregar, eliminar y cambiar las cantidades de los productos seleccionados,  
**para** organizar mi compra antes de confirmarla.

**Requisito relacionado:** RF-03  
**Prioridad:** Alta

**Criterios de aceptación:**
- El cliente puede agregar productos al carrito.
- Puede eliminar productos que ya no desea comprar.
- Puede modificar las cantidades de los artículos.
- El sistema actualiza correctamente el total del carrito.

### HU-04. Buscar y filtrar productos

**Como** cliente,  
**quiero** buscar y filtrar los productos disponibles,  
**para** encontrar con mayor rapidez los artículos que necesito.

**Requisito relacionado:** RF-04  
**Prioridad:** Media

**Criterios de aceptación:**
- El sistema permite buscar productos mediante palabras clave.
- El cliente puede utilizar los filtros disponibles.
- Los resultados corresponden con la búsqueda o el filtro seleccionado.

### HU-05. Revisar resumen del pedido

**Como** cliente,  
**quiero** revisar un resumen de los productos seleccionados antes de confirmar mi compra,  
**para** comprobar las cantidades y el importe total del pedido.

**Requisito relacionado:** RF-05  
**Prioridad:** Alta

**Criterios de aceptación:**
- El sistema muestra los productos incluidos en el pedido.
- Se visualizan las cantidades seleccionadas.
- Se presenta el importe total.
- El cliente puede revisar la información antes de confirmar.

## 3. Tabla de trazabilidad

| Historia de usuario | Requisito funcional | Prioridad |
|---|---|---|
| HU-01. Visualizar catálogo | RF-01 | Alta |
| HU-02. Registro e inicio de sesión | RF-02 | Alta |
| HU-03. Gestionar carrito | RF-03 | Alta |
| HU-04. Buscar y filtrar productos | RF-04 | Media |
| HU-05. Revisar resumen del pedido | RF-05 | Alta |

## 4. Relación con GitHub Issues

Estas historias de usuario sirven como referencia para las tareas registradas en GitHub Issues.

Cada Issue permite dar seguimiento al trabajo necesario para desarrollar una funcionalidad, identificar tareas pendientes y comprobar el cumplimiento de los criterios de aceptación.

El estado real de cada historia deberá actualizarse de acuerdo con los avances registrados en el repositorio y en el tablero de GitHub Projects.

## 5. Estado actual

Las cinco historias de usuario están definidas como parte de la documentación inicial del sistema Queen Blossom.

Su implementación y cumplimiento deberán verificarse mediante pruebas funcionales durante las siguientes etapas del desarrollo.

## 6. Conclusión

Las historias de usuario permitieron comprender mejor las necesidades de los clientes y establecer las funciones principales que deberá ofrecer Queen Blossom.

Además, facilitan la relación entre los requisitos, los modelos UML y las actividades de seguimiento, proporcionando una base organizada para continuar el desarrollo del sistema.