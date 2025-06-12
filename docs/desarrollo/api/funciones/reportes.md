## ARCHIVO CRUD reportes_implementation.py

### Funciones
#### get_block_reports_documents

Prepara el payload añadiendo la clave section_key = PRD, luego obtiene 6 nodos, tres son para los 3 tipos de catálogos: documentos, documento genéricos y reporte y los otros tres son para los tipos de catálogos relacionados directamente con el id del producto en caso de que exista relación

``` json title="Payload de entrada"
{
    id_producto: 1,
}
```
#### assign_block_reports_documents

Registra la relación entre cada tipo de reporte y el producto usando su id en la tabla <a href="../../../../../sistema/direccion/direccion/#generalproducto"> 
    <strong>DIRECCION.Tb_ProductoReporte</strong>
  </a>
``` json title="Payload de entrada"
{
    "section_key": "PRD",
    "product_id": 1,
    "cpr_selection": [],
    "opr_selection": [],
    "pd_selection": []
}
```