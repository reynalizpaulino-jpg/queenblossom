# Arquitectura general – Queen Blossom

## 1. Introducción

Para el sistema Queen Blossom se propone una arquitectura cliente-servidor que permita organizar de manera independiente la interfaz del usuario, los procesos internos y el almacenamiento de la información.

El frontend seguirá una arquitectura basada en componentes, mientras que el backend utilizará el patrón Modelo-Vista-Controlador (MVC), incorporando una capa sencilla de servicios para organizar las reglas del negocio.

Esta combinación permitirá mantener una estructura clara y facilitar el desarrollo de las funcionalidades de la tienda virtual.

## 2. Arquitectura del frontend

El frontend estará organizado mediante páginas, componentes reutilizables y servicios encargados de comunicarse con el backend.

### Páginas

Representarán las diferentes pantallas de la tienda, como el inicio, el catálogo, el acceso a la cuenta y el carrito de compras.

### Componentes

Serán elementos reutilizables de la interfaz, como la barra de navegación, las tarjetas de productos y los botones.

### Servicios API

Se encargarán de enviar solicitudes al backend y recibir la información necesaria para presentar los productos, gestionar usuarios y actualizar el carrito.

Para una implementación futura se propone utilizar React, aunque esta elección deberá confirmarse al comenzar la programación.

## 3. Arquitectura MVC del backend

El backend estará organizado mediante el patrón MVC, que permite separar las responsabilidades del sistema.

### Modelo (Model)

Representará los datos y las entidades principales de Queen Blossom, como Usuario, Producto, Carrito y Pedido.

Los modelos servirán para organizar la información y establecer su relación con la base de datos.

### Vista (View)

En esta propuesta, el backend funcionará principalmente como una API, por lo que la representación de los resultados se realizará mediante respuestas JSON.

La presentación visual de esos datos será responsabilidad del frontend.

### Controlador (Controller)

Recibirá las solicitudes enviadas desde el frontend, verificará los datos necesarios y coordinará las operaciones correspondientes.

Por ejemplo, ProductController atenderá las solicitudes relacionadas con los productos y CartController las relacionadas con el carrito.

### Capa de servicios

Como apoyo al patrón MVC, se utilizará una capa de servicios para concentrar las reglas del negocio y evitar que los controladores tengan demasiadas responsabilidades.

Por ejemplo, CartService podrá verificar los productos seleccionados, actualizar cantidades y calcular el total del carrito.

## 4. Base de datos

La base de datos permitirá almacenar la información relacionada con usuarios, productos, carritos y pedidos.

El acceso a estos datos se realizará desde el backend, evitando que el frontend se conecte directamente con la base de datos.

La tecnología específica de almacenamiento se seleccionará en la etapa de implementación.

## 5. Comunicación entre frontend y backend

La comunicación se realizará mediante solicitudes HTTP a una API que devolverá respuestas en formato JSON.

Por ejemplo, cuando un cliente agregue un producto al carrito:

1. El cliente seleccionará un artículo desde el frontend.
2. El frontend enviará una solicitud al backend.
3. El controlador correspondiente recibirá la petición.
4. El servicio verificará la información del producto y aplicará las reglas necesarias.
5. El modelo y la capa de acceso a datos permitirán consultar o guardar la información.
6. El backend devolverá una respuesta JSON.
7. El frontend actualizará la información mostrada en pantalla.

Este proceso permitirá mantener separadas las responsabilidades de cada componente.

## 6. Relación con los requisitos del sistema

La arquitectura propuesta permitirá organizar las funciones definidas anteriormente:

- RF-01: Mostrar el catálogo de productos.
- RF-02: Gestionar el registro e inicio de sesión.
- RF-03: Administrar el carrito de compras.
- RF-04: Buscar y filtrar los productos.
- RF-05: Mostrar el resumen del pedido.

## 7. Estado de la arquitectura

La arquitectura MVC del backend y la organización basada en componentes del frontend forman parte del diseño técnico propuesto para Queen Blossom.

Su implementación, integración y pruebas quedan pendientes para una etapa posterior del desarrollo.

## 8. Conclusión

La combinación de una arquitectura basada en componentes para el frontend y el patrón MVC para el backend permite establecer una estructura sencilla y organizada para Queen Blossom.

Con esta separación será más fácil identificar las responsabilidades de cada parte del sistema, mantener el código organizado y realizar mejoras cuando se incorporen nuevas funcionalidades.