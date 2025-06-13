| Nombre del Campo | Tipo de Dato | Permite Nulo | Llave Primaria | Descripción |
| --- | --- | --- | --- | --- |
| id_producto | INT | No | Sí | Identificador único del producto |
| id_producto_buro | INT | Sí | No | Referencia del producto en Buró de Crédito |
| id_producto_circulo | INT | Sí | No | Referencia del producto en Círculo de Crédito |
| id_empresa | INT | Sí | No | ID de la empresa a la que pertenece el producto |
| id_linea_fondeo | INT | Sí | No | ID de la línea de fondeo asociada al producto |
| id_tipo_modelo | INT | Sí | No | Tipo de modelo financiero del producto |
| nombre | VARCHAR(50) | Sí | No | Nombre corto del producto |
| reca | VARCHAR(60) | Sí | No | Clave o referencia del producto para uso interno |
| iva | DECIMAL(18) | Sí | No | Porcentaje de IVA aplicado al producto |
| iva_excento | INT | Sí | No | Indica si el producto está exento de IVA (1: Sí, 0: No) |
| id_tipo_pago_anticipado | INT | Sí | No | Tipo de aplicación de pagos anticipados |
| id_tipo_aplicacion_pago | INT | Sí | No | Forma en que se aplica el pago al producto |
| id_estado_cuenta_envio | INT | Sí | No | Modo de envío del estado de cuenta del producto |
| id_tipo_estado_cuenta | INT | Sí | No | Tipo de estado de cuenta que se genera |
| modo_seguro | INT | Sí | No | Indica si el producto tiene seguro asociado (1: Sí, 0: No) |
| id_estatus | INT | Sí | No | Estatus del producto |
| id_usuario_actualiza | INT | Sí | No | Usuario que realizó la última actualización |
| fecha_actualiza | DATETIME | Sí | No | Fecha de la última actualización del registro |
| nombre_producto | VARCHAR(50) | Sí | No | Nombre comercial del producto |