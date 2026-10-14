# Organización del frontend y backend – Queen Blossom

## 1. Introducción

Para desarrollar Queen Blossom de manera organizada se propone separar la aplicación en dos partes principales: frontend y backend.

El frontend estará encargado de las pantallas y de la interacción con los usuarios, mientras que el backend procesará las solicitudes, aplicará las reglas del negocio y administrará la información almacenada.

Esta separación ayudará a distribuir mejor las responsabilidades del sistema y facilitará su mantenimiento durante las siguientes etapas de desarrollo.

## 2. Organización del frontend

El frontend utilizará una arquitectura basada en componentes, tomando React como tecnología propuesta para su futura implementación.

Esta organización permitirá construir las diferentes pantallas de la tienda a partir de elementos reutilizables, evitando tener que desarrollar varias veces las mismas funciones visuales.

### 2.1. Estructura de carpetas propuesta

```text
frontend/
└── src/
    ├── pages/
    │   ├── Home.jsx
    │   ├── Products.jsx
    │   ├── Login.jsx
    │   ├── Register.jsx
    │   └── Cart.jsx
    ├── components/
    │   ├── Navbar.jsx
    │   ├── ProductCard.jsx
    │   ├── ProductList.jsx
    │   └── CartItem.jsx
    ├── services/
    │   ├── api.js
    │   ├── authService.js
    │   ├── productService.js
    │   └── cartService.js
    ├── assets/
    ├── App.jsx
    └── main.jsx
```

### 2.2. Responsabilidades principales

**Pages (Páginas):**

Contendrá las pantallas principales que podrán visitar los clientes, como el catálogo, el formulario de acceso y el carrito de compras.

**Components (Componentes):**

Contendrá elementos visuales reutilizables, como la barra de navegación, las tarjetas de productos y los elementos del carrito.

**Services (Servicios):**

Se encargará de enviar solicitudes HTTP al backend y recibir las respuestas de la API.

**Assets (Recursos):**

Guardará los recursos estáticos necesarios para la interfaz, como imágenes, íconos y estilos.

### 2.3. Funcionamiento del frontend

Cuando un cliente visite Queen Blossom, el frontend mostrará las páginas y los productos disponibles.

Si el usuario realiza una búsqueda, inicia sesión o modifica su carrito, la aplicación enviará una solicitud al backend mediante el servicio correspondiente.

Una vez recibida la respuesta, la interfaz mostrará los resultados de la operación.

## 3. Organización del backend

El backend utilizará una arquitectura MVC (Modelo-Vista-Controlador), complementada con una capa de servicios para separar las reglas del negocio de los controladores.

Esta arquitectura permitirá mantener el procesamiento de las operaciones organizado y facilitar la incorporación de nuevas funcionalidades.

Para la implementación futura se propone utilizar Node.js con Express, aunque la tecnología definitiva podrá seleccionarse al iniciar la programación.

### 3.1. Estructura de carpetas propuesta

```text
backend/
└── src/
    ├── models/
    │   ├── User.js
    │   ├── Product.js
    │   ├── Cart.js
    │   ├── CartItem.js
    │   └── Order.js
    ├── controllers/
    │   ├── AuthController.js
    │   ├── ProductController.js
    │   ├── CartController.js
    │   └── OrderController.js
    ├── services/
    │   ├── AuthService.js
    │   ├── ProductService.js
    │   ├── CartService.js
    │   └── OrderService.js
    ├── routes/
    │   ├── authRoutes.js
    │   ├── productRoutes.js
    │   ├── cartRoutes.js
    │   └── orderRoutes.js
    ├── middlewares/
    │   └── authMiddleware.js
    ├── config/
    │   └── database.js
    └── app.js
```

### 3.2. Responsabilidades principales

**Models (Modelos):**

Representarán las entidades principales de Queen Blossom y facilitarán el acceso a los datos almacenados.

**Controllers (Controladores):**

Recibirán las solicitudes realizadas desde el frontend, verificarán la información enviada y coordinarán la ejecución de las operaciones.

**Services (Servicios):**

Contendrán las reglas del negocio. Por ejemplo, calcular el total de un carrito, validar cantidades y preparar los datos de un pedido.

**Routes (Rutas):**

Definirán las direcciones de la API y establecerán qué controlador atenderá cada solicitud.

**Middlewares:**

Permitirán realizar verificaciones antes de procesar determinadas solicitudes, como comprobar la autenticación de un usuario.

**Config (Configuración):**

Contendrá los elementos necesarios para configurar el funcionamiento del backend y su conexión con la base de datos.

### 3.3. Representación de la vista en MVC

Debido a que Queen Blossom tendrá un frontend independiente, el backend no estará encargado de generar directamente las páginas visuales.

En esta propuesta, la representación de los resultados se realizará mediante respuestas JSON de la API. El frontend recibirá esos datos y los presentará mediante sus componentes.

De esta manera, se utilizará una adaptación del patrón MVC para una aplicación web con frontend y backend separados.

## 4. Comunicación entre frontend y backend

El frontend y el backend se comunicarán mediante una API HTTP que utilizará JSON para intercambiar información.

Las solicitudes llegarán a las rutas correspondientes del backend y serán procesadas por sus controladores y servicios.

### 4.1. Ejemplos de endpoints propuestos

