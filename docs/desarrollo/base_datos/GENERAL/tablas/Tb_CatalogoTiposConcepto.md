| Campo | Tipo de dato | ¿Permite nulos? | Descripción |
| --- | --- | --- | --- |
| id_tipo_concepto | INT (IDENTITY) | NO | Identificador único del tipo de concepto (clave primaria, auto incremental). |
| clave | VARCHAR(10) | SÍ | Clave corta del tipo de concepto. |
| nombre | VARCHAR(50) | SÍ | Nombre descriptivo del tipo de concepto. |
| descripcion | VARCHAR(500) | SÍ | Descripción detallada del tipo de concepto. |
| fecha_actualiza | DATETIME | SÍ | Fecha de la última actualización del registro. |
| id_estatus | INT | SÍ | Referencia al estatus del tipo de concepto (activo/inactivo u otro). |