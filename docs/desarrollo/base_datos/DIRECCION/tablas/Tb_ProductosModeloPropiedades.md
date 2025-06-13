| Nombre del Campo | Tipo de Dato | Permite Nulo | Llave Primaria | Descripción |
| --- | --- | --- | --- | --- |
| id_producto_propiedades | INT | No | Sí | Identificador único de propiedades del modelo del producto |
| id_producto | INT | No | No | Identificador del producto asociado |
| arr_valor_residual | DECIMAL(18,2) | Sí | No | Valor residual en esquemas de arrendamiento |
| arr_num_rentas_iniciales | INT | Sí | No | Número de rentas iniciales requeridas |
| arr_gastos_administracion | BIT | Sí | No | Indica si se aplican gastos de administración (1: Sí, 0: No) |