
# Proyecto Biblioteca

Este proyecto de práctica consiste en la creación de una web para la gestión de una biblioteca municipal utilizando Django, Bootstrap, jQuery y SQL Lite. Nos permitirá distinguir entre tres tipos de usuario:
- Estándar, usuarios normales que podrán revisar el catálogo de la  biblioteca
- Socios, usuarios estándar que además podrán revisar su histórico de préstamos
- Bibliotecarios, podran modificar, añadir o desactivar datos de la biblioteca, así como dar de alta o baja préstamos a los Socios

## Estructura

Vamos a necesitar tres aplicaciones:
- bases: Para vistas generales, como el inicio, login, logout...
- libros: Modelos de libros, copias y autores
- usuarios: Para gestionar usuarios y préstamos

### Modelos

#### App de libros

- Libro ( título, autor(es), tipo, género, sinopsis, observacion, portada, año, creacion, modificacion, activo? )
- Copia ( ( libro, numero ), condicion, prestada?, creacion, modificacion, activo? )
- Autor ( apellido(s), nombre, retrato, genero, nacimiento, nacionalidad, biografia, creacion, modificacion, activo? )

#### App de Usuarios

- Usuario si quisieramos crear un modelo personalizado
- Préstamo ( fecha de inicio, fecha de devolución, plazo, estado, libro(s), usuario, creacion, modificacion, activo? )

### Vistas

- Inicio: Dashboard con algo de informacion acerca de nuestra biblioteca y con una preview de las novedades (Últimos libros añadidos este mes)

- Catálogo: Catálogo de todos los libros y autores
- Vista detalle de un libro y otra de los autores

- Datatables de todos los modelos para la gestion por los bibliotecarios, con vistas para realizar operaciones CRUD 

- Historial de prestamos y perfil para los usuarios registrados