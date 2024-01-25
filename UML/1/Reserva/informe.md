# Casos de Uso Reserva de vuelos 

<img src="reserva.png">

## Especificacion de los actores

Actor|Usuario (incluye Pasajero y Agente)
--|--
Descripción|Destinario de los servicios del sistema de reserva
Relaciones|Sistema del pago externo
Referencias|Autorizacion, Reservar vuelo, Buscar vuelo, Cancelar vuelo, Check-in, Gestionar reserva, Psagar
Autor|Inna Vdovitsyna
Fecha|23/01/24

Actor|Sistema del pago externo
--|--
Descripción|Realizacion del pago por las reservas
Relaciones|Usuario
Referencias|Pagar
Autor|Inna Vdovitsyna
Fecha|23/01/24


## Especificacion de los casos de uso


**Caso de Uso CU**|**Buscar vuelo**
--|--
Fuentes| Diagrama de los casos de uso
Actor|Usuario (incluye Pasajero y Agente)
Descripción|Búsqueda de vuelos por parte de un pasajero.
**Flujo básico**| 
1 |Pasajero accede al sistema
2 |Selecciona "Buscar Vuelo"
3 |Ingresa criterios de búsqueda
4 |Sistema muestra resultados
5 |Pasajero selecciona vuelo
6 |Sistema muestra detalles del vuelo
**Flujo básico**| 
Pre-condiciones|Pasajero autenticado, sistema tiene información de vuelos.
Post-condiciones|Sistema registra búsqueda del pasajero, muestra resultados al pasajero
Autor|Inna Vdovitsyna
Fecha|23/01/2024


**Caso de Uso CU**|**Reserva**
--|--
Fuentes| Diagrama de los casos de uso
Actor|Usuario (incluye Pasajero y Agente)
Descripción|Reserva de Vuelo
**Flujo básico**|
1|Pasajero accede al sistema
2| Selecciona "Buscar Vuelo"
3| Ingresa criterios de búsqueda
4| Sistema muestra resultados
5| Pasajero selecciona vuelo
6| Sistema muestra detalles del vuelo
7| Pasajero selecciona "Reservar Vuelo"
8| Sistema solicita confirmación
9| Pasajero confirma la reserva
10| Sistema confirma la reserva al pasajero
**Flujo alternativo**|
Pre-condiciones|Pasajero autenticado, sistema tiene información de vuelos
Post-condiciones|Sistema registra la reserva del pasajero, genera un número de reserva
Autor|Inna Vdovitsyna
Fecha|23/01/2024

**Caso de Uso CU**|**Check-in**
--|--
Fuentes| Diagrama de los casos de uso
Actor|Usuario (incluye Pasajero y Agente)
Descripción|Check-in de Vuelo
**Flujo básico**|
1|Pasajero accede al sistema
2|Selecciona "Consultar Reservas"
3|Sistema muestra las reservas del pasajero
4|Pasajero selecciona la reserva para hacer check-in
5|Pasajero confirma el check-in
6|Sistema emite tarjeta de embarque y actualiza el estado del check-in
**Flujo alternativo**|
Pre-condiciones|Pasajero autenticado, pasajero tiene al menos una reserva con check-in disponible
Post-condiciones|Sistema emite tarjeta de embarque, actualiza el estado del check-in
Autor|Inna Vdovitsyna
Fecha|23/01/2024

**Caso de Uso CU**|**Gestionar Reserva**
--|--
Fuentes| Diagrama de los casos de uso
Actor|Usuario (incluye Pasajero y Agente)
Descripción|Gestionar Reserva
**Flujo básico**|
1|Agente de Reservas accede al sistema
2|Selecciona "Gestionar Reservas"
3|Sistema muestra la lista de reservas pendientes
4|Agente selecciona una reserva para gestionar
5|Sistema muestra detalles de la reserva
6|Agente realiza operaciones de gestión (modificar detalles, asignar asientos, etc.)
7|Sistema confirma las modificaciones y actualiza la reserva
**Flujo alternativo**|
Pre-condiciones|Agente de Reservas autenticado, existencia de al menos una reserva pendiente de gestión.
Post-condiciones|Sistema actualiza la reserva según las modificaciones realizadas por el agente
Autor|Inna Vdovitsyna
Fecha|23/01/2024

**Caso de Uso CU**|**Cancelar Reserva**
--|--
Fuentes| Diagrama de los casos de uso
Actor|Usuario (incluye Pasajero y Agente)
Descripción|Cancelar Reserva
**Flujo básico**|
1|Pasajero accede al sistema
2|Selecciona "Consultar Reservas"
3|Sistema muestra las reservas del pasajero
4|Pasajero selecciona la reserva a cancelar
5|Sistema muestra detalles de la reserva
6|Pasajero selecciona "Cancelar Reserva"
7|Sistema cancela la reserva y actualiza el estado
**Flujo alternativo**|
Pre-condiciones|Pasajero autenticado, pasajero tiene al menos una reserva activa
Post-condiciones|Sistema cancela la reserva seleccionada
Autor|Inna Vdovitsyna
Fecha|23/01/2024

**Caso de Uso CU**|**Autorización**
--|--
Fuentes| Diagrama de los casos de uso
Actor|Usuario (incluye Pasajero y Agente)
Descripción|Autorización de Usuario en el Sistema
**Flujo básico**|
1|Usuario intenta acceder a funciones que requieren autorización
2|Sistema verifica la identidad del usuario
3|Usuario proporciona credenciales de inicio de sesión
4|Sistema verifica las credenciales y concede o niega la autorización
**Flujo alternativo**|
Pre-condiciones|Usuario intenta acceder a funciones que requieren autorización, usuario autenticado o dispuesto a iniciar sesión.
Post-condiciones|Usuario autorizado para acceder a las funciones solicitadas
Autor|Inna Vdovitsyna
Fecha|23/01/2024

**Caso de Uso CU**|**Pagar**
--|--
Fuentes| Diagrama de los casos de uso
Actor|Usuario (incluye Pasajero y Agente), Sistema del pago externo, 
Descripción|Proceso de Pago de Reserva
**Flujo básico**|
1|Pasajero confirma la reserva de vuelo
2|Sistema presenta las opciones de pago
3|Pasajero selecciona el método de pago (tarjeta de crédito, PayPal, etc.)
4|Sistema solicita la información de pago al pasajero
5|Pasajero proporciona la información requerida
6|Sistema verifica la validez de la información de pago
7|Sistema genera un recibo de pago y lo presenta al pasajero, pasajero recibe confirmación de la reserva y el pago
**Flujo alternativo**|
Pre-condiciones|Pasajero ha confirmado la reserva, sistema tiene opciones de pago configuradas
Post-condiciones|Reserva marcada como pagada, generación de un recibo de pago
Nota| Accion obligatoria(include)
Autor|Inna Vdovitsyna
Fecha|23/01/2024
