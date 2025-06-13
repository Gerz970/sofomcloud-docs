| Nombre del Campo | Tipo de Dato | Permite Nulo | Llave Primaria | Descripción |
| --- | --- | --- | --- | --- |
| id_factor_riesgo | INT | No | Sí | Identificador único del registro del factor de riesgo del producto |
| id_producto | INT | Sí | No | ID del producto relacionado |
| id_producto_condusef | INT | Sí | No | ID del producto en el catálogo de CONDUSEF |
| id_moneda | INT | Sí | No | Identificador de la moneda del producto |
| id_canal | INT | Sí | No | Canal de distribución del producto (e.g. sucursal, digital) |
| id_instrumento_monetario | INT | Sí | No | Instrumento monetario utilizado en la transacción |
| id_regimen_fiscal | INT | Sí | No | Régimen fiscal aplicable al cliente o producto |
| id_nacionalidad | INT | Sí | No | Nacionalidad del cliente al que se asocia el producto |
| principal | INT | Sí | No | Indica si es el factor principal (1: Sí, 0: No) |
| id_estatus | INT | Sí | No | Estatus del factor de riesgo |