## ARCHIVO JS cat_productos_refactor.js
### Funciones
#### getProducts

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getrpoductslist"> 
    <strong>GetProductsList</strong>
  </a> para mostrar el listado de productos registrados al acceder al modulo.
#### getBlockStatus

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getsafemodepermission"> 
    <strong>GetSafeModePermission</strong>
  </a> que obtiene un valor booleano que sirve para validar si el usuario tiene la capacidad de bloquear/desbloquear un producto y mostrar el botón en el listado de registros.
#### loadInitCats

Esta función se ejecuta al acceder al modulo, realiza peticiones a los siguientes endpoints que consultan catálogos de listas desplegables y estructura del formulario.

* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getpropiedadesproducto"> 
    <strong>GetPropiedadesProducto</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getcalculationmodels"> 
    <strong>GetCalculationModels</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#gettypesend"> 
    <strong>GetTypeSend</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#gettypestatement"> 
    <strong>GetTypeStatement</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getlineafondeo"> 
    <strong>GetLineaFondeo</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#gettypeproductbureau"> 
    <strong>GetTypeProductBureau</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#gettypeproductcircle"> 
    <strong>GetTypeProductCircle</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#gettypeanticipedpayment"> 
    <strong>GetTypeAnticipedPayment</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#gettypeaplicatepayment"> 
    <strong>GetTypeAplicatePayment</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getmonedas"> 
    <strong>GetMonedas</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getregimenesfiscales"> 
    <strong>GetRegimenesFiscales</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getcanaltransaccional"> 
    <strong>GetCanalTransaccional</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getproductsimpact"> 
    <strong>GetProductsImpact</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getinstrumentosmonetariosref"> 
    <strong>GetInstrumentosMonetariosRef</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getstatecountry"> 
    <strong>GetStateCountry</strong>
  </a>
#### loadCats

Esta función se ejecuta al abrir el formulario de productos, realiza peticiones a los siguientes endpoints que consultan catálogos de listas desplegables.

* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getperiodsmodel"> 
    <strong>GetPeriodsModel</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getcalculationmodels"> 
    <strong>GetCalculationModels</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getratevariables"> 
    <strong>GetRateVariables</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getchargemodes"> 
    <strong>GetChargeModes</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getbaseamounts"> 
    <strong>GetBaseAmounts</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getlistelementos"> 
    <strong>GetListElementos</strong>
  </a> Este endpoint se consulta tres veces, para obtener los elementos propios de ordinarios, moratorios y gastos de cobranza
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getproductsdocuments"> 
    <strong>GetProductsdocuments</strong>
  </a>
* <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getproductconcepts"> 
    <strong>GetProductConcepts</strong>
  </a>
#### showOrd

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getcaracteristicsmodel"> 
    <strong>GetCaracteristicsModel</strong>
  </a> para mostrar las caracteristicas que serán asociadas directamente al producto, según el modelo seleccionado.
#### deleteProduct

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#postdeleteproductrefactor"> 
    <strong>PostDeleteProductRefactor</strong>
  </a> para eliminar lógicamente un producto, solo evita que se muestre en el listado inicial.
#### lockProduct

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#postsafemodeupdate"> 
    <strong>PostSafeModeUpdate</strong>
  </a> para bloquear o desbloquear el producto seleccionado.
#### saveConfigurations

Genera el payload necesario y realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#postsaveproductrefactor"> 
    <strong>PostSaveProductRefactor</strong>
  </a> para guardar un producto nuevo o actualizar uno ya existente, esto dependerá de si el payload tiene el id_producto o no.
#### getPeriods

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getgraceperiods"> 
    <strong>GetGracePeriods</strong>
  </a> para llenar el listado desplegable de periodos de gracia.
#### getSubMethods

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getsubmethodscalculation"> 
    <strong>GetSubmethodsCalculation</strong>
  </a> para llenar el listado desplegable de submétodos de calculo.
#### getProductoInterface

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/productos/#getproductinterface"> 
    <strong>GetProductInterface</strong>
  </a> para abrir el formulario con los datos del producto seleccionado para su actualización.