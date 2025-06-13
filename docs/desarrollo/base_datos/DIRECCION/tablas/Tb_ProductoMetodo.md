| Nombre del Campo | Tipo de Dato | Permite Nulo | Llave Primaria | Descripción |
| --- | --- | --- | --- | --- |
| id_producto_metodo | INT | No | Sí | Identificador único del método de cálculo del producto |
| id_producto | INT | Sí | No | ID del producto relacionado |
| id_metodo_calculo | INT | Sí | No | Método de cálculo financiero utilizado |
| id_submetodo_calculo | INT | Sí | No | Submétodo de cálculo (detalle del método) |
| id_tipo_gracia | INT | Sí | No | Tipo de periodo de gracia aplicable |
| id_periodo_pago | INT | Sí | No | Periodo de pago establecido para el producto |
| numero_pagos | INT | Sí | No | Número total de pagos establecidos |
| fecha_actualiza | DATETIME | Sí | No | Fecha de última modificación del registro |
| id_estatus | INT | Sí | No | Estatus del registro |