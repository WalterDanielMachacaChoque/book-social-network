# Book Social Network

## Tabla de contenido

- [Descripción general](#overview)
- [Características](#features)
- [Tecnologías utilizadas](#technologies-used)
    - [Backend (book-social-network)](#backend-book-social-network)
    - [Frontend (book-social-network-ui)](#frontend-book-social-network-ui)
- [Instalacion](#Instalation)
- [Vista Previa](#Preview)

## Descripción general

Book Social Network es una aplicación completa que permite a los usuarios administrar sus colecciones de libros e interactuar con una comunidad de entusiastas de los libros. Ofrece funciones como registro de usuarios, validación segura de correo electrónico, gestión de libros (incluida la creación, actualización, uso compartido y archivo), préstamo de libros con verificación de disponibilidad, funcionalidad de devolución de libros y aprobación de devoluciones de libros. La aplicación garantiza la seguridad mediante tokens JWT y cumple con las mejores prácticas en el diseño de API REST. El backend está construido con Spring Boot 3 y Spring Security 6, mientras que el frontend se desarrolla usando Angular con Bootstrap para diseñar.

## Características

- Registro de usuario: los usuarios pueden registrarse para obtener una nueva cuenta.
- Validación de correo electrónico: las cuentas se activan mediante códigos seguros de validación de correo electrónico.
- Autenticación de usuario: los usuarios existentes pueden iniciar sesión en sus cuentas de forma segura.
- Gestión de libros: los usuarios pueden crear, actualizar, compartir y archivar sus libros.
- Préstamo de libros: implementa las comprobaciones necesarias para determinar si un libro se puede prestar.
- Devolución de libros: los usuarios pueden devolver libros prestados.
- Aprobación de devolución de libros: Funcionalidad para aprobar devoluciones de libros.

## Tecnologías utilizadas

### Backend (book-network)

- Spring Boot 3
- Spring Security 6
- JWT Token Authentication
- Spring Data JPA
- JSR-303 and Spring Validation
- OpenAPI and Swagger UI Documentation
- Docker
- GitHub Actions

### Frontend (book-network-ui)

- Angular
- Component-Based Architecture
- Lazy Loading
- Authentication Guard
- OpenAPI Generator for Angular
- Bootstrap

## Instalacion

Para comenzar con el proyecto Book Social Network, siga las instrucciones de configuración en los directorios respectivos:

Para configurar el backend del proyecto book-social-network, siga estos pasos:

1. Clone the repository:

```bash
   git clone https://github.com/WalterDanielMachacaChoque/book-social-network
```

2. Ejecute el archivo docker-compose:

```bash
  docker-compose up -d
```

3. Navegue hasta el directorio de book-social-network:

```bash
  cd book-social-network
```

4. Instalar dependencias (suponiendo que Maven esté instalado):

```bash
  mvn clean install
```

4. Ejecute la aplicación pero primero reemplace `x.x.x` con la versión actual del archivo `pom.xml`

```bash
  java -jar target/book-network-api-x.x.x.jar
```

5. Acceda a la documentación de la API utilizando Swagger UI:

Abra un navegador web y vaya a `http://localhost:8088/swagger-ui/index.html.


##Servidor de desarrollo (Angular)

Ejecute `ngserve` para un servidor de desarrollo. Navegue hasta `http://localhost:4200/login`. La aplicación se recargará automáticamente si cambia alguno de los archivos fuente.


## Build

Ejecute `ng build` para construir el proyecto. Los artefactos de compilación se almacenarán en el directorio `dist/`.

## Vista Previa:

### Login (Auth0 (OAuth2))

![My Image](https://i.postimg.cc/kMVF2Vnn/login.jpg)

### Home:

![My Image](https://i.postimg.cc/7Z4gtmS6/libros-home-dan.jpg)


### My books (Muestra los libros del usuario):

![My Image](https://i.postimg.cc/7LYSw-hsr/mis-libros-dan.jpg)

### My Returned Books (Libros que presto el usuario, mas calificacion):

![My Image](https://i.postimg.cc/J4VJtP6q/mi-retorno-libros-dan.jpg)

### My Borrowed Books (Libros que se presto de otro usuario):

![My Image](https://i.postimg.cc/Kz3k8Mtw/my-borrowed-books-dan.jpg)

### Manage my Books (Agregando nuevos libros a mi lista):

![My Image](https://i.postimg.cc/Mpsv0DDg/agregando-nuevo-libro.jpg)

### My Books List (Lista de libros actualizada con exito):

![My Image](https://i.postimg.cc/DwWKDPh9/my-books-actual-dan.jpg)


## Recomendaciones:

- El puerto elegido para el Backend es el "8088", usted puede elegir el que mas le guste.
- Recuerde cambiar las configuraciones de la conexion a la base de datos en los archivos ".yml".
- Cuando inicie el servidor angular y parece no funcionar, pruebe con el siguiente endpoint: `http://localhost:4200/login`.
