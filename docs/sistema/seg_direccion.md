## CATÁLOGO DE PRODUCTOS
### DESCRIPCIÓN GENERAL
---
El sistema automatizado SOFOMCloud posee una estructura modular, esto implica la distribución del TODO en una red de módulos interdependientes y de manera consecuente, la interacción entre cada uno de módulos referidos.

![[SOFOMCloud.png]]

Dentro de las estructuras particulares descritas, tenemos el Módulo de Dirección, donde el Usuario puede desplegar una determinada sección que le permitirá crear nuevos registros, llamados Productos, y editar registros existentes, que contendrán una configuración particular, con la que se podrá construir una tentativa operación de Crédito, cuya esencia se enunciará posteriormente.

![[Módulo de Dirección.png]]
![[Catálogo de Productos.png]]

### GENERAL.Producto

| Campo                     | Tabla            | Tipo de dato       | Descripción                                        |
| ------------------------- | ---------------- | ------------------ | -------------------------------------------------- |
| id_producto               | GENERAL.Producto | INT (PK, Identity) | Identificador único del producto.                  |
| id_producto_catalogo      | GENERAL.Producto | INT                | Identificador del catálogo del producto.           |
| producto                  | GENERAL.Producto | NVARCHAR(50)       | Nombre o descripción del producto.                 |
| id_empresa                | GENERAL.Producto | INT                | ID de la empresa propietaria del producto.         |
| id_linea_fondeo           | GENERAL.Producto | INT                | Identificador de la línea de fondeo asociada.      |
| reca                      | GENERAL.Producto | NVARCHAR(300)      | Descripción de RECA asociada al producto.          |
| tasa_anual                | GENERAL.Producto | DECIMAL(18)        | Tasa anual aplicable al producto.                  |
| fact_seguro               | GENERAL.Producto | DECIMAL(18)        | Factor de seguro aplicado.                         |
| comision                  | GENERAL.Producto | DECIMAL(18)        | Comisión por contratación del producto.            |
| cat                       | GENERAL.Producto | DECIMAL(18)        | Costo Anual Total del producto.                    |
| garantia_liquida          | GENERAL.Producto | DECIMAL(18)        | Porcentaje de garantía líquida requerida.          |
| tasa_fija                 | GENERAL.Producto | DECIMAL(18)        | Tasa fija del producto.                            |
| causa_moratorios          | GENERAL.Producto | INT                | Identificador de causa de interés moratorio.       |
| moratorios                | GENERAL.Producto | DECIMAL(18)        | Porcentaje de interés moratorio.                   |
| causa_gastos_cobranza     | GENERAL.Producto | INT                | Identificador de causa de gastos de cobranza.      |
| gastos_cobranza           | GENERAL.Producto | DECIMAL(18)        | Monto de gastos de cobranza.                       |
| iva                       | GENERAL.Producto | DECIMAL(18)        | Porcentaje de IVA aplicado.                        |
| id_estatus                | GENERAL.Producto | INT                | Estatus del producto.                              |
| id_usuario_actualiza      | GENERAL.Producto | INT                | Usuario que realizó la última actualización.       |
| fecha_actualiza           | GENERAL.Producto | DATETIME           | Fecha de la última actualización.                  |
| tipo_pago_anticipado      | GENERAL.Producto | INT                | Tipo de pago anticipado permitido.                 |
| id_moneda                 | GENERAL.Producto | INT                | Identificador de la moneda utilizada.              |
| id_instrumento_monetario  | GENERAL.Producto | INT                | Instrumento monetario asociado.                    |
| id_regimen_fiscal         | GENERAL.Producto | INT                | Identificador del régimen fiscal.                  |
| id_nacionalidad           | GENERAL.Producto | INT                | Nacionalidad del producto o cliente.               |
| seguro                    | GENERAL.Producto | BIT                | Indica si el producto incluye seguro (0=No, 1=Sí). |
| descripcion_seguro        | GENERAL.Producto | VARCHAR(300)       | Descripción del seguro del producto.               |
| aseguradora               | GENERAL.Producto | VARCHAR(300)       | Nombre de la aseguradora.                          |
| clausula_seguro           | GENERAL.Producto | VARCHAR(300)       | Cláusula específica del seguro.                    |
| advertencia_seguro        | GENERAL.Producto | VARCHAR(300)       | Advertencias del seguro asociado.                  |
| estado_cuenta             | GENERAL.Producto | INT                | Tipo de estado de cuenta.                          |
| id_tipo_aplicacion_pago   | GENERAL.Producto | INT                | Tipo de aplicación de pagos.                       |
| factoraje                 | GENERAL.Producto | BIT                | ¿El producto permite factoraje? (0=No, 1=Sí).      |
| tasa_variable             | GENERAL.Producto | BIT                | ¿La tasa es variable? (0=No, 1=Sí).                |
| id_regimen_fiscal_cedente | GENERAL.Producto | INT                | Régimen fiscal del cedente.                        |
| arrendamientop            | GENERAL.Producto | BIT                | ¿Producto de arrendamiento puro?                   |
| arrendamientof            | GENERAL.Producto | BIT                | ¿Producto de arrendamiento financiero?             |
| id_producto_condusef      | GENERAL.Producto | INT                | Clave de producto ante CONDUSEF.                   |
| id_tipo_moratorio         | GENERAL.Producto | INT                | Tipo de interés moratorio.                         |
| automotriz                | GENERAL.Producto | BIT                | ¿Es un producto automotriz? (0=No, 1=Sí).          |
### GENERAL.ProductoDetalle

