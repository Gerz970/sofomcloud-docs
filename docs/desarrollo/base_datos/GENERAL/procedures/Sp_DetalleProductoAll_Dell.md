``` SQL title="l"
create procedure general.Sp_DetalleProductoAll_Del
(
	@id_producto int 
)
as
/*
-------------------------------------------------------------------------
Informacion del Objeto: Sp_DetalleProductoAll_Del
                   Abreviacion    Nombre Completo
                  -------------   ------------------------------------
Base de Datos:     [Bd]           SOFOM
Negocio:           [Neg]          dbo
Entidad:           [Entidad]      Sp_DetalleProductoAll_Del
Accion:            [_Acc]         Consulta
-------------------------------------------------------------------------------------------------------------------------------
Funcion:
> Se elimna el detalle del producto
-------------------------------------------------------------------------------------------------------------------------------
Modificaciones:
NÃƒÂºm.  Fecha         SSO        Autor           DescripciÃƒÂ³n
----  -----------   ---------  -------------   --------------------------------------------------------------------------------
> 01  20 MAR 2022   4BYTES00001  AMINA			Creacion
*/
begin 

	SET NOCOUNT ON
	
	delete from general.ProductoDetalle
	where id_producto = @id_producto
	
	
end
```