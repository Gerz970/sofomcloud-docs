| Campo | Tipo de dato | ¿Permite nulos? | Descripción |
| --- | --- | --- | --- |
| id_estatus | INT (IDENTITY) | NO | Identificador único del estatus (clave primaria, auto incremental). |
| clave | NVARCHAR(20) | SÍ | Clave o código del estatus. |
| descripcion | NVARCHAR(50) | SÍ | Descripción corta del estatus (ej. “Activo”, “Inactivo”, “Pendiente”). |
| id_tabla | INT | SÍ | Referencia al identificador de la tabla o módulo que aplica este estatus. |
| id_usuario_actualiza | INT | SÍ | Identificador del usuario que realizó la última modificación. |
| fecha_actualiza | DATETIME | SÍ | Fecha de la última actualización del registro. |