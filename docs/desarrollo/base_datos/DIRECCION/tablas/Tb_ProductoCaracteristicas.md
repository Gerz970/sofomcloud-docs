| Nombre del Campo | Tipo de Dato | Permite Nulo | Llave Primaria | Descripción |
| --- | --- | --- | --- | --- |
| id_producto_caracteristica | INT | No | Sí | Identificador único del registro de característica del producto |
| id_producto | INT | No | No | Identificador del producto relacionado |
| id_caracteristica | INT | No | No | Identificador de la característica asociada al producto |
| valor | DECIMAL(18,4) | Sí | No | Valor numérico asignado a la característica |
| id_tipo_valor | INT | No | No | Tipo de valor (entero, decimal, booleano, etc.) |
| es_tasa_variable | INT | Sí | No | Indica si es una tasa variable (1: Sí, 0: No) |
| id_tasa_variable | INT | Sí | No | Identificador de la tasa variable asociada |
| spread | DECIMAL(18,4) | Sí | No | Porcentaje adicional sobre la tasa base (spread) |
| id_monto_base_cobro | INT | Sí | No | Base de cálculo para el cobro del producto |
| id_tipo_cobro | INT | Sí | No | Tipo de cobro aplicable |
| dias_tolerancia | INT | Sí | No | Cantidad de días de tolerancia permitida |
| id_estatus | INT | Sí | No | Estatus del registro |
| fecha_creacion | DATETIME | Sí | No | Fecha en la que se creó el registro |
| fecha_actualiza | DATETIME | Sí | No | Fecha de la última actualización del registro |