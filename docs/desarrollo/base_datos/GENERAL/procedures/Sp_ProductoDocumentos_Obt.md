``` SQL title="l"
CREATE  procedure GENERAL.Sp_ProductoDocumentos_Obt
(
	@id_producto int 
	
)
as
/*
-------------------------------------------------------------------------
Informacion del Objeto: GENERAL.Sp_ProductoDocumentos_Obt
                   Abreviacion    Nombre Completo
                  -------------   ------------------------------------
Base de Datos:     [Bd]           SOFOM
Negocio:           [Neg]          dbo
Entidad:           [Entidad]      GENERAL.Sp_ProductoDocumentos_Obt
Accion:            [_Acc]         Consulta
-------------------------------------------------------------------------------------------------------------------------------
Funcion:
> Se obtienen los documentos asignados al producto
-------------------------------------------------------------------------------------------------------------------------------
Modificaciones:
Num.  Fecha         SSO        Autor           Descripcion
----  -----------   ---------  -------------   --------------------------------------------------------------------------------
> 01  20 MAR 2022  MVERDIN	   MILAGROS VERDIN		Creacion
*/

BEGIN 

SET NOCOUNT ON
	
	
	
  SELECT
   productodoc.id_producto_documento
	, productodoc.id_producto
	, productodoc.id_documento_digitalizado
	, documento.descripcion
	, productodoc.forzoso
	, productodoc.valor
	, productodoc.orden
	, productodoc.id_estatus
	, productodoc.id_usuario_actualiza
	, productodoc.fecha_actualiza
	
	
FROM GENERAL.ProductoDocumento AS productodoc
INNER JOIN GENERAL.DocumentoDigitalizado AS documento ON productodoc.id_documento_digitalizado = documento.id_documento_digitalizado

		where  productodoc.id_producto = @id_producto
		
		
end
```