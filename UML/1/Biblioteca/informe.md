# Casos de uso de una biblioteca
<img src="biblioteca.png">

## Especificacion de los actores

**Actor**| **Administrador**
---|---|
Descripción|Gestion de la biblioteca
Relaciones|Usuario (Buscar libro)
Referencias|Autorizacion, modificacion del catalago, buscar libro, crear ususario
Autor|Inna Vdovitsyna
Fecha|23/01/24

**Actor**| **Usuario**
---|---|
Descripción|Gestion de la biblioteca
Relaciones|Usuario (Buscar libro)
Referencias|Buscar libro, Prestar libro, Volver libro
Autor|Inna Vdovitsyna
Fecha|23/01/24

## Especificacion de los casos de uso

**Caso de Uso CU**|**Autorizacion**
---|----
Fuentes|Diagrama de los casos de uso
Actor|Bibliotecario
Descripción|Autorizarse en el sistema de biblioteca para gestionar el trabajo de la biblioteca
Flujo básico|Abrir el sistema, introducir el nombre y contraseña
Pre-condiciones|Existir la cuenta del administrador
Post-condiciones|Las acciones del administrador deberian estar disponibles
Autor|Inna Vdovitsyna
Fecha|23/01/24

**Caso de Uso CU**|**Verificar credenciales**
---|---
Fuentes|Diagrama de los casos de uso
Actor|Bibliotecario
Descripción|Verificar los datos  introducidos por usuario
Flujo básico|Buscar la cuenta, verificar el nombre, comprobar la contraseña de la cuenta
Pre-condiciones|Existir la cuenta del administrador
Post-condiciones|Las acciones del administrador deberian estar disponibles
Notas| accion obligatorio (include)
Autor|Inna Vdovitsyna
Fecha|23/01/24

**Caso de Uso CU**|**Modificar catalogo de los libros**
--|--
Fuentes|Diagrama de los casos de uso
Actor|Bibliotecario
Descripción|Verificar los datos  introducidos por usuario
Flujo básico|Autorizarse en el sistema, añadir o borrar los libros del catalogo
Pre-condiciones|El catalogo de los libros debe estar creado
Post-condiciones|Catalogo de libros disponibles modificado
Autor|Inna Vdovitsyna
Fecha|23/01/24

**Caso de Uso CU**|**Prestar libro**
--|--
Fuentes|Diagrama de los casos de uso
Actor|Usuario
Descripción|Prestar libro disponible del catalogo
Flujo básico|Buscar un libro en catalogo, comprobar que libro esta disponible, prestar el libro
Pre-condiciones|Libro debe ser disponible
Post-condiciones|Libro y el usuario se associan 
Autor|Inna Vdovitsyna
Fecha|23/01/24

**Caso de Uso CU**|**Buscar libro**
--|--
Fuentes|Diagrama de los casos de  uso
Actor|Usuario, Bibliotecario
Descripción|Buscar en el catalogo y comprobar su estado
Flujo básico|Buscar libro en catalago, comprobar, si libro esta disponible
Pre-condiciones|Libro debe estar registrado en el catalogo
Post-condiciones|
Autor|Inna Vdovitsyna
Fecha|23/01/24

**Caso de Uso CU**|**Recomendar libro**
--|--
Fuentes|Diagrama de los casos de  uso
Actor|Usuario, Bibliotecario
Descripción|Proponer lista de recomendaciones
Flujo básico|Buscar libros del mismo autor/del mismo genero/etc, formar la lista de recomendaciones, mostrar la lista al usuario
Pre-condiciones|Los libros en catalogo deben estar asociados entre si mismos
Post-condiciones|Formacion de la lista de recomendaciones
Nota|accion opcional (extend)
Autor|Inna Vdovitsyna
Fecha|23/01/24

**Caso de Uso CU**|**Volver libro**
--|--
Fuentes|Diagrama de los casos de  uso
Actor|Usuario
Descripción|Volver libro prestado por usuario
Flujo básico|Encontrar el libro en la lista de libros prestados por usuario, eliminar el libro de esta lista
Pre-condiciones|El libro debe estar prestado por el mismo usuario que lo vuelve
Post-condiciones|El libro desaparece de la lista de libros prestados
Autor|Inna Vdovitsyna
Fecha|23/01/24