| Campo                        | Tabla                   | Tipo de dato       | Descripción                                   |
| ---------------------------- | ----------------------- | ------------------ | --------------------------------------------- |
| id_producto_detalle          | GENERAL.ProductoDetalle | INT (PK, Identity) | Identificador único del detalle del producto. |
| id_producto                  | GENERAL.ProductoDetalle | INT                | Relación con el producto principal.           |
| id_producto_detalle_catalogo | GENERAL.ProductoDetalle | INT                | Catálogo que describe el tipo de detalle.     |
| id_tipo_medida_parametro     | GENERAL.ProductoDetalle | INT                | Tipo de unidad o medida del parámetro.        |
| valor                        | GENERAL.ProductoDetalle | DECIMAL(18,4)      | Valor numérico del parámetro.                 |
| orden                        | GENERAL.ProductoDetalle | NCHAR(10)          | Orden o prioridad del parámetro.              |
| es_financiado                | GENERAL.ProductoDetalle | BIT                | ¿Es financiado este componente? (0=No, 1=Sí). |
| id_estatus                   | GENERAL.ProductoDetalle | INT                | Estatus del detalle.                          |
| id_usuario_actualiza         | GENERAL.ProductoDetalle | INT                | Usuario que realizó la última actualización.  |
| fecha_actualiza              | GENERAL.ProductoDetalle | DATETIME           | Fecha de la última actualización.             |
| descripcion_seguro           | GENERAL.ProductoDetalle | NVARCHAR(100)      | Descripción del seguro (si aplica).           |
| nombre_aseguradora           | GENERAL.ProductoDetalle | NVARCHAR(100)      | Nombre de la aseguradora.                     |
| clausula_seguro              | GENERAL.ProductoDetalle | NVARCHAR(100)      | Cláusula del seguro.                          |
| concepto_advertencia         | GENERAL.ProductoDetalle | NVARCHAR(100)      | Advertencias o conceptos importantes.         |
| tipo_seguro                  | GENERAL.ProductoDetalle | BIT                | ¿Es un seguro? (0=No, 1=Sí).                  |
| calcula_iva                  | GENERAL.ProductoDetalle | BIT DEFAULT (0)    | ¿Se calcula IVA para este componente?         |
| permite_financiar            | GENERAL.ProductoDetalle | BIT DEFAULT (0)    | ¿Se permite financiar este componente?        |
| prorrateado                  | GENERAL.ProductoDetalle | INT                | ¿Está prorrateado?                            |
| interes_moratorio            | GENERAL.ProductoDetalle | INT                | Tipo o categoría de interés moratorio.        |
| id_tasa_variable             | GENERAL.ProductoDetalle | INT                | Identificador de tasa variable.               |
| spread                       | GENERAL.ProductoDetalle | DECIMAL(18,4)      | Margen o spread adicional aplicado a la tasa. |
| aforo                        | GENERAL.ProductoDetalle | DECIMAL(18,2)      | Porcentaje de aforo.                          |
| honorarios                   | GENERAL.ProductoDetalle | DECIMAL(18,2)      | Monto de honorarios.                          |
| pago_anticipado              | GENERAL.ProductoDetalle | BIT                | ¿Se permite pago anticipado? (0=No, 1=Sí).    |

