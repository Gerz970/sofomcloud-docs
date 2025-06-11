| Nombre de Columna | Tipo de Dato | Longitud / Precisión | Permite Nulo | Descripción |
| --- | --- | --- | --- | --- |
| id_producto_documento | INT | — | NO | Clave primaria del documento asociado al producto |
| id_producto | INT | — | SÍ | Identificador del producto asociado |
| id_documento_digitalizado | INT | — | SÍ | Referencia al documento digitalizado |
| forzoso | INT | — | SÍ | Indica si el documento es obligatorio (1 = Sí, 0 = No) |
| valor | DECIMAL | (18,4) | SÍ | Valor asociado al documento, si aplica |
| orden | INT | — | SÍ | Orden de visualización o procesamiento del documento |
| id_estatus | INT | — | SÍ | Estado del documento (activo, inactivo, etc.) |
| id_usuario_actualiza | INT | — | SÍ | Usuario que realizó la última actualización |
| fecha_actualiza | DATETIME | — | SÍ | Fecha de la última actualización del registro |