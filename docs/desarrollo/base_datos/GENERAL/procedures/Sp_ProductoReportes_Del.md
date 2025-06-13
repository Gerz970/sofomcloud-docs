``` SQL title="l"
create procedure GENERAL.Sp_ProductoReportes_Del
(
	@id_producto int 

)
as
/*
-------------------------------------------------------------------------
Informacion del Objeto: GENERAL.Sp_ProductoReportes_Del
                   Abreviacion    Nombre Completo
                  -------------   ------------------------------------
Base de Datos:     [Bd]           SOFOM
Negocio:           [Neg]          dbo
Entidad:           [Entidad]      GENERAL.Sp_ProductoReportes_Del
Accion:            [_Acc]         DELETE
-------------------------------------------------------------------------------------------------------------------------------
Funcion:
> eliminar los reportes del producto
-------------------------------------------------------------------------------------------------------------------------------
Modificaciones:
NÃƒÂºm.  Fecha         SSO        Autor           DescripciÃƒÂ³n
----  -----------   ---------  -------------   --------------------------------------------------------------------------------
> 01  20 MAR 2022   MVERDIN		 MILAGROS VERDIN	Creacion
*/

BEGIN 

SET NOCOUNT ON

	declare @id_producto_reporte int 
   
	begin 
	select @id_producto_reporte = id_producto_reporte from GENERAL.ProductoReporte where id_producto = @id_producto
	end 
	
   
	
	delete  from  GENERAL.ProductoReporte where id_producto = @id_producto 
end
```