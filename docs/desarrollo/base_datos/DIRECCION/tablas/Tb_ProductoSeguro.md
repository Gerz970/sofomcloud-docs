| Nombre del Campo | Tipo de Dato | Permite Nulo | Llave Primaria | Descripción |
| --- | --- | --- | --- | --- |
| id_seguro | INT | No | Sí | Identificador único del seguro asociado al producto |
| id_producto | INT | No | No | Identificador del producto al que pertenece el seguro |
| aseguradora | NVARCHAR(100) | Sí | No | Nombre de la compañía aseguradora |
| descripcion_seguro | NVARCHAR(300) | Sí | No | Descripción general del seguro |
| clausula_seguro | NVARCHAR(100) | Sí | No | Cláusula principal del seguro |
| advertencia_seguro | NVARCHAR(100) | Sí | No | Advertencias importantes del seguro |
| principal | INT | Sí | No | Indica si es el seguro principal (1: Sí, 0: No) |
| id_estatus | INT | Sí | No | Estatus del registro de seguro |