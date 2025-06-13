| Nombre del Campo | Tipo de Dato | Permite Nulo | Llave Primaria | Descripción |
| --- | --- | --- | --- | --- |
| id_producto_concepto | INT | No | Sí | Identificador único del concepto asociado al producto |
| id_producto | INT | No | No | ID del producto relacionado |
| id_concepto | INT | No | No | ID del concepto base asociado |
| nombre_concepto | NVARCHAR(50) | Sí | No | Nombre del concepto |
| id_tipo_concepto | INT | No | No | Identificador del tipo de concepto |
| nombre_tipo_concepto | NVARCHAR(50) | Sí | No | Nombre del tipo de concepto |
| id_categoria | INT | No | No | Identificador de la categoría del concepto |
| nombre_tipo_categoria | NVARCHAR(50) | Sí | No | Nombre de la categoría del concepto |
| id_forma_pago | INT | Sí | No | Forma de pago asociada al concepto |
| nombre_forma_pago | NVARCHAR(50) | Sí | No | Nombre de la forma de pago |
| id_metodo_calculo | INT | Sí | No | Método de cálculo aplicado al concepto |
| id_submetodo_calculo | INT | Sí | No | Submétodo de cálculo aplicado al concepto |
| id_tipo_gracia | INT | Sí | No | Tipo de periodo de gracia aplicado al concepto |
| id_periodo_pago_concepto | INT | Sí | No | Periodo de pago correspondiente al concepto |
| requiere_pagos | INT | Sí | No | Indica si el concepto requiere pagos (1: Sí, 0: No) |
| num_pagos | INT | Sí | No | Número de pagos requeridos para el concepto |
| requiere_iva | INT | Sí | No | Indica si el concepto requiere IVA (1: Sí, 0: No) |
| iva_concepto | DECIMAL(18) | Sí | No | Tasa de IVA aplicable al concepto |
| requiere_concepto | INT | Sí | No | Indica si el concepto es obligatorio (1: Sí, 0: No) |
| valor | DECIMAL(18,4) | Sí | No | Valor numérico asignado al concepto |
| id_tipo_valor | INT | Sí | No | Tipo de valor del concepto (monto fijo, porcentaje, etc.) |
| fecha_creacion | DATETIME | Sí | No | Fecha en la que se creó el registro |
| fecha_actualiza | DATETIME | Sí | No | Fecha de última modificación del registro |
| id_estatus | BIT | Sí | No | Estatus del concepto |