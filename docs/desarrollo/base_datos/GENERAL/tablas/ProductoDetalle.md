| Campo | Tabla | Tipo de dato | Descripción |
| --- | --- | --- | --- |
| id_producto_detalle | GENERAL.ProductoDetalle | INT (PK, Identity) | Identificador único del detalle del producto. |
| id_producto | GENERAL.ProductoDetalle | INT | Relación con el producto principal. |
| id_producto_detalle_catalogo | GENERAL.ProductoDetalle | INT | Catálogo que describe el tipo de detalle. |
| id_tipo_medida_parametro | GENERAL.ProductoDetalle | INT | Tipo de unidad o medida del parámetro. |
| valor | GENERAL.ProductoDetalle | DECIMAL(18,4) | Valor numérico del parámetro. |
| orden | GENERAL.ProductoDetalle | NCHAR(10) | Orden o prioridad del parámetro. |
| es_financiado | GENERAL.ProductoDetalle | BIT | ¿Es financiado este componente? (0=No, 1=Sí). |
| id_estatus | GENERAL.ProductoDetalle | INT | Estatus del detalle. |
| id_usuario_actualiza | GENERAL.ProductoDetalle | INT | Usuario que realizó la última actualización. |
| fecha_actualiza | GENERAL.ProductoDetalle | DATETIME | Fecha de la última actualización. |
| descripcion_seguro | GENERAL.ProductoDetalle | NVARCHAR(100) | Descripción del seguro (si aplica). |
| nombre_aseguradora | GENERAL.ProductoDetalle | NVARCHAR(100) | Nombre de la aseguradora. |
| clausula_seguro | GENERAL.ProductoDetalle | NVARCHAR(100) | Cláusula del seguro. |
| concepto_advertencia | GENERAL.ProductoDetalle | NVARCHAR(100) | Advertencias o conceptos importantes. |
| tipo_seguro | GENERAL.ProductoDetalle | BIT | ¿Es un seguro? (0=No, 1=Sí). |
| calcula_iva | GENERAL.ProductoDetalle | BIT DEFAULT (0) | ¿Se calcula IVA para este componente? |
| permite_financiar | GENERAL.ProductoDetalle | BIT DEFAULT (0) | ¿Se permite financiar este componente? |
| prorrateado | GENERAL.ProductoDetalle | INT | ¿Está prorrateado? |
| interes_moratorio | GENERAL.ProductoDetalle | INT | Tipo o categoría de interés moratorio. |
| id_tasa_variable | GENERAL.ProductoDetalle | INT | Identificador de tasa variable. |
| spread | GENERAL.ProductoDetalle | DECIMAL(18,4) | Margen o spread adicional aplicado a la tasa. |
| aforo | GENERAL.ProductoDetalle | DECIMAL(18,2) | Porcentaje de aforo. |
| honorarios | GENERAL.ProductoDetalle | DECIMAL(18,2) | Monto de honorarios. |
| pago_anticipado | GENERAL.ProductoDetalle | BIT | ¿Tipo A o tipo B? (0 = A , 1 = B). |