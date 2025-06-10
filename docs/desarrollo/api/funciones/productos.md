## ARCHIVO CRUD products.py
### Funciones

#### post_product_ins

Prepara el payload recibido para ejecutar el SP GENERAL.Sp_producto_Ins que inserta los campos necesarios en la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.producto</strong>
  </a>, en caso de que venga un id de producto valido, actualiza el registro con el payload entrante.
  
``` json title="Payload de entrada"
{
    "id_producto": "",
    "id_producto_catalogo": "",
    "producto": "",
    "id_empresa": "",
    "id_linea_fondeo": "",
    "reca": "",
    "iva": "",
    "id_estatus": "",
    "id_usuario_actualiza": "",
    "tipo_pago_anticipado": "",
    "id_moneda": "",
    "id_instrumento_monetario": "",
    "id_regimen_fiscal": "",
    "id_nacionalidad": "",
    "seguro": "",
    "descripcion_seguro": "",
    "aseguradora": "",
    "clausula_seguro": "",
    "advertencia_seguro": "",
    "estado_cuenta": "",
    "id_tipo_aplicacion_pago": "",
    "factoraje": "",
    "tasa_variable": "",
    "id_regimen_fiscal_cedente": "",
    "arrendamientop": "",
    "arrendamientof": "",
    "automotriz": "",
    "id_producto_condusef": "",
    "id_tipo_moratorio": ""
}
```
#### post_metodo_calculo_producto

Prepara el payload recibido para ejecutar el SP GENERAL.Sp_MetodoCalculoProducto_INS que inserta los campos necesarios en la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductometodoscalculo"> 
    <strong>GENERAL.ProductoMetodosCalculo</strong>
  </a> de esta manera se crea una relación entre el producto registrado y su método de calculo
  
``` json title="Payload de entrada"
{
    "id_producto": 1
    , "id_metodo_calculo": 1
    , "id_submetodo_calculo": 2
    , "id_tipo_gracia": 1
    , "id_periodo_pago": 1
    , "numero_pagos": 2
}
```
#### post_producto_documents_del

Prepara el payload recibido para ejecutar el SP GENERAL.Sp_ProductoDocumentos_Del que usando el id_producto elimina los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductometodoscalculo"> 
    <strong>GENERAL.ProductoDocumento</strong>
  </a>
  
``` json title="Payload de entrada"
{
    id_producto: 1,
}
```
#### post_product_det_del

Prepara el payload recibido para ejecutar el SP GENERAL.Sp_DetalleProductoAll_Del que usando el id_producto elimina los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>GENERAL.ProductoDetalle</strong>
  </a>
  
``` json title="Payload de entrada"
{
    id_producto: 1,
}
```
#### post_detalles_producto

Al ser el payload recibido un Array o List, inicia la función con un ciclo for, y por cada detalle en el payload ejecuta el SP GENERAL.Sp_DetallesProducto_Ins para insertar uno a uno los detalles en la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>GENERAL.ProductoDetalle</strong>
  </a>
  
``` json title="Payload de entrada"
[
    {
        id_producto: 1,
        id_producto_detalle_catalogo:1,
        id_tipo_medida_parametro: 1,
        valor: 10,
        orden: 1,
        es_financiado:  0,
        id_estatus: 1,
        id_usuario_actualiza: 1,
        fecha_actualiza: "",
        permite_financiar:  0,
        pago_anticipado:  0,
        calcula_iva: 0,
        interes_moratorio: 0,
        id_tasa_variable: 1,
        spread: 1,
        prorrateado: 0
    }
]
```
#### post_domicilio_cedente

Prepara el payload recibido para ejecutar el SP General.Sp_CedenteDomicilio_Ins que inserta los campos necesarios en la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>Cliente.domicilio</strong>
  </a>, en caso de que venga un id de domicilio valido, actualiza el registro con el payload entrante.
  
``` json title="Payload de entrada"
{
	id_domicilio: 0,
    id_cliente: 1,
    domicilio: "",
    num_exterior: 0,
    num_interior:  0,
    colonia: '',
    codigo_postal: '',
    id_localidad: 0,
    id_estado:  0,
    id_pais:  0,
    id_estatus: 0,
    id_municipio: 0,
}
```
#### post_cedente_fisico

Prepara el payload recibido para ejecutar el SP General.Sp_CedentePF_Ins que en primer lugar verifica si ya hay una PF relacionada al producto, consultando en la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.Tb_Cedente_Fisica</strong>
  </a> usando el id de producto, en caso de existir coincidencia actualiza el registro, de lo contrario,  inserta los campos necesarios en la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.Tb_Cedente_Fisica</strong>
  </a>
  
