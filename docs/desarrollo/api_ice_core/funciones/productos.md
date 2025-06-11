## ARCHIVO CRUD product_refactor.py

### Funciones
#### get_calculation_models

Consulta el catálogo de registros activos  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_Modelos</strong>
  </a> CRÉDITO SIMPLE, ARRENDAMIENTO PURO, ARRENDAMIENTO FINANCIERO etc.
#### get_products_list

Consulta el catalogo básico de productos (nombre, modelo, método y submétodo, línea de fondeo y modo seguro) para mostrar en la tabla de la vista inicial en el módulo. Tablas: <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>direccion.tb_producto</strong>
  </a> , <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>general.LineaFondeo</strong>
  </a> , <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.MetodoCalculo</strong>
  </a> , <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>direccion.Tb_ProductoMetodo</strong>
  </a> , <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>general.SubmetodoCalculo</strong>
  </a> ,<a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_Modelos</strong>
  </a> 
#### get_product_properties

Consulta el archivo de configuración o esqueleto del formulario de productos.
#### get_safe_mode_permission

Función destinada a validar si el usuario cuenta con la capacidad de bloquear / desbloquear un producto. El criterio para esta validación aún esta pendiente por definirse, por ende, se retorna un true por default.
#### get_type_send

Consulta el catálogo de registros activos  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>Tb_MediosEnvio</strong>
  </a> 
#### get_type_statement_account

Consulta el catálogo de registros activos  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_TipoEstadoCuenta</strong>
  </a>, periódico o al corte
#### get_type_products_bureau

Consulta el catálogo de registros activos y con la clave de buro de crédito   <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.ProductoCatalogo</strong>
  </a> 
#### get_type_products_circle

Consulta el catálogo de registros activos  y con la clave de circulo de crédito     <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.ProductoCatalogo</strong>
  </a>
#### get_type_anticiped_payment

Consulta el catálogo de registros  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tipo_Pago_Anticipado</strong>
  </a>, reduce pago fijo o plazo
#### get_type_aplicate_payment

Consulta el catálogo de registros activos  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.TipoAplicacionPago</strong>
  </a> orden de prelación o amortización 
#### get_state_country

Consulta los registros de las tablas <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.pais</strong>
  </a>, <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.estado</strong>
  </a> y retorna un json con ambos catálogos
#### methods_calculation

Consulta el catálogo de registros <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.MetodoCalculo</strong>
  </a> filtrando por su relación a la tabla de  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_Modelos</strong>
  </a> usando el key_model 

``` json title="Payload de entrada"
{
    key_model: "",
}
```
#### get_periods_model

Consulta todos los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.PeriodoPago</strong>
  </a> relacionados a los modelos, aplicando filtro por la key_model 
  
``` json title="Payload de entrada"
{
    key_model: "",
}
```
#### get_type_rate_variables

Consulta el catálogo de registros  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.TipoTasaVariable</strong>
  </a> 
#### get_base_calculation_amounts

Consulta el catálogo de registros  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoMontosBaseCobro</strong>
  </a> relacionados a los modelos, aplicando filtro por la key_model 
  
``` json title="Payload de entrada"
{
    key_model: "",
}
```
#### get_product_concepts

Consulta los datos y características de los conceptos relacionados al modelo usando key_model  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_Conceptos</strong>
  </a>, <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoCategoriasConcepto </strong>
  </a>
<a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoFormasPago </strong>
  </a>,  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoTiposConcepto </strong>
  </a>, <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_Modelos </strong>
  </a>

``` json title="Payload de entrada"
{
    key_model: "",
}
```
#### get_model_caracteristics

Consulta las características relacionadas al modelo usando key_model    <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoCaracteristicas </strong>
  </a>

``` json title="Payload de entrada"
{
    key_model: "",
}
```
#### delete_product

Actualiza el id_estatus del producto selccionado a 0, inactivo.<a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_Productos</strong>
  </a>, 

``` json title="Payload de entrada"
{
    id: 1,
}
```
#### safe_mode_update

Actualiza el modo_seguro a 1 o 0, dependiendo del valor recibido, para activar o desactivar este modo. El modo seguro bloquea el producto a usuarios no autorizados <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_Productos</strong>
  </a>

``` json title="Payload de entrada"
{
    id: 1,
    safe_mode: 0
}
```
#### save_product

