En una base de datos de una empresa de alquiler de vehículos, se tiene la siguiente tabla Alquileres que contiene información sobre los vehículos alquilados y sus conductores.

Normaliza la tabla Alquileres para que cumpla con 1FN, 2FN y 3FN. Identifica las dependencias funcionales y elimina las dependencias parciales y transitivas en cada paso.

| AlquilerID | FechaAlquiler |	ClienteID | ClienteNombre |	Vehiculos             | PrecioVehiculos |
| ---        | ---           | ---        | ---           | ---                   | ---             |
| 101        |	10/03/2023   | 201        |	Carlos        |	"Sedán, SUV"          |	"50, 70"        |
| 102        |	12/03/2023   | 202        |	Laura         | "Convertible, Pickup" |	"80, 65"        |
| 103        |	15/03/2023   | 203        |	Pedro         |	"SUV, Van, Sedán"     |	"70, 60, 50"    |
| 104        |	18/03/2023   | 204        |	Ana           | "Sedán"               |	"50"            |

## Resolución 

Tabla `Vehiculos`

| AlquilerID | Vehiculo |
| --- | --- |
| 101 | "Sedán" |
| 101 | "SUV" |
| 102 | "Convertible" |
| 102 | "Pickup" | 
| 103 | "SUV" | 
| 103 | "Sedán" |
| 103 | "Van" |
| 104 | "Sedán" |

Tabla `Precios`

| Vehiculo | Precio |
| --- | --- |
| "Sedán" | 50 |
| "SUV" | 70 |
| "Convertible" | 80 |
| "Pickup" | 65 |
| "Van" | 60 |


Tabla `Alquileres`

| AlquilerID | ClienteID | FechaAlquiler |
| --- | --- | --- |
| 101 | 201 | 10/03/2023 |
| 102 | 202 | 12/03/2023 |
| 103 | 203 | 15/03/2023 |
| 104 | 204 | 18/03/2023 |

Tabla `Clientes`

| ClienteID | ClienteNombre |
| --- | --- |
| 201 | "Carlos" |
| 202 | "Laura" |
| 203 | "Pedro" |
| 204 | "Ana" |