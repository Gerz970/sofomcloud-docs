| Campo | Tipo de dato | ¿Permite nulos? | Descripción |
| --- | --- | --- | --- |
| id_elemento | INT (IDENTITY) | NO | Identificador único del elemento (clave primaria, auto incremental). |
| clave | VARCHAR(10) | SÍ | Clave corta del elemento. |
| nombre | VARCHAR(50) | SÍ | Nombre del elemento. |
| descripcion | VARCHAR(500) | SÍ | Descripción detallada del elemento. |
| fecha_actualiza | DATETIME | SÍ | Fecha de la última modificación o actualización del registro. |
| id_estatus | INT | SÍ | Referencia al estatus del elemento (activo/inactivo u otro). |