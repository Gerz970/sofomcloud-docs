## ARCHIVO CRUD risk_levels.py

### Funciones
#### get_producto_impacto

Prepara el payload y ejecuta el SP RIESGOS.Sp_ProductoImpacto_Obt que consulta los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>RIESGOS.Tb_Historial_Impacto_Producto </strong>
  </a> unida a <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>RIESGOS.Producto_Impacto_CONDUSEF </strong>
  </a>, si   <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>RIESGOS.Tb_Historial_Impacto_Producto</strong>
  </a> no retorna al filtrar por año de ejercicio (año 0 = año más reciente en <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>RIESGOS.Producto_Impacto_CONDUSEF </strong>
  </a>) lo consulta de <a href="../../../../../sistema/direccion/direccion/#generalproductodetalle"> 
    <strong>RIESGOS.Producto_Impacto_CONDUSEF </strong>
  </a>

``` json title="Payload de entrada"
{
    anio: 0,
}
```
