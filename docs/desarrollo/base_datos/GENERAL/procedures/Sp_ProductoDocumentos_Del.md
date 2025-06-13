``` SQL title="l"
CREATE  procedure GENERAL.Sp_ProductoDocumentos_Del
(
	@id_producto int 

)
as
/*
-------------------------------------------------------------------------
Informacion del Objeto: general.Sp_ProductoDocumentos_Del
                   Abreviacion    Nombre Completo
                  -------------   ------------------------------------
Base de Datos:     [Bd]           SOFOM
Negocio:           [Neg]          dbo
Entidad:           [Entidad]      general.Sp_ProductoDocumentos_Del
Accion:            [_Acc]         DELETE
-------------------------------------------------------------------------------------------------------------------------------
Funcion:
> eliminar los documentos del producto
-------------------------------------------------------------------------------------------------------------------------------
Modificaciones:
NÃƒÂºm.  Fecha         SSO        Autor           DescripciÃƒÂ³n
----  -----------   ---------  -------------   --------------------------------------------------------------------------------
> 01  20 MAR 2022  MVERDIN     MILAGROS VERDIN		Creacion
*/

BEGIN 

SET NOCOUNT ON

	declare @id_documento_digitalizado int 
   
	begin 
	select @id_documento_digitalizado = id_documento_digitalizado from GENERAL.ProductoDocumento where id_producto = @id_producto
	end 
	
   
	
	delete  from  GENERAL.ProductoDocumento where id_producto = @id_producto 
end
```