``` json title="Payload de entrada"
{
    id_producto: 1,
    id_regimen_fiscal: 1,
    nombre: '',
    apellido_paterno: '',
    apellido_materno: '',
    id_pais: 0,
    id_estado:0,
    id_ciudad:  0,
    id_localidad: 0,
    fecha_nacimiento: "",
    rfc: '',
    curp: '',
    id_estado_civil:  0,
    numero_identificacion: 0,
    correo_electronico: '',
    id_domicilio: 0,
}
```
#### create_ceding_bank

Prepara el payload recibido, añade las claves de fecha registro y fecha actualiza con la fecha actual, el id estatus 1 y elimina, en caso de existir, la clave id cedente banco y ejecuta el SP General.Sp_Cedente_Banco_Ins que inserta los campos necesarios en la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.Tb_Cedente_Banco</strong>
  </a>
  
``` json title="Payload de entrada"
{
	id_cedente: 0
  , id_regimen_fiscal_cedente: 0
  , banco: ""
  , sucursal: ""
  , numero_cuenta: ""
  , numero_clabe: ""
  , pagina_web: ""
  , id_usuario_actualiza: 0
}
```
#### update_ceding_bank

Prepara el payload recibido, añade la clave fecha actualiza con la fecha actual y ejecuta el SP General.Sp_Cedente_Banco_Mod que actualiza el registro correspondiente en la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.Tb_Cedente_Banco</strong>
  </a>
  
``` json title="Payload de entrada"
{
	id_cedente: 0
  , banco: ""
  , sucursal: ""
  , numero_cuenta: ""
  , numero_clabe: ""
  , pagina_web: ""
  , id_usuario_actualiza: 0
  , fecha_actualiza: ""
}
```
#### post_cedent_documents_del

Prepara el payload recibido, y ejecuta el SP General.Sp_CedenteDocumentos_Del que valida el régimen fiscal del cedente registrado, en caso de ser PF obtiene su id de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.Tb_Cedente_Fisica</strong>
  </a>, en caso de ser PM lo obtiene de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.Tb_Cedente_Moral</strong>
  </a>
y elimina el registro relacionado de la tabla   <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.Tb_Cedente_Documento</strong>
  </a>
  
``` json title="Payload de entrada"
{
	id_producto: 1
}
```
#### post_cedent_documents_ins

Al ser el payload recibido un Array o List, inicia la función con un ciclo for, y por cada detalle en el payload ejecuta el SP General.Sp_CedenteDocumentos_Ins que inserta los campos necesarios en la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.Tb_Cedente_Documento</strong>
  </a>
  
``` json title="Payload de entrada"
[
	{
		id_documento_cedente: 1,
		id_regimen_fiscal: 1,
		id_cedente: 1,
	}
]
```
#### post_cedente_moral

Prepara el payload recibido para ejecutar el SP General.Sp_CedentePM_Ins que en primer lugar verifica si ya hay una PM relacionada al producto, consultando en la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.Tb_Cedente_Moral</strong>
  </a> usando el id de producto, en caso de existir coincidencia actualiza el registro, de lo contrario,  inserta los campos necesarios en la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.Tb_Cedente_Moral</strong>
  </a>
  
``` json title="Payload de entrada"
{
        id_producto: "",
        razon_social: "",
        numero_escritura_emp: "",
        fecha_escritura_emp: "",
        id_estado_escritura_emp: "",
        id_localidad_escritura_emp: "",
        nombre_notario_emp: "",
        apellido_paterno_notario_emp: "",
        apellido_materno_notario_emp: "",
        numero_notario_emp: "",
        id_estado_notario_emp: "",
        id_localidad_notario_emp: "",
        folio_mercantil_emp: "",
        fecha_registro_emp: "",
        rfc_emp: "",
        correo_emp: "",
        id_estado_registro_publico_emp: "",
        id_localidad_registro_publico_emp: "",
        id_domicilio_emp: "",
        nombre_rep: "",
        apellido_paterno_rep: "",
        apellido_materno_rep: "",
        numero_escritura_rep: "",
        fecha_escritura_rep: "",
        rfc_rep: "",
        id_estado_rep: "",
        id_localidad_rep: "",
        nombre_notario_rep: "",
        apellido_paterno_notario_rep: "",
        apellido_materno_notario_rep: "",
        numero_notario_rep: "",
        id_estado_notario_rep: "",
        id_localidad_notario_rep: "",
        folio_mercantil_rep: "",
        fecha_registro_rep: "",
        id_estado_registro_publico_rep: "",
        id_localidad_registro_publico_rep: "",
        id_usuario: "",
}
```

#### get_instrumento_monetario

Ejecuta el SP General.Sp_InstrumentoMonetario_Obt que retorna todos los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.InstrumentoMonetario</strong>
  </a>
