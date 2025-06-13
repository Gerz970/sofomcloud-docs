``` SQL title="l"
CREATE procedure GENERAL.Sp_ProductoCatalogo_Obt 
/*
-------------------------------------------------------------------------
Informacion del Objeto: Sp_ProductoCatalogo_Obt
                   Abreviacion    Nombre Completo
                  -------------   ------------------------------------
Base de Datos:     [Bd]           SOFOM
Negocio:           [Neg]          dbo
Entidad:           [Entidad]      Sp_ProductoCatalogo_Obt
Accion:            [_Acc]         Consulta
-------------------------------------------------------------------------------------------------------------------------------
Funcion:
> Se obtienen los catalogos de los productos
-------------------------------------------------------------------------------------------------------------------------------
Modificaciones:
NÃƒÂºm.  Fecha         SSO        Autor           DescripciÃƒÂ³n
----  -----------   ---------  -------------   --------------------------------------------------------------------------------
01   23 MAR 2022    VERDIN		MILAGROS VERDIN 	creacion 
*/
as
BEGIN 

	SET NOCOUNT ON
	
	
	
	select 
		id_producto_catalogo
		, producto
		, id_estatus
		, id_usuario_actualiza
		, fecha_actualiza
		, id_producto_portal
		, clave_bc
		, tipo_credito
		, clave_cc
	from GENERAL.ProductoCatalogo WHERE id_estatus = 1 
	
	
end
```