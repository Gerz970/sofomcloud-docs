``` SQL title="l"
CREATE  procedure GENERAL.Sp_DetallesProducto_Ins 
(
    
	 @id_producto INT
	, @id_producto_detalle_catalogo INT
	, @id_tipo_medida_parametro INT
	, @valor DECIMAL (18,4)
	, @orden VARCHAR(10)
	, @es_financiado INT
	, @id_estatus INT
	, @id_usuario_actualiza INT
	, @fecha_actualiza VARCHAR(10)
	, @permite_financiar INT
	, @pago_anticipado BIT
	, @calcula_iva INT
	, @interes_moratorio INT
	, @id_tasa_variable INT
	, @spread DECIMAL (18,4)
	, @prorrateado INT
	
   
)

as 
/*
  use uno
  drop procedure GENERAL.Sp_DetallesProducto_Ins
(
  -------------------------------------------------------------------------
  Informacion del Objeto: GENERAL.Sp_DetallesProducto_Ins
  
                     Abreviacion    Nombre Completo
                    -------------   ------------------------------------
  Base de Datos:     [Bd]           SOFOM
  Negocio:           [Neg]          producto
  Entidad:           [Entidad]      GENERAL.Sp_DetallesProducto_Ins
  Accion:            [_Acc]         Insertar
  -------------------------------------------------------------------------------------------------------------------------------
  Funcion:
  > Proceso que inserta los detalles del producto
  -------------------------------------------------------------------------------------------------------------------------------
  Modificaciones:
  Num.  Fecha         SSO        Autor           Descripcion
  ----  -----------   ---------  -------------   --------------------------------------------------------------------------------
  > 01  29 Mar 2022   MVERDIN	 Milagros Verdin	 Creacion
  > 02  09 Jun 2022   MVERDIN	 Milagros Verdin	 Modificacion, se agregaron correciones en los tipos de datos DECIMAL (18,4)
  > 03  02 FEB 2023	  4BYTES	 EDI				 SE AGREGO EL PAGO ANTICIPADO
*/
begin 
	SET NOCOUNT ON;

	   INSERT INTO GENERAL.ProductoDetalle
	(
    id_producto
	, id_producto_detalle_catalogo
	, id_tipo_medida_parametro
	, valor
	, orden
	, es_financiado
	, id_estatus
	, id_usuario_actualiza
	, fecha_actualiza 
	, permite_financiar
	, pago_anticipado
	, calcula_iva
	, interes_moratorio
	, id_tasa_variable
	, spread
	, prorrateado
	)
VALUES
	(
	@id_producto
	, @id_producto_detalle_catalogo
	, @id_tipo_medida_parametro
	, @valor
	, @orden
    , convert (BIT,@es_financiado)
	, @id_estatus
	, @id_usuario_actualiza
	, convert(DATE,@fecha_actualiza)
	, convert (BIT,@permite_financiar) 
	, @pago_anticipado
    , convert (BIT,@calcula_iva)
	, @interes_moratorio
	, @id_tasa_variable
	, @spread
	,@prorrateado
  
	)
	SELECT @@IDENTITY
	
end
```