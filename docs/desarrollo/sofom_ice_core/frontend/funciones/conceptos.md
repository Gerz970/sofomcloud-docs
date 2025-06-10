## ARCHIVO JS cat_productos_agregar.js
### Funciones
#### LoadListas

Realiza peticiones a los siguientes endpoints que consultan los catálogos de listas desplegables.

* <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getproductcatalogoapi"> 
    <strong>GetProductCatalogoAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getempresasapi"> 
    <strong>GetEmpresasAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getlineasfondeoapi"> 
    <strong>GetLineasFondeoAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getmetodoscalculo"> 
    <strong>GetMetodosCalculo</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getsubmetodoscalculo"> 
    <strong>GetSubmetodosCalculo</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getmonedasapi"> 
    <strong>GetMonedasAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getregimenfiscalapi"> 
    <strong>GetRegimenFiscalAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getnacionalidadapi"> 
    <strong>GetNacionalidadAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getdetallescatalogoapi"> 
    <strong>GetDetallesCatalogoAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#gettiposmedidaapi"> 
    <strong>GetTiposMedidaAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospago"> 
    <strong>GetPeriodosPago</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#gettiposgracia"> 
    <strong>GetTiposGracia</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#gettasasactualesapi"> 
    <strong>GetTasasActualesAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getdocumentosdisponiblesapi"> 
    <strong>GetDocumentosDisponiblesAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getpaisesapi"> 
    <strong>GetPaisesAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getpaisestadoapi"> 
    <strong>GetPaisEstadoAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getestadoscivilesapi"> 
    <strong>GetEstadosCivilesAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/riesgos/#getproductsimpactapi"> 
    <strong>GetProductsImpactAPI</strong>
  </a> 
* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getconfiguracionautomotrizmethod"> 
    <strong>GetConfiguracionAutomotrizMethod</strong>
  </a> 
#### get_block_reports_documents

Realiza una petición al siguiente endpoint que obtiene los catálogos necesario para la pestaña de documentos, además, consulta los documentos relacionados al producto en caso de mandarle un id valido

* <a href="../../../../../desarrollo/sofom/backend/funciones/reportes/#getblockreportsdocuments"> 
    <strong>GetBlockReportsDocuments</strong>
  </a>
#### CargaProducto

Esta función se ejecuta al momento de querer editar un producto, pues al iniciar la carga de pantalla, se verifica que venga en la url un id de producto, en caso de haberlo se llama esta función pasando el id. Inicialmente consulta los siguientes endpoints

* <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getproductoguardadoapi"> 
    <strong>GetProductoGuardadoAPI</strong>
  </a>
* <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getdetallesproductoapi"> 
    <strong>GetDetallesProductoAPI</strong>
  </a>
*  <a href="../../../../../desarrollo/sofom/backend/funciones/riesgos/#getproductsimpactapi"> 
    <strong>GetProductsImpactAPI</strong>
  </a>
* <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getmetodocalculoproductoapi"> 
    <strong>GetMetodoCalculoProductoAPI</strong>
  </a>

Una vez consultado el método de calculo del producto, verifica si este es metodo revolvente, en caso de serlo, consulta el siguiente endpoint usando la clave de revolvente

* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospagometodo"> 
    <strong>GetPeriodosPagoMetodo</strong>
  </a>

Se procede a realizar varias validaciones, en las cuales se consultan ciertos endpoints

1. Se valida que el producto sea tasa variable únicamente: Se realiza otra validación anidada, en la cual se revisa que existan detalles relacionados al producto y se consultan los siguientes endpoints. Después se prepara la estructura de los detalles o conceptos con la data obtenida

    * <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#gettasasactualesapi"> 
    <strong>GetTasasActualesAPI</strong>
  </a> 
    * <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getdesctasasactualesapi"> 
    <strong>GetDescTasasActualesAPI</strong>
  </a>

2. Se valida que el producto sea factoraje con tasa fija : Se realiza otra validación anidada, en la cual se revisa que existan detalles relacionados al producto, después se prepara la estructura de los detalles o conceptos con la data obtenida

3. Se valida que el producto sea factoraje con tasa variable: Se realiza otra validación anidada, en la cual se revisa que existan detalles relacionados al producto y se consultan los siguientes endpoints. Después se prepara la estructura de los detalles o conceptos con la data obtenida

    * <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#gettasasactualesapi"> 
    <strong>GetTasasActualesAPI</strong>
  </a> 
    * <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getdesctasasactualesapi"> 
    <strong>GetDescTasasActualesAPI</strong>
  </a>
  
