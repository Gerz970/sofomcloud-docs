## ARCHIVO CRUD product_concepts.py

### Funciones
#### get_charge_modes

Consulta los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoModosCobro</strong>
  </a>, usando la clave characteristic_key MOR - GC para filtrar los registros por su relación con la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoCaracteristicas</strong>
  </a> en la tabla intermedia <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_ConfiguracionModosCobro</strong>
  </a>
  
``` json title="Payload de entrada"
{
    characteristic_key: "MOR",
}
```
#### get_elements

Consulta los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoElementos</strong>
  </a>, usando la clave characteristic_key MOR - GC - ORD para filtrar los registros por su relación con la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoCaracteristicas</strong>
  </a> en la tabla intermedia <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_ConfiguracionElementos</strong>
  </a>

``` json title="Payload de entrada"
{
    characteristic_key: "ORD",
}
```
#### get_characteristics

Consulta los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoCaracteristicas</strong>
  </a> usando la clave category_key y payment_methods_key  para filtrar los registros por su relación con las tablas <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.tb_catalogoFormasPago</strong>
  </a> y <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.tb_catalogoCategoriasConcepto</strong>
  </a> en la tabla intermedia <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_ConfiguracionCaracteristicas</strong>
  </a>
  
``` json title="Payload de entrada"
{
    category_key: "GAS",
    payment_methods_key: "FIN"
}
```
#### get_concept_categories

Consulta los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.tb_catalogoCategoriasConcepto</strong>
  </a>, usando la clave concept_key CRE - IMP para filtrar los registros por su relación con la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoCaracteristicas</strong>
  </a> en la tabla intermedia <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_ConfiguracionCategoria</strong>
  </a>
  
``` json title="Payload de entrada"
{
    concept_key: "",
}
```
#### get_payment_methods

Consulta los registros <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoFormasPago</strong>
  </a>, usando las claves del concepto concept_key y category_key, filtrando por su relación con la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoCategoriasConcepto</strong>
  </a> y  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_CatalogoTiposConcepto</strong>
  </a> en la tabla intermedia  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>GENERAL.Tb_ConfiguracionFormasPago</strong>
  </a>
  
``` json title="Payload de entrada"
{
    concept_key: "",
    category_key: ""
}
```
#### update_concept

Ejecuta el SP DIRECCION.Sp_AdministracionConceptos_Mod que actualiza un concepto en la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_Conceptos</strong>
  </a> , inserta sus características nuevas y actualiza las existentes en  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_AdministracionCaracteristicas</strong>
  </a> 
  
``` json title="Payload de entrada"
{
    "id_concept": 1,
    "name_concept" : "",
    "description_concept" : "",
    "type_concept" : "",
    "calculation_model" : "",
    "category_concept" : "",
    "payment_method" : "",
    "periodicity"  : 0,
    "required" : 0,
    "type_value" : 0,
    "iva_applies": 0,
    "id_state": 1,
    "characteristics":[
        {
            "id_characteristic" :0,
            "key_characteristic" : "",
            "type_rate" : "",
            "tolerance_days" :0,
            "id_charge_mode" :0,
            "key_element" : ""
        }
    ]
}
```
#### create_concept

Ejecuta el SP DIRECCION.Sp_AdministracionConceptos_Ins que inserta un concepto en la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_Conceptos</strong>
  </a> e inserta sus características en  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_AdministracionCaracteristicas</strong>
  </a> 
  
``` json title="Payload de entrada"
{
    "id_concept": 0,
    "name_concept" : "",
    "description_concept" : "",
    "type_concept" : "",
    "calculation_model" : "",
    "category_concept" : "",
    "payment_method" : "",
    "periodicity"  : 0,
    "required" : 0,
    "type_value" : 0,
    "iva_applies": 0,
    "id_state": 1,
    "characteristics":[
        {
            "id_characteristic" :0,
            "key_characteristic" : "",
            "type_rate" : "",
            "tolerance_days" :0,
            "id_charge_mode" :0,
            "key_element" : ""
        }
    ]
}
```
#### get_concept_log

Consulta todos los registros de acciones realizadas en modulo por todos los usuarios de la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_ConceptosLog</strong>
  </a>
#### get_product_concepts

Consulta todos los registros de conceptos de la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_Conceptos</strong>
  </a> y <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_AdministracionCaracteristicas</strong>
  </a> 
#### get_forms

Consulta el archivo de configuración o esqueleto del formulario de conceptos
#### get_measurement_types_concepts

Consulta los elementos usados para el concepto como tal de la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>general.Tb_CatalogoElementos</strong>
  </a> , valor o porcentaje
#### get_type_concepts

Consulta los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>General.Tb_CatalogoTiposConcepto</strong>
  </a>  crédito, adicional, extraordinario inicial o al vencimiento, e informativo.
#### get_product_concepts

Consulta todos los registros de conceptos de la tabla  <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_Conceptos</strong>
  </a> y <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_AdministracionCaracteristicas</strong>
  </a> 

