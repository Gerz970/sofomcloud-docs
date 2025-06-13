| Campo | Tipo de Dato | Longitud | Clave Primaria | Obligatorio | Descripción |
| --- | --- | --- | --- | --- | --- |
| id_administracion_caracteristica | INT | N/A | Sí | Sí | Identificador único de la administración de características |
| id_concepto | INT | N/A | No | No | Identificador del concepto relacionado (FK) |
| id_caracteristica | INT | N/A | No | No | Identificador de la característica (FK) |
| tipo_tasa | VARCHAR | 2 | No | No | Tipo de tasa asociada (Ej: FI=Fija, VA=Variable) |
| dias_tolerancia | INT | N/A | No | No | Cantidad de días de tolerancia permitidos |
| id_modo_cobro | INT | N/A | No | No | Modo de cobro asociado (FK) |
| id_elemento | INT | N/A | No | No | Elemento de cobro o parámetro asociado (FK) |
| fecha_actualiza | DATETIME | N/A | No | No | Última fecha de modificación del registro |
| id_estatus | INT | N/A | No | No | Estatus del registro (activo/inactivo) |