4. Se valida que el producto sea revolvente con tasa variable: Se realiza otra validación anidada, en la cual se revisa que existan detalles relacionados al producto y se consultan los siguientes endpoints. Después se prepara la estructura de los detalles o conceptos con la data obtenida

    * <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#gettasasactualesapi"> 
    <strong>GetTasasActualesAPI</strong>
  </a> 
    * <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getdesctasasactualesapi"> 
    <strong>GetDescTasasActualesAPI</strong>
  </a>

5. Se valida que el producto sea automotriz con tasa fija : Se realiza otra validación anidada, en la cual se revisa que existan detalles relacionados al producto, después se prepara la estructura de los detalles o conceptos con la data obtenida

6. Se valida que el producto sea arrendamiento puro o financiero con tasa fija : Se realiza otra validación anidada, en la cual se revisa que existan detalles relacionados al producto, después se prepara la estructura de los detalles o conceptos con la data obtenida

7. Se valida que el producto sea arrendamiento financiado con tasa variable :Se realiza otra validación anidada, en la cual se revisa que existan detalles relacionados al producto y se consultan los siguientes endpoints. Después se prepara la estructura de los detalles o conceptos con la data obtenida

    * <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#gettasasactualesapi"> 
    <strong>GetTasasActualesAPI</strong>
  </a> 
    * <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getdesctasasactualesapi"> 
    <strong>GetDescTasasActualesAPI</strong>
  </a>
  
8. Se valida que el producto contenga cedente y se consultan los siguientes endpoints, despues prepara y alamcena la data en memoria para su uso más adelante.

    * <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getdomiciliocedenteapi"> 
    <strong>GetDomicilioCedenteAPI</strong>
  </a> 
    * <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getpersonamoralapi"> 
    <strong>GetPersonaMoralAPI</strong>
  </a> o <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getpersonamoralapi"> 
    <strong>GetPersonaFisicaAPI</strong>
  </a> según el régimen fiscal del cedente
    * <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#getcedentebancoapi"> 
    <strong>GetCedenteBancoAPI</strong>
  </a>
    * <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postobtdocumentcedentapi"> 
    <strong>PostObtDocumentCedentAPI</strong>
  </a>
    
Se consultan los siguientes endpoints referentes a localidades y estados

* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getpaisesestadoslocalidadesapi"> 
    <strong>GetPaisesEstadosLocalidadesAPI</strong>
  </a> se ejecuta este endpoint varias veces para las listas desplegables de domicilio de cedente PF y PM, notario, representante legal, y localidades general.
* <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getpaisesestadosmunicipiosapi"> 
    <strong>GetPaisesEstadosMunicipiosAPI</strong>
  </a> se ejecuta este endpoint varias veces para las listas desplegables de domicilio de cedente PF y PM, notario, representante legal, y localidades general.

#### conceptoFactoraje

Esta función se encarga de pintar los conceptos requeridos cuando la opción o checkbox de factoraje es activada o desactivada, por ende, realiza ciertas validaciones según su valor y el de tasa variable.

1. Se valida si es tasa variable y factoraje a la vez: Dentro de esta validación se consultan los periodos de pago relacionados a factoraje, y se asignan por default el método amortizado, submétodo saldos insolutos y periodo diario, además de bloquear los campos

    * <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospagometodo"> 
    <strong>GetPeriodosPagoMetodo</strong>
  </a>
  
    Una vez hecho lo anterior, se preparan los conceptos que serán mostrados en vista, propios de factoraje como interés ordinario, tasa variable, spread, honorarios, aforo
   
2. Se valida si es tasa variable pero no es factoraje: Se consultan los periodos de pago generales, para después añadir los conceptos tasa variable y spread

    * <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospagometodo"> 
    <strong>GetPeriodosPagoMetodo</strong>
  </a>
   
  
3. Se valida que no es tasa variable y tampoco es factoraje: Se consultan los periodos de pago generales, para después quitar los conceptos propios de factoraje y tasa variable, mostrar solo los generales en pantalla

    * <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospagometodo"> 
    <strong>GetPeriodosPagoMetodo</strong>
  </a>
   
  
4. Se valida que no es tasa variable y pero si es factoraje: Dentro de esta validación se consultan los métodos de pago relacionados a factoraje, y se asignan por default el método amortizado, submétodo saldos insolutos y periodo diario, además de bloquear los campos

    * <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospagometodo"> 
    <strong>GetPeriodosPagoMetodo</strong>
  </a>
  
    Una vez hecho lo anterior, se preparan los conceptos que serán mostrados en vista, propios de factoraje como interés ordinario, honorarios, aforo

#### conceptoAutomotriz

