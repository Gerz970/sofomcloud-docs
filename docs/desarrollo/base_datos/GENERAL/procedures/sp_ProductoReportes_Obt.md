``` SQL title="l"
CREATE  procedure GENERAL.sp_ProductoReportes_Obt 
(
	@id_producto int 
	
)
as
/*
-------------------------------------------------------------------------
Informacion del Objeto: GENERAL.sp_ProductoReportes_Obt
                   Abreviacion    Nombre Completo
                  -------------   ------------------------------------
Base de Datos:     [Bd]           SOFOM
Negocio:           [Neg]          dbo
Entidad:           [Entidad]      GENERAL.sp_ProductoReportes_Obt
Accion:            [_Acc]         Consulta
-------------------------------------------------------------------------------------------------------------------------------
Funcion:
> Se obtienen los reportes asignados al producto
-------------------------------------------------------------------------------------------------------------------------------
Modificaciones:
Num.  Fecha         SSO        Autor           Descripcion
----  -----------   ---------  -------------   --------------------------------------------------------------------------------
> 01  20 MAR 2022   VERDIN	   MILAGROS VERDIN		Creacion
*/

BEGIN 

SET NOCOUNT ON
	
	
	SELECT
	  productoRep.id_producto_reporte
	, productoRep.id_producto
	, productoRep.id_reporte
	, reporte.descripcion
    , reporte.clave
	, productoRep.id_usuario_actualiza
	, productoRep.fecha_actualiza
   

	
	
       FROM GENERAL.ProductoReporte AS productoRep
       INNER JOIN GENERAL.Reporte  AS reporte ON productoRep.id_reporte = reporte.id_reporte

		where  productoRep.id_producto = @id_producto
		
		
end
```