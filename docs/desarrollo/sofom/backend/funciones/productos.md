## ARCHIVO CONTROLLER CatProductosController.cs
### Funciones

#### EliminaDetalle

Elimina la relación entre el producto y los conceptos registradas en la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>GENERAL.ProductoDetalle</strong>
  </a> usando el id_producto_detalle.

``` json title="Payload de entrada"
{
    "pID_Producto_Detalle": 1,
}
```

#### PostProductAPI

Crea una petición al endpoint  <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idproducto_ins"> 
    <strong>{platform_id}/empresas/{company_id}/producto_ins</strong>
  </a> del api, añadiendo a la consulta el payload recibido
#### PostMetodoCalculoProductoAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idpost_metodocalculo"> 
    <strong>{platform_id}/empresas/{company_id}/post_metodoCalculo</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### PostProductDetDelAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_iddetalle_producto_del"> 
    <strong>{platform_id}/empresas/{company_id}/detalle_producto_del</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### PostDeleteDocumentProductoAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_iddocumentos_producto_del"> 
    <strong>{platform_id}/empresas/{company_id}/documentos_producto_del</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### PostDetalleProductAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idpost_detalles_producto2"> 
    <strong>{platform_id}/empresas/{company_id}/post_detalles_producto2</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### PostDomicilioCedenteAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idpost_domicilio_cedente"> 
    <strong>{platform_id}/empresas/{company_id}/post_domicilio_cedente</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### PostPersonaFisicaAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idpost_cedente_fisico"> 
    <strong>{platform_id}/empresas/{company_id}/post_cedente_fisico</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### PostCreaCedenteBanco

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idcreate_ceding_bank"> 
    <strong>{platform_id}/empresas/{company_id}/create_ceding_bank</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### PostActualizaCedenteBanco

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idupdate_ceding_bank"> 
    <strong>{platform_id}/empresas/{company_id}/update_ceding_bank</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### PostDelDocumentCedentAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_iddocumentos_cedente_del"> 
    <strong>{platform_id}/empresas/{company_id}/documentos_cedente_del</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### PostInsertDocumentCedentAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_iddocumentos_cedente_ins"> 
    <strong>{platform_id}/empresas/{company_id}/documentos_cedente_ins</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### PostPersonaMoralAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idpost_cedente_moral"> 
    <strong>{platform_id}/empresas/{company_id}/post_cedente_moral</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### UpdateMetodoCalculoProductoAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idupdate_metodocalculo"> 
    <strong>{platform_id}/empresas/{company_id}/update_metodoCalculo</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### GetProductCatalogoAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idcatalogos_producto"> 
    <strong>{platform_id}/catalogos_producto</strong>
  </a> del api, añadiendo a la consulta el payload recibido
  
#### GetInstrumentosMonetariosAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idinstrumentos_monetarios"> 
    <strong>{platform_id}/instrumentos_monetarios</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### GetDetallesCatalogoAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idget_detalles_producto_catalogo"> 
    <strong>{platform_id}/get_detalles_producto_catalogo</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### GetTiposMedidaAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idtipos_medida"> 
    <strong>{platform_id}/tipos_medida</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### GetDocumentosCatalogConfigurationAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_iddocumentos_cedente"> 
    <strong>/{platform_id}/empresas/{company_id}/documentos_cedente</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### GetDocumentosDisponiblesAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idget_documentos"> 
    <strong>{platform_id}/get_documentos</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### PostCatalogoTiposMoratorioRevolvente

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idproductotipos_moratorio_revolvente"> 
    <strong>{platform_id}/producto/tipos_moratorio_revolvente</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### GetProductoGuardadoAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idget_detalles_producto_guardado"> 
    <strong>{platform_id}/empresas/{company_id}/get_detalles_producto_guardado</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### GetDetallesProductoAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idget_detalles_producto"> 
    <strong>{platform_id}/empresas/{company_id}/get_detalles_producto</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### GetMetodoCalculoProductoAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idget_metodocalculo_producto_guardado"> 
    <strong>{platform_id}/empresas/{company_id}/get_metodoCalculo_producto_guardado</strong>
  </a> del api, añadiendo a la consulta el payload recibido
  
#### GetDomicilioCedenteAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idget_domicilio_cedente"> 
    <strong>{platform_id}/empresas/{company_id}/get_domicilio_cedente</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### GetPersonaMoralAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idget_cedente_moral"> 
    <strong>{platform_id}/empresas/{company_id}/get_cedente_moral</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### GetCedenteBancoAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idget_ceding_bank"> 
    <strong>{platform_id}/empresas/{company_id}/get_ceding_bank</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### PostObtDocumentCedentAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_iddocumentos_cedente_obt"> 
    <strong>{platform_id}/empresas/{company_id}/documentos_cedente_obt</strong>
  </a> del api, añadiendo a la consulta el payload recibido

#### GetPersonaFisicaAPI

Crea una petición al endpoint <a href="../../../../../desarrollo/api/endpoints/productos/#platform_idempresascompany_idget_cedente_fisico"> 
    <strong>{platform_id}/empresas/{company_id}/get_cedente_fisico</strong>
  </a> del api, añadiendo a la consulta el payload recibido