Esta función se encarga de pintar los conceptos requeridos cuando la opción o checkbox de automotriz es activada, por ende, desactiva el resto de opciones: factoraje y arrendamientos, además de desactivar tasas variable. Solo realiza la validación de que el automotriz este activada 

Consulta los periodos de pago de automotriz al endpoint 
<a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospagometodo"> 
    <strong>GetPeriodosPagoMetodo</strong>
  </a> para despues añadir los conceptos de auto motriz como comisión de apertura, enganche, ordinario, moratorios, seguro de daños, seguro de vida y accesorios

#### conceptoArrendamientoP

Esta función se encarga de pintar los conceptos requeridos cuando la opción o checkbox de arrendamiento puro es activada o desactivada, por ende, realiza dos validaciones según el valor del checkbox

1. Se valida si es arrendamiento puro: Dentro de esta validación se consultan los periodos de pago relacionados a arrendamiento, y se asignan por default el método amortizado, submétodo saldos globales y periodo mensual, además de bloquear los campos

    * <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospagometodo"> 
    <strong>GetPeriodosPagoMetodo</strong>
  </a>
    
    Una vez hecho lo anterior, se preparan los conceptos que serán mostrados en vista, propios de arrendamiento puro como comisión de apertura, renta extraordinaria, interés ordinario, interés moratorios, valor seguro, seguro, accesorios, deposito garantía, otros gastos, valor residual, comisión administración, mantenimiento plus, placas y tenencia 1er año

2. Se valida que no es arrendamiento puro: Dentro de esta validación, se consultan los periodos de pago generales

    * <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospagometodo"> 
    <strong>GetPeriodosPagoMetodo</strong>
  </a>

#### conceptoArrendamientoF

Esta función se encarga de pintar los conceptos requeridos cuando la opción o checkbox de arrendamiento financiero es activada o desactivada, por ende, realiza dos validaciones según el valor del checkbox

1. Se valida si es arrendamiento financiero: Dentro de esta validación se consultan los periodos de pago relacionados a arrendamiento, y se asignan por default el método amortizado, submétodo saldos globales y periodo mensual, además de bloquear los campos

    * <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospagometodo"> 
    <strong>GetPeriodosPagoMetodo</strong>
  </a>
    
    Una vez hecho lo anterior, se preparan los conceptos que serán mostrados en vista, propios de arrendamiento puro como comisión de apertura, anticipo, interés ordinario, interés moratorios, valor seguro, accesorios, deposito garantía, otros gastos, valor residual, comisión administración, mantenimiento plus, placas y tenencia 1er año

2. Se valida que no es arrendamiento finaciero: Dentro de esta validación, se consultan los periodos de pago generales

    * <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospagometodo"> 
    <strong>GetPeriodosPagoMetodo</strong>
  </a>

#### conceptoRevolvente

Esta función se encarga de pintar los conceptos requeridos cuando la opción o checkbox de revolvente es activada, y realiza dos validaciones según tasa variable activada o desactivada, además de consulta los periodos de pago relacionados a revolvente <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospagometodo"> 
    <strong>GetPeriodosPagoMetodo</strong>
  </a>

1. Se valida si es tasa variable: se preparan los conceptos interés ordinario, interés moratorios, tasa variable, spread, comisión por disposición, comisión por apertura

2. Se valida que no es tasa variable: se preparan los conceptos interés ordinario, interés moratorios, comisión por disposición, comisión por apertura

#### citybystate

Consulta los endpoints <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getpaisesestadoslocalidadesapi"> 
    <strong>GetPaisesEstadosLocalidadesAPI</strong>
  </a> y <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getpaisesestadoslocalidadesapi"> 
    <strong>GetPaisesEstadosLocalidadesAPI</strong>
  </a> usando el id de estado en el payload

#### obtenerSubmetodos

Consulta el endpint <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#postcatalogosubmetodosrefacto"> 
    <strong>PostCatalogoSubMetodosRefacto</strong>
  </a> y <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getdetallescatalogoapi"> 
    <strong>GetDetallesCatalogoAPI</strong>
  </a> que inicializa los conceptos de un producto. También consulta el endpoint con los periodos generales  <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#getperiodospagometodo"> 
    <strong>GetPeriodosPagoMetodo</strong>
  </a>  una vez se haya validado que no se trata de un revolvente

#### assign_block_reports

Consulta el endpint <a href="../../../../../desarrollo/sofom/backend/funciones/catalogos/#postassignblockreportsdocuments"> 
    <strong>PostAssignBlockReportsDocuments</strong>
  </a> con la selección de documentos y el id del producto registrado para guardar su relación