| Método | Endpoint | Función |
|---|---|---|
| GET | /api/products | Consultar el catálogo de productos. |
| GET | /api/products/:id | Consultar un producto específico. |
| GET | /api/products?search= | Buscar productos. |
| POST | /api/auth/register | Registrar un usuario. |
| POST | /api/auth/login | Iniciar sesión. |
| GET | /api/cart | Consultar el carrito del usuario. |
| POST | /api/cart/items | Agregar productos al carrito. |
| PATCH | /api/cart/items/:id | Modificar cantidades. |
| DELETE | /api/cart/items/:id | Eliminar productos del carrito. |
| GET | /api/orders/preview | Consultar el resumen previo del pedido. |

Los endpoints anteriores son una propuesta de diseño. Todavía no representan funcionalidades implementadas ni probadas.

## 5. Ejemplo de funcionamiento: agregar un producto al carrito

Para explicar cómo se comunicarían ambas partes del sistema, se utiliza como ejemplo la función de agregar productos al carrito.

**Paso 1. Selección del producto**

El cliente consulta el catálogo de Queen Blossom y selecciona un artículo que desea comprar.

**Paso 2. Solicitud desde el frontend**

El componente correspondiente utiliza `cartService.js` para enviar una solicitud HTTP al backend.

**Paso 3. Recepción de la solicitud**

La ruta `/api/cart/items` recibe la solicitud y la dirige hacia `CartController`.

**Paso 4. Procesamiento**

El controlador utiliza `CartService` para verificar los datos del artículo, validar la cantidad solicitada y calcular los cambios necesarios.

**Paso 5. Acceso a los datos**

El backend consulta o actualiza la información del carrito utilizando los modelos y la conexión con la base de datos.

**Paso 6. Respuesta del backend**

El servidor devuelve una respuesta JSON con el resultado de la operación y los datos actualizados del carrito.

**Paso 7. Actualización de la interfaz**

El frontend recibe la información y actualiza la cantidad de artículos y el total de la compra que se muestra al cliente.

Este proceso corresponde principalmente al requisito RF-03 y a la historia de usuario HU-03.

## 6. Ejemplo de comunicación mediante JSON

### Solicitud para agregar un producto

**POST /api/cart/items**

```json
{
  "productId": 15,
  "quantity": 2
}
```

### Respuesta esperada

```json
{
  "success": true,
  "message": "Producto agregado al carrito",
  "cart": {
    "items": [
      {
        "productId": 15,
        "quantity": 2,
        "unitPrice": 500,
        "subtotal": 1000
      }
    ],
    "total": 1000
  }
}
```

Este ejemplo es ilustrativo y no corresponde a una respuesta obtenida de un sistema en funcionamiento.

## 7. Responsabilidad de la base de datos

La base de datos almacenará la información de los usuarios, productos, carritos y pedidos.

Solo el backend tendrá acceso directo a la base de datos. El frontend deberá realizar sus operaciones mediante la API.

Esto permitirá centralizar las validaciones y evitar que la aplicación cliente pueda modificar directamente la información almacenada.

Las entidades principales se relacionarán con las clases identificadas durante el modelado UML:

- Usuario
- Producto
- Carrito
- ItemCarrito
- Pedido

## 8. Consideraciones de seguridad

Para proteger la información de los usuarios se deberán aplicar diferentes medidas durante la implementación.

Entre ellas se encuentran la validación de los datos recibidos, el almacenamiento seguro de las contraseñas mediante algoritmos de hash adecuados y la verificación de identidad en las operaciones que requieran autenticación.

También se deberán controlar los permisos de acceso y evitar que un usuario consulte o modifique el carrito de otra persona.

Las credenciales y los datos sensibles no deberán incluirse directamente en el código ni publicarse en el repositorio.

## 9. Relación con los requisitos del proyecto

| Requisito | Frontend | Backend |
|---|---|---|
| RF-01 | Mostrar catálogo | Consultar productos |
| RF-02 | Formularios de acceso | Validar credenciales |
| RF-03 | Mostrar carrito | Gestionar artículos y totales |
| RF-04 | Mostrar filtros | Procesar búsquedas |
| RF-05 | Mostrar resumen | Preparar datos del pedido |

Esta distribución permitirá que cada parte del sistema tenga responsabilidades definidas.

## 10. Estado actual y próximos pasos

La arquitectura descrita constituye una propuesta para la futura implementación de Queen Blossom.

Durante la asignatura se han trabajado los requisitos, las historias de usuario, los modelos UML y la planificación del proyecto.

La programación de los componentes del frontend y backend, la integración con la base de datos y las pruebas funcionales deberán realizarse o verificarse en las siguientes etapas.

El próximo paso técnico recomendado será implementar inicialmente los módulos de productos y usuarios, para luego continuar con la gestión del carrito y los pedidos.

## 11. Conclusión

La separación entre frontend y backend permitirá que Queen Blossom cuente con una estructura sencilla y organizada.

El frontend basado en componentes facilitará la construcción de las pantallas, mientras que el backend MVC con servicios permitirá distribuir las responsabilidades relacionadas con los datos y las operaciones del sistema.

Esta propuesta servirá como guía para continuar el desarrollo de la tienda virtual y mantener una relación clara entre las funcionalidades, la arquitectura y la documentación del proyecto.