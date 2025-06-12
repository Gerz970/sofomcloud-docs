| Campo | Tabla | Tipo de dato | Descripción |
| --- | --- | --- | --- |
| id_producto_detalle_catalogo | GENERAL.ProductoDetalleCatalogo | INT (PK, Identity) | Identificador único del catálogo de detalles de producto. |
| id_empresa | GENERAL.ProductoDetalleCatalogo | INT | Empresa a la que pertenece el concepto. |
| clave | GENERAL.ProductoDetalleCatalogo | NVARCHAR(50) | Clave del concepto o código del detalle. |
| descripcion | GENERAL.ProductoDetalleCatalogo | NVARCHAR(50) | Descripción del detalle o parámetro. |
| acumula_cat | GENERAL.ProductoDetalleCatalogo | INT | Indicador de si acumula al CAT (1=Sí, 0=No). |
| id_cuenta | GENERAL.ProductoDetalleCatalogo | INT | Identificador de cuenta contable. |
| cuenta | GENERAL.ProductoDetalleCatalogo | NVARCHAR(50) | Nombre o número de la cuenta contable. |
| id_estatus | GENERAL.ProductoDetalleCatalogo | INT | Estatus del detalle. |
| id_usuario_actualiza | GENERAL.ProductoDetalleCatalogo | INT | ID del usuario que realizó la última modificación. |
| fecha_actualiza | GENERAL.ProductoDetalleCatalogo | DATETIME | Fecha de la última modificación. |
| tipo_concepto | GENERAL.ProductoDetalleCatalogo | INT | Tipo de concepto (gasto, comisión, seguro, etc.). |