Recibe el pyaload y verifica si cuenta con un id producto para actualiza el registro, de lo contrario, lo crea, con el id producto, va actualizando/ registrando las demás dependencias. <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_Productos</strong>
  </a>

``` json title="Payload de entrada"
{
	"id": 0,
	"id_type_product_bureau": 0,
	"id_type_product_circle": 0,
	"company": 0,
	"id_fondeo_line": 0,
	"id_type_model": 0,
	"product_name": "",
	"comercial_name": "",
	"reca_number": "",
	"ivaMetodoCalculo": 0,
	"iva_excented_required": 0,
	"id_type_payment_anticiped": 0,
	"id_type_payment": 0,
	"id_account_statement_send": 0,
	"id_account_statement_cut": 0,
	"safe_mode": 0,
	"id_usuario_actualiza": 0,
	"id_method_calculation": 0,
	"id_product_method": 0,
	"id_submethod_calculation": 0,
	"id_type_grace": 0,
	"id_periodicity": 0,
	"number_payments": 0,
	"id_state": 0,
	"id_product_properties": 0,
	"residual_value": 0,
	"num_initial_rents": 0,
	"rental_expenses": 0,
	"sections": {
		"factorRiesgo":{
			"id":0,
			"id_rysk_factor":0,
			"id_type_risk_product": 0,
			"id_type_divisa": 0,
			"id_chanel": 0,
			"id_monetary_instrument": 0,
			"id_type_person": 0,
			"id_nationality": 0,
			"risk_required": 0,
			"id_state": 0,
			"details":{
				"id_risk_factor_detail":0,
				"id_risk_factor": 0,
				"id_country": 0,
				"id_state": 0
			}
		},
		"detallesSeguro":{
			"id": 0,
			"id_insurance": 0,
			"insurance_name": 0,
			"insurance_descriptions": 0,
			"insurance_contract_reference": 0,
			"insurance_warning": 0,
			"insurance": 0,
			"id_state":""
		},
		"products_caracteristics":{
			"id_product_characteristic": 0,
			"id_characteristic": 0,
			"value_characteristic": 0,
			"id_type_value": 0,
			"is_variable_rate": 0,
			"id_type_variable_rate": 0,
			"spread": 0,
			"id_base_amount": 0,
			"id_charge_mode": 0,
			"tolerance_days": 0,
			"creation_date": 0
		},
		"conceptos": {
			"id_product_concept": 0,
			"id": 0,
			"id_concept": 0,
			"name_concept": 0,
			"id_type_concept": 0,
			"type_concept": 0,
			"id_type_category": 0,
			"type_category": 0,
			"id_type_payment": 0,
			"type_payment": 0,
			"id_calculation_method": 0,
			"id_calculation_submethod": 0,
			"id_type_grace": 0,
			"id_paymenth_periodicity_concept": 0,
			"required_num_payments": 0,
			"number_payment": 0,
			"required_iva": 0,
			"iva_concept": 0,
			"is_required_concept": 0,
			"value_concept": 0,
			"id_type_value": 0,
			"creation_date": 0,
			"caracteristicas": {
				"id_concept_characteristic": 0,
				"id_product_concept": 0,
				"id_characteristic": 0,
				"name_characteristic": 0,
				"is_variable_rate": 0,
				"id_type_variable_rate": 0,
				"spread": 0,
				"id_type_value": 0,
				"value_characteristic": 0,
				"required_tolerance_days": 0,
				"tolerance_days": 0,
				"id_charge_mode": 0
			}
		}
	}
}
```

#### get_grace_periods_method

Consulta el catálogo de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>General.TiposGracia</strong>
  </a>  filtrando por su relación con submétodo de calculo 

``` json title="Payload de entrada"
{
    submethod_id: 1
}
```
#### submethods_calculation

Consulta el catálogo de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>General.SubMetodoCalculo</strong>
  </a>  filtrando por su relación con método de calculo 

``` json title="Payload de entrada"
{
    method_id: 1
}
```
#### get_product_interface

Consulta toda la data del producto, incluidas sus dependencias, y formula el payload o formulario, esto para mostrarlo en vista al momento de querer editar un producto.

``` json title="Payload de entrada"
{
    id_product: 1
}
```
