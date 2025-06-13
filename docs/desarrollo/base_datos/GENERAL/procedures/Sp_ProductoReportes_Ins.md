``` SQL title="l"
CREATE procedure GENERAL.Sp_ProductoReportes_Ins 
(
   
   @id_producto INT
	, @id_reporte INT
	, @id_usuario_actualiza INT

)
as
/*
-------------------------------------------------------------------------
Informacion del Objeto: general.Sp_ProductoReportes_Ins 
                   Abreviacion    Nombre Completo
                  -------------   ------------------------------------
Base de Datos:     [Bd]           SOFOM
Negocio:           [Neg]          dbo
Entidad:           [Entidad]      general.Sp_ProductoReportes_Ins 
Accion:            [_Acc]         insercion
-------------------------------------------------------------------------------------------------------------------------------
Funcion:
> Se insertan los reportes del producto
-------------------------------------------------------------------------------------------------------------------------------
Modificaciones:
NÃƒÂºm.  Fecha         SSO        Autor           DescripciÃƒÂ³n
----  -----------   ---------  -------------   --------------------------------------------------------------------------------
> 01  20 MAR 2022    MVERDIN	MILAGROS VERDIN		Creacion
*/

BEGIN 

SET NOCOUNT ON


INSERT INTO GENERAL.ProductoReporte
	(
   	id_producto
	, id_reporte
	, id_usuario_actualiza
	, fecha_actualiza
	)
VALUES
	(
	  @id_producto
	, @id_reporte
	, @id_usuario_actualiza
	, GETDATE()
	
	)

END
```