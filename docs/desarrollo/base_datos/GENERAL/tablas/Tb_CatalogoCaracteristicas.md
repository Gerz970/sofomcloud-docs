| Campo | Tipo de dato | ¿Permite nulos? | Descripción |
| --- | --- | --- | --- |
| id_caracteristica | INT (IDENTITY) | NO | Identificador único de la característica (clave primaria, auto incremental). |
| clave | VARCHAR(10) | SÍ | Clave corta de la característica. |
| nombre | VARCHAR(50) | SÍ | Nombre o título de la característica. |
| descripcion | VARCHAR(500) | SÍ | Descripción detallada de la característica. |
| dias_tolerancia | INT | SÍ | Días de tolerancia asociados a la característica (si aplica). |
| fecha_actualiza | DATETIME | SÍ | Fecha de la última actualización o modificación. |
| id_estatus | INT | SÍ | Referencia al estatus actual de la característica (activo/inactivo u otro). |