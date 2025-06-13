| Campo | Tipo de dato | ¿Permite nulos? | Descripción |
| --- | --- | --- | --- |
| id_forma_pago | INT (IDENTITY) | NO | Identificador único de la forma de pago (clave primaria, auto incremental). |
| clave | VARCHAR(10) | SÍ | Clave corta de la forma de pago. |
| nombre | VARCHAR(50) | SÍ | Nombre de la forma de pago. |
| descripcion | VARCHAR(500) | SÍ | Descripción detallada de la forma de pago. |
| fecha_actualiza | DATETIME | SÍ | Fecha de la última actualización o modificación. |
| aplica_plazo | INT | SÍ | Indica si aplica un plazo asociado a la forma de pago (booleano o FK). |
| id_estatus | INT | SÍ | Referencia al estatus del registro (activo/inactivo u otro). |