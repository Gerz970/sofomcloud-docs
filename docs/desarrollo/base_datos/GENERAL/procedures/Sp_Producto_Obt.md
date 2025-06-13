``` SQL title="l"
CREATE procedure GENERAL.Sp_Producto_Obt 
(
    @id_empresa INT,
	@id_producto INT
	 
)
as
/*
  use uno
  drop procedure GENERAL.Sp_Producto_Obt
(
  -------------------------------------------------------------------------
  Informacion del Objeto: GENERAL.Sp_Producto_Obt
  
                     Abreviacion    Nombre Completo
                    -------------   ------------------------------------
  Base de Datos:     [Bd]           SOFOM
  Negocio:           [Neg]          PRODUCTO
  Entidad:           [Entidad]      GENERAL.Sp_Producto_Obt
  Accion:            [_Acc]         Consultar
  -------------------------------------------------------------------------------------------------------------------------------
  Funcion:
  > Proceso que obtiene el producto getbyId
   
  -------------------------------------------------------------------------------------------------------------------------------
  Modificaciones:
  Num.  Fecha         SSO        Autor           Descripcion
  ----  -----------   ---------  -------------   --------------------------------------------------------------------------------
  > 01  29 Mar 2022   MVERDIN	 Milagros Verdin	 Creacion
*/
begin 
	SET NOCOUNT ON;
  
   
    SELECT
		producto.producto AS Producto,
		empresa.nombre_comun AS Empresa,
		linea.descripcion AS Linea_de_Fondeo,
		ProductoCatalogo.producto AS Tipo_de_credito,
        reca AS Reca,
        estatus.descripcion AS Estatus
	

	
FROM GENERAL.Producto  AS producto INNER JOIN GENERAL.LineaFondeo AS linea on producto.id_linea_fondeo = linea.id_linea_fondeo 
INNER JOIN GENERAL.ProductoCatalogo AS ProductoCatalogo ON producto.id_producto_catalogo = ProductoCatalogo.id_producto_catalogo
INNER JOIN GENERAL.Empresa AS empresa ON producto.id_empresa = empresa.id_empresa
INNER JOIN GENERAL.Estatus AS estatus ON producto.id_estatus = estatus.id_estatus

WHERE producto.id_empresa = @id_empresa  AND producto.id_producto = @id_producto

  
    
end
```