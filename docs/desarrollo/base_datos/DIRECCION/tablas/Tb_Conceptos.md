| Campo | Tipo de Dato | Longitud | Clave Primaria | Obligatorio | Descripción |
| --- | --- | --- | --- | --- | --- |
| id_concepto | INT | N/A | Sí | Sí | Identificador único del concepto |
| nombre | VARCHAR | 50 | No | No | Nombre del concepto |
| descripcion | VARCHAR | 100 | No | No | Descripción breve del concepto |
| id_tipo_concepto | INT | N/A | No | No | Tipo de concepto (FK) |
| id_categoria | INT | N/A | No | No | Categoría del concepto (FK) |
| id_forma_pago | INT | N/A | No | No | Forma de pago asociada (FK) |
| id_modelo | INT | N/A | No | No | Modelo financiero relacionado (FK) |
| plazo | INT | N/A | No | No | Plazo asociado al concepto (en días o meses) |
| requerido | INT | N/A | No | No | Indica si el concepto es requerido (1=Sí, 0=No) |
| id_tipo_medida | INT | N/A | No | No | Unidad de medida asociada (FK) |
| iva | INT | N/A | No | No | Indica si el concepto aplica IVA (1=Sí, 0=No) |
| fecha_actualiza | DATETIME | N/A | No | No | Fecha de última actualización |
| id_usuario_actualiza | INT | N/A | No | No | Usuario que realizó la última actualización |
| id_estatus | INT | N/A | No | No | Estatus actual del concepto (FK o catálogo) |