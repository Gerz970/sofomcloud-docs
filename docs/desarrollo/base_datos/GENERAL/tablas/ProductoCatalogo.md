| Campo | Tabla | Tipo de dato | Descripción |
| --- | --- | --- | --- |
| id_producto_catalogo | GENERAL.ProductoCatalogo | INT (PK, Identity) | Identificador único del catálogo de productos. |
| producto | GENERAL.ProductoCatalogo | NVARCHAR(99) | Nombre o descripción del producto en catálogo. |
| id_estatus | GENERAL.ProductoCatalogo | INT | Estatus del producto (activo, inactivo, etc.). |
| id_usuario_actualiza | GENERAL.ProductoCatalogo | INT | Usuario que realizó la última modificación. |
| fecha_actualiza | GENERAL.ProductoCatalogo | DATETIME | Fecha de la última modificación. |
| id_producto_portal | GENERAL.ProductoCatalogo | INT | Relación con identificador de producto en el portal. |
| clave_bc | GENERAL.ProductoCatalogo | NVARCHAR(5) | Clave de Banco de Crédito o sistema externo. |
| tipo_credito | GENERAL.ProductoCatalogo | NVARCHAR(10) | Tipo de crédito (ej. 'simple', 'revolvente'). |
| clave_cc | GENERAL.ProductoCatalogo | NVARCHAR(5) | Clave de Centro de Costo u otra codificación. |