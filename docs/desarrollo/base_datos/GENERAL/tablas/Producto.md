| Campo | Tabla | Tipo de dato | Descripción |
| --- | --- | --- | --- |
| id_producto | GENERAL.Producto | INT (PK, Identity) | Identificador único del producto. |
| id_producto_catalogo | GENERAL.Producto | INT | Identificador del catálogo del producto. |
| producto | GENERAL.Producto | NVARCHAR(50) | Nombre o descripción del producto. |
| id_empresa |  | INT | ID de la empresa propietaria del producto. |
| id_linea_fondeo | GENERAL.Producto | INT | Identificador de la línea de fondeo asociada. |
| reca | GENERAL.Producto | NVARCHAR(300) | Descripción de RECA asociada al producto. |
| tasa_anual | GENERAL.Producto | DECIMAL(18) | Tasa anual aplicable al producto. |
| fact_seguro | GENERAL.Producto | DECIMAL(18) | Factor de seguro aplicado. |
| comision | GENERAL.Producto | DECIMAL(18) | Comisión por contratación del producto. |
| cat | GENERAL.Producto | DECIMAL(18) | Costo Anual Total del producto. |
| garantia_liquida | GENERAL.Producto | DECIMAL(18) | Porcentaje de garantía líquida requerida. |
| tasa_fija | GENERAL.Producto | DECIMAL(18) | Tasa fija del producto. |
| causa_moratorios | GENERAL.Producto | INT | Identificador de causa de interés moratorio. |
| moratorios | GENERAL.Producto | DECIMAL(18) | Porcentaje de interés moratorio. |
| causa_gastos_cobranza | GENERAL.Producto | INT | Identificador de causa de gastos de cobranza. |
| gastos_cobranza | GENERAL.Producto | DECIMAL(18) | Monto de gastos de cobranza. |
| iva | GENERAL.Producto | DECIMAL(18) | Porcentaje de IVA aplicado. |
| id_estatus | GENERAL.Producto | INT | Estatus del producto. |
| id_usuario_actualiza | GENERAL.Producto | INT | Usuario que realizó la última actualización. |
| fecha_actualiza | GENERAL.Producto | DATETIME | Fecha de la última actualización. |
| tipo_pago_anticipado | GENERAL.Producto | INT | Tipo de pago anticipado permitido. |
| id_moneda | GENERAL.Producto | INT | Identificador de la moneda utilizada. |
| id_instrumento_monetario | GENERAL.Producto | INT | Instrumento monetario asociado. |
| id_regimen_fiscal | GENERAL.Producto | INT | Identificador del régimen fiscal. |
| id_nacionalidad | GENERAL.Producto | INT | Nacionalidad del producto o cliente. |
| seguro | GENERAL.Producto | BIT | Indica si el producto incluye seguro (0=No, 1=Sí). |
| descripcion_seguro | GENERAL.Producto | VARCHAR(300) | Descripción del seguro del producto. |
| aseguradora | GENERAL.Producto | VARCHAR(300) | Nombre de la aseguradora. |
| clausula_seguro | GENERAL.Producto | VARCHAR(300) | Cláusula específica del seguro. |
| advertencia_seguro | GENERAL.Producto | VARCHAR(300) | Advertencias del seguro asociado. |
| estado_cuenta | GENERAL.Producto | INT | Tipo de estado de cuenta. |
| id_tipo_aplicacion_pago | GENERAL.Producto | INT | Tipo de aplicación de pagos. |
| factoraje | GENERAL.Producto | BIT | ¿El producto permite factoraje? (0=No, 1=Sí). |
| tasa_variable | GENERAL.Producto | BIT | ¿La tasa es variable? (0=No, 1=Sí). |
| id_regimen_fiscal_cedente | GENERAL.Producto | INT | Régimen fiscal del cedente. |
| arrendamientop | GENERAL.Producto | BIT | ¿Producto de arrendamiento puro? |
| arrendamientof | GENERAL.Producto | BIT | ¿Producto de arrendamiento financiero? |
| id_producto_condusef | GENERAL.Producto | INT | Clave de producto ante CONDUSEF. |
| id_tipo_moratorio | GENERAL.Producto | INT | Tipo de interés moratorio. |
| automotriz | GENERAL.Producto | BIT | ¿Es un producto automotriz? (0=No, 1=Sí). |