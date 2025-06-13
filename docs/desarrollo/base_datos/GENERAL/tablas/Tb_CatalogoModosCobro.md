| Campo | Tipo de dato | ¿Permite nulos? | Descripción |
| --- | --- | --- | --- |
| id_modo_cobro | INT (IDENTITY) | NO | Identificador único del modo de cobro (clave primaria, auto incremental). |
| clave | VARCHAR(10) | SÍ | Clave corta del modo de cobro. |
| nombre | VARCHAR(50) | SÍ | Nombre del modo de cobro. |
| descripcion | VARCHAR(500) | SÍ | Descripción detallada del modo de cobro. |
| fecha_actualiza | DATETIME | SÍ | Fecha de la última modificación o actualización. |
| id_estatus | INT | SÍ | Referencia al estatus del modo de cobro (activo/inactivo u otro). |