#### get_detalles_producto_catalogo

Ejecuta el SP General.Sp_DetallesProductoCatalogo_Obt que retorna todos los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetallecatalogo"> 
    <strong>General.ProductoDetallecatalogo</strong>
  </a>
#### get_tipo_medida_parametro

Ejecuta el SP General.Sp_TipoMedidaParametro_Obt que retorna todos los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetallecatalogo"> 
    <strong>General.TipoMedidaParametro</strong>
  </a>
#### get_documents_cedent_catalog

Ejecuta el SP General.Sp_DocumentoCedente_Obt que retorna todos los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetallecatalogo"> 
    <strong>General.Tb_Documento_Cedente</strong>
  </a>
#### get_documentos

Ejecuta el SP General.Sp_Documentos_Obt que retorna todos los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetallecatalogo"> 
    <strong>General.DocumentoDigitalizado</strong>
  </a> relacionados con el id usuario
  
``` json title="Payload de entrada"
{
	id_usuario: 1
}
```
#### get_product_type_mora_rate

Ejecuta el SP General.Sp_TipoMoratorioRevolvente_Obt que retorna todos los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetallecatalogo"> 
    <strong>General.Tb_TipoMoratorioRevolvente</strong>
  </a>
  
``` json title="Payload de entrada"
{
	id_producto: 1
}
```
#### get_producto_guardado

Ejecuta el SP General.Sp_ProductoGuardado_Obt que retorna el registro que coincida con el id producto de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>General.Producto</strong>
  </a>
  
``` json title="Payload de entrada"
{
	id_producto: 1
}
```
#### get_detalles_producto

Ejecuta el SP General.Sp_DetallesProducto_Obt que retorna los registros relacionados con el id producto de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.ProductoDetalle</strong>
  </a>
  
``` json title="Payload de entrada"
{
	id_producto: 1
}
```
#### get_metodo_calculo_producto

Ejecuta el SP General.Sp_MetodosCalculo_Obt que retorna los registros relacionados con el id producto de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>General.ProductoMetodosCalculo</strong>
  </a>
  
``` json title="Payload de entrada"
{
	id_producto: 1
}
```
#### get_domicilio_cedente

Ejecuta el SP General.Sp_CedenteDomicilio_Obt que retorna los registros relacionados con el id producto de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>Cliente.domicilio</strong>
  </a>
  
``` json title="Payload de entrada"
{
	id_producto: 1
}
```
#### get_cedente_moral

Ejecuta el SP General.Sp_CedentePM_Obt que retorna los registros relacionados con el id producto de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>GENERAL.Tb_Cedente_Moral</strong>
  </a>
  
``` json title="Payload de entrada"
{
	id_producto: 1
}
```
#### get_ceding_bank

Ejecuta el SP General.Sp_Cedente_Banco_Obt que retorna los registros relacionados con el id cedente y régimen fiscal  de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>GENERAL.Tb_Cedente_Banco</strong>
  </a>, en caso de no tener resultados, retorna un array, con un registro con valores 0 y ""
  
``` json title="Payload de entrada"
{
	id_cedente: 1
	, id_regimen_fiscal
}
```
#### get_cedent_document

Ejecuta el SP General.Sp_CedenteDocumentos_Obt que retorna los registros relacionados con el id cedente y régimen fiscal  de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>GENERAL.Tb_Cedente_Documento</strong>
  </a> 
  
``` json title="Payload de entrada"
{
	id_cedente: 1
	, id_regimen_fiscal
}
```
#### get_cedente_fisico

Ejecuta el SP General.Sp_CedentePF_Obt que retorna los registros relacionados con el id producto de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>GENERAL.Tb_Cedente_Fisica</strong>
  </a>
  
``` json title="Payload de entrada"
{
	id_producto: 1
}
```
#### get_product_submetod_refactor

Ejecuta el SP General.Sp_MetodosSubmetodosRefactor_Obt que retorna los registros relacionados con el id metodo de calculo de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>GENERAL.SubmetodoCalculo</strong>
  </a>
  
``` json title="Payload de entrada"
{
	id_metodo_calculo: 1
}
```

#### get_configuration_automotriz_method

Ejecuta una consulta sql para obtener el registro con la clave MetodoAutomotriz de la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>GENERAL.Tb_ConfigAplicacion</strong>
  </a>
#### get_lineas_fondeo

Ejecuta el SP GENERAL.Sp_LineasFondeo_Obt que obtiene el catálogo de líneas de fondeo de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>GENERAL.lineafondeo</strong>
  </a> filtrando las relacionadas al usuario
  
``` json title="Payload de entrada"
{
	id_usuario: 1
}
```

