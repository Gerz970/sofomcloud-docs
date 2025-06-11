## ARCHIVO JS cat_productos_agregar.js
### Funciones
#### setListModes

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getchargemodes"> 
    <strong>GetChargeModes</strong>
  </a> para llenar la lista desplegable de modos de cobro.
#### setListElementsCaracteristics

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getlistelementos"> 
    <strong>GetListElementos</strong>
  </a> para llenar la lista desplegable de elementos por cada característica que aplique (Ord, mora, cobranza).
#### setListCaracteristics

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getlistcaracteristicas"> 
    <strong>GetListCaracteristicas</strong>
  </a> para mostrar en pantalla, en la tab secundaria, las características e inicializar los valores de cada una, en caso de no tener características aplicables, ocultar la tab.
#### setListCategorys

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getlistcategorias"> 
    <strong>GetListCategorias</strong>
  </a> para llenar la lista desplegable de categorias.
#### setListPayWays

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getlistformaspago"> 
    <strong>GetListFormasPago</strong>
  </a> para llenar la lista desplegable de formas de pago, en caso de que no se obtengan registro, oculta la tab de características. 
#### saveConfigurations

Realiza la construcción del payload, y con una variable de validación, ejecuta el guardado del concepto con una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#postcreateconcept"> 
    <strong>PostCreateConcept</strong>
  </a>  o el actualizado del concepto con una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#postupdateconcept"> 
    <strong>PostUpdateConcept</strong>
  </a>.
#### getConceptLogs

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getlogs"> 
    <strong>GetLogs</strong>
  </a> para llenar el listado de acciones realizadas en el modulo..
#### conceptActive

Realiza la construcción del payload y con una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#postupdateconcept"> 
    <strong>PostUpdateConcept</strong>
  </a> actualiza el estatus del concepto únicamente, no modifica nada más, aunque es necesario mandar el payload completo.
#### loadConcepts

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getconcepts"> 
    <strong>GetConcepts</strong>
  </a> para mostrar el listado de los conceptos registrados al momento de acceder al modulo.
#### loadInitCats

Realiza una petición al endpoint <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getforms"> 
    <strong>GetForms</strong>
  </a> para crear la vista del formulario de conceptos, ya que sus campos se muestran dinámicamente.
#### loadCats

Realiza una petición a los endpoints <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getmeasurement"> 
    <strong>GetMeasurement</strong>
  </a>,  <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getlisttiposconceptos"> 
    <strong>GetListTiposConceptos</strong>
  </a>, <a href="../../../../../desarrollo/sofom_ice_core/backend/funciones/conceptos/#getcalculationmodels"> 
    <strong>GetCalculationModels</strong>
  </a>para para el llenado de las listas desplegables inicales.