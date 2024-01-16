# Especificación del diagrama de los casos de uso

## Especificación de los actores del sistema

**Actor**|**Administrador**
|---|---|
Descripción|Gestion del sistema del transporte
Características|
Referencias| CU1, CU2, CU3
Autor|Inna Vdovitsyna
Fecha|11/01/2024
|

**Actor**|**Usuario**
|---|---|
Descripción|Destinatario final del servicio
Características|
Referencias|CU2, CU4, CU5, CU6, CU7, Cu8, CU9, CU10
Autor|Inna Vdovitsyna
Fecha|11/01/2024
|


**Actor**|**Sistema ext posic.**
|---|---|
Descripción|Sistema exterior de geoposicionamiento
Características|
Referencias| CU6
Autor|Inna Vdovitsyna
Fecha|11/01/2024

## Especificación de los casos de uso


|**Caso de Uso CU1**|**Definir medio de transporte**|
|---|---|
Fuentes|Diagrama de los casos del uso
|Actor|Administrador|
|Descripción|El administrador define medio del transporte para cliente|
|Flujo básico|Entrar en el sistema, buscar medio de transporte disponible, elegir transporte para la ruta del cliente|
|Pre-condiciones|Medio de transporte esta registrado en el sistema y esta disponible|
|Post-condiciones|Se fija el medio del transporte |del medio del transporte
|Autor|Inna Vdovitsyna|
|Fecha|11/01/2024|

**Caso de Uso CU2**|**Definir precio transporte**
---|---
Fuentes|Diagrama de los casos del uso
Actor|Administrador
Descripción|Definicion del precio final para cliente de la cierta ruta y cierto medio del transporte
Flujo básico|Calcular el precio para ruta y transporte concretos con respeto del medio transporte y el destino
Pre-condiciones|Destino y medio del transporte seleccionados por usuario y administrador
Post-condiciones|Mostrar precio final
Autor|Inna Vdovitsyna
Fecha|11/01/2024
|

**Caso de Uso CU3**|**Alta y baja de usuarios**
--|--
Fuentes|Diagrama de los casos del uso
Actor|Administrador, Usuario
Descripción|Crear y borrar usuarios en el sistema
Flujo básico|Elegir nombre del usuario, crear contraseña, registrar usuario en el sistema/Elegir usuario y borrar su cuenta del sistema
Pre-condiciones|Cumplir con los requisitos necessarios para registrarse en el sistema/Existencia del usuario en el sistema
Post-condiciones|Se crea usuario/Se borra la cuenta del usuario
Autor|Inna Vdovitsyna
Fecha|11/01/2024
|

**Caso de Uso CU4**|**Login**
---|---
Fuentes|Diagrama de los casos del uso
Actor|Usuario
Descripción|Entrar en el sistema con la cuenta existente
Flujo básico|Introducir el nombre y la contraseña del usuario registrado
Pre-condiciones|Tener cuenta registrada en el sistema
Post-condiciones|Acceder a los servicios del sistema disponibles para usuarios
Autor|Inna Vdovitsyna
Fecha|11/01/2024
|

**Caso de Uso CU5**|**Verificar credenciales**
---|---
Fuentes|Diagrama de los casos del uso
Actor|Usuario
Descripción|Verificacion de los datos del usuarios introducidos en la entrada 
Flujo básico|Comprobar que la cuenta existe y su contaseña es correcta
Pre-condiciones|Disponer de la base de datos de las cuentas y sus contraseñas
Post-condiciones|Autorizacion del usuario en el sistema
Notas|Accion obligatoria (“incluide”)
Autor|Inna Vdovitsyna
Fecha|11/01/2024
|

**Caso de Uso CU6**|**Geoposicionamiento**
---|---
Fuentes|Diagrama de los casos del uso
Actor|Usuario, sistema ext posic.
Descripción|Definir la ubicacion del cliente
Flujo básico|Usuario envia su posicion al sistema del geoposicionamiento, el ultimo proporciona datos de su ubicacion al sistema
Pre-condiciones| Estar autorizado en el sistema
Post-condiciones|Que debe ocurrir con posterioridad
Autor|Inna Vdovitsyna
Fecha|11/01/2024

**Caso de Uso CU7**|**Definir destino**
--|--
Fuentes|Diagrama de los casos del uso
Actor|Usuario
Descripción|El usuario define el destino del viaje
Pre-condiciones|Usuario autorizado elige el destino final
Post-condiciones|Se crea la ruta del viaje
Autor|Inna Vdovitsyna
Fecha|11/01/2024
|

**Caso de Uso CU8**|**Modificar ruta**
--|--
Fuentes|Diagrama de los casos del uso
Actor|Usuario
Descripción|Modificacion del destino intermedio o final
Pre-condiciones|La ruta debe ser ya creada
Post-condiciones|La ruta se modifica con respeto de los cambios realizados por cliente
Autor|Inna Vdovitsyna
Fecha|11/01/2024
|

**Caso de Uso CU9**|**Sugerir destinos interesantes**
--|--
Fuentes|Diagrama de los casos del uso
Actor|Usuario
Descripción|Sugerir destinos interesantes
Flujo básico|Sugerir destinos interesantes en la etapa de la eleccion del destino final por el usuario
Pre-condiciones|Usuario debe estar autorizado y elegiendo el destino final
Post-condiciones|Mostrar la lista de los destinos interesantes 
Notas|Accion opcional (“extend”)
Autor|Inna Vdovitsyna
Fecha|11/01/2024
|

**Caso de Uso CU10**|**Mostrar puntos interés en ruta**
--|--
Fuentes|Diagrama de los casos del uso
Actor|Usuario
Descripción|Mostrar puntos interés en la ruta
Flujo básico|Elegir puntos de interes cerca del ruta estabelecida por usuario
Pre-condiciones|Tener la ruta y destino estabelecidos
Post-condiciones|Mostrar la lista de los los puntos del interes
Notas|Accion opcional (“extend”)
Autor|Inna Vdovitsyna
Fecha|11/01/2024