#### GuardarProductoAPI

Esta función se encarga del guardado de productos y todas sus dependencias, inicalmente prepara un payload con la data principal del producto y la envía al endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postproductapi"> 
    <strong>PostProductAPI</strong>
  </a> para guardarlo y obtener el id del registro. Una vez hecho esto se consulta el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postmetodocalculoproductoapi"> 
    <strong>PostMetodoCalculoProductoAPI</strong>
  </a> para guardar el método y submétodo de calculo.
Se consulta el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postproductdetdelapi"> 
    <strong>PostProductDetDelAPI</strong>
  </a> para eliminar los conceptos relacionados al producto en caso de existir para después consultar el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postdetalleproductapi"> 
    <strong>PostDetalleProductAPI</strong>
  </a> para guardar los nuevos conceptos. El siguiente paso es usar la función <a href="#assign_block_reports"> 
    <strong>assign_block_reports</strong>
  </a> para el guardado de los documentos seleccionados para el producto.
  
Continua el proceso con una validación de cedente, si es que hay un cedente y su régimen fiscal, en caso de existir y ser PF se consulta el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postdomiciliocedenteapi"> 
    <strong>PostDomicilioCedenteAPI</strong>
  </a> enviando el payload requerido del domicilio del cedente, después, se procede a guardar la información del cedente en el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postpersonafisicaapi"> 
    <strong>PostPersonaFisicaAPI</strong>
  </a>, se elimina cualquier relación con documentos consultando el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postdeldocumentcedentapi"> 
    <strong>PostDelDocumentCedentAPI</strong>
  </a> y se crea una nueva relación entre documentos y cedente en el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postinsertdocumentcedentapi"> 
    <strong>PostInsertDocumentCedentAPI</strong>
  </a>. 
Finalmente se guarda <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postcreacedentebanco"> 
    <strong>PostCreaCedenteBanco</strong>
  </a>  o actualiza <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postactualizacedentebanco"> 
    <strong>PostActualizaCedenteBanco</strong>
  </a>  en caso de ya contar con un banco de cedente
Para cedentes PM, el proceso es similar, solo cambia el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postpersonamoralapi"> 
    <strong>PostPersonaMoralAPI</strong>
  </a> para el guardado de los datos propios del cedente

#### EditarProductoAPI

Esta función se encarga de actualizar productos y todas sus dependencias, inicalmente prepara un payload con la data principal del producto y la envía al endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postproductapi"> 
    <strong>PostProductAPI</strong>
  </a> para actualizarlo. Una vez hecho esto se consulta el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#updatemetodocalculoproductoapi"> 
    <strong>UpdateMetodoCalculoProductoAPI</strong>
  </a> para actualizar el método y submétodo de calculo.
Se consulta el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postproductdetdelapi"> 
    <strong>PostProductDetDelAPI</strong>
  </a> para eliminar los conceptos relacionados al producto en caso de existir para después consultar el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postdetalleproductapi"> 
    <strong>PostDetalleProductAPI</strong>
  </a> para guardar los nuevos conceptos. El siguiente paso es usar la función <a href="#assign_block_reports"> 
    <strong>assign_block_reports</strong>
  </a> para la actualización de los documentos seleccionados para el producto.
  
Continua el proceso con una validación de cedente, si es que hay un cedente y su régimen fiscal, en caso de existir y ser PF se consulta el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postdomiciliocedenteapi"> 
    <strong>PostDomicilioCedenteAPI</strong>
  </a> enviando el payload requerido del domicilio del cedente, después, se procede a guardar la información del cedente en el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postpersonafisicaapi"> 
    <strong>PostPersonaFisicaAPI</strong>
  </a>, se elimina cualquier relación con documentos consultando el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postdeldocumentcedentapi"> 
    <strong>PostDelDocumentCedentAPI</strong>
  </a> y se crea una nueva relación entre documentos y cedente en el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postinsertdocumentcedentapi"> 
    <strong>PostInsertDocumentCedentAPI</strong>
  </a>. 
Finalmente se guarda <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postcreacedentebanco"> 
    <strong>PostCreaCedenteBanco</strong>
  </a>  o actualiza <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postactualizacedentebanco"> 
    <strong>PostActualizaCedenteBanco</strong>
  </a>  en caso de ya contar con un banco de cedente
Para cedentes PM, el proceso es similar, solo cambia el endpoint <a href="../../../../../desarrollo/sofom/backend/funciones/productos/#postpersonamoralapi"> 
    <strong>PostPersonaMoralAPI</strong>
  </a> para el guardado de los datos propios del cedente