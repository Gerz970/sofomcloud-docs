``` SQL title="l"
create procedure GENERAL.Sp_ProductoDocumentos_Ins 
(
   
	@id_producto INT,
	@id_documento_digitalizado INT,
	@id_usuario_actualiza INT
	

)
as
/*
-------------------------------------------------------------------------
Informacion del Objeto: GENERAL.Sp_ProductoDocumentos_Ins
                   Abreviacion    Nombre Completo
                  -------------   ------------------------------------
Base de Datos:     [Bd]           SOFOM
Negocio:           [Neg]          dbo
Entidad:           [Entidad]      general.Sp_ProductoDocumentos_Ins
Accion:            [_Acc]         insercion
-------------------------------------------------------------------------------------------------------------------------------
Funcion:
> Se insertan los documentos del producto
-------------------------------------------------------------------------------------------------------------------------------
Modificaciones:
NÃƒÂºm.  Fecha         SSO        Autor           DescripciÃƒÂ³n
----  -----------   ---------  -------------   --------------------------------------------------------------------------------
> 01  20 MAR 2022   MVERDIN		MILAGROS VERDIN 	Creacion
*/

BEGIN 

SET NOCOUNT ON



	insert INTO  GENERAL.ProductoDocumento
	(
	  
	id_producto,
	id_documento_digitalizado,
	id_usuario_actualiza,
	fecha_actualiza
	)
	values 
	(
	  
	@id_producto,
	@id_documento_digitalizado,
	@id_usuario_actualiza
	,GETDATE()
	
	
	)
END
```