### GENERAL.ProductoCatalogo

| Campo                | Tabla                    | Tipo de dato       | Descripción                                          |
| -------------------- | ------------------------ | ------------------ | ---------------------------------------------------- |
| id_producto_catalogo | GENERAL.ProductoCatalogo | INT (PK, Identity) | Identificador único del catálogo de productos.       |
| producto             | GENERAL.ProductoCatalogo | NVARCHAR(99)       | Nombre o descripción del producto en catálogo.       |
| id_estatus           | GENERAL.ProductoCatalogo | INT                | Estatus del producto (activo, inactivo, etc.).       |
| id_usuario_actualiza | GENERAL.ProductoCatalogo | INT                | Usuario que realizó la última modificación.          |
| fecha_actualiza      | GENERAL.ProductoCatalogo | DATETIME           | Fecha de la última modificación.                     |
| id_producto_portal   | GENERAL.ProductoCatalogo | INT                | Relación con identificador de producto en el portal. |
| clave_bc             | GENERAL.ProductoCatalogo | NVARCHAR(5)        | Clave de Banco de Crédito o sistema externo.         |
| tipo_credito         | GENERAL.ProductoCatalogo | NVARCHAR(10)       | Tipo de crédito (ej. 'simple', 'revolvente').        |
| clave_cc             | GENERAL.ProductoCatalogo | NVARCHAR(5)        | Clave de Centro de Costo u otra codificación.        |

### GENERAL.ProductoDetalleCatalogo

| Campo                        | Tabla                           | Tipo de dato       | Descripción                                               |
| ---------------------------- | ------------------------------- | ------------------ | --------------------------------------------------------- |
| id_producto_detalle_catalogo | GENERAL.ProductoDetalleCatalogo | INT (PK, Identity) | Identificador único del catálogo de detalles de producto. |
| id_empresa                   | GENERAL.ProductoDetalleCatalogo | INT                | Empresa a la que pertenece el concepto.                   |
| clave                        | GENERAL.ProductoDetalleCatalogo | NVARCHAR(50)       | Clave del concepto o código del detalle.                  |
| descripcion                  | GENERAL.ProductoDetalleCatalogo | NVARCHAR(50)       | Descripción del detalle o parámetro.                      |
| acumula_cat                  | GENERAL.ProductoDetalleCatalogo | INT                | Indicador de si acumula al CAT (1=Sí, 0=No).              |
| id_cuenta                    | GENERAL.ProductoDetalleCatalogo | INT                | Identificador de cuenta contable.                         |
| cuenta                       | GENERAL.ProductoDetalleCatalogo | NVARCHAR(50)       | Nombre o número de la cuenta contable.                    |
| id_estatus                   | GENERAL.ProductoDetalleCatalogo | INT                | Estatus del detalle.                                      |
| id_usuario_actualiza         | GENERAL.ProductoDetalleCatalogo | INT                | ID del usuario que realizó la última modificación.        |
| fecha_actualiza              | GENERAL.ProductoDetalleCatalogo | DATETIME           | Fecha de la última modificación.                          |
| tipo_concepto                | GENERAL.ProductoDetalleCatalogo | INT                | Tipo de concepto (gasto, comisión, seguro, etc.).         |
