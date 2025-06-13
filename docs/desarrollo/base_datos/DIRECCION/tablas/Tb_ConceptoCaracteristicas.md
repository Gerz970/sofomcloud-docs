| Campo | Tipo de Dato | Longitud | Clave Primaria | Obligatorio | Descripción |
| --- | --- | --- | --- | --- | --- |
| id_concepto_caracteristica | INT | N/A | Sí | Sí | Identificador único del concepto-característica |
| id_producto_concepto | INT | N/A | No | Sí | ID del concepto del producto asociado (FK) |
| id_caracteristica | INT | N/A | No | Sí | Identificador de la característica aplicada (FK) |
| nombre_caracteristica | NVARCHAR | 50 | No | No | Nombre descriptivo de la característica |
| es_tasa_variable | INT | N/A | No | Sí | Indica si la característica es una tasa variable (1=Sí, 0=No) |
| id_tipo_tasa_variable | INT | N/A | No | No | Tipo de tasa variable (FK) |
| spread | DECIMAL | 18,4 | No | No | Porcentaje adicional al tipo base (spread) |
| id_tipo_valor | INT | N/A | No | No | Tipo de valor asociado (catálogo o FK) |
| valor | DECIMAL | 18,4 | No | No | Valor aplicado para la característica |
| requiere_dias | INT | N/A | No | No | Indica si requiere definir días para aplicar |
| dias_tolerancia | INT | N/A | No | No | Cantidad de días de tolerancia permitidos |
| id_modo_cobro | INT | N/A | No | No | Modo de cobro de la característica (FK) |
| fecha_creacion | DATETIME | N/A | No | No | Fecha en que se creó el registro |
| fecha_actualiza | DATETIME | N/A | No | No | Última fecha de modificación |
| id_estatus | BIT | N/A | No | No | Estatus del registro (activo/inactivo) |