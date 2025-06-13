``` SQL title="l"
CREATE procedure General.Sp_ProductoGuardado_Obt 
(
	@id_producto INT
)

as 
/*
  use uno
  drop procedure General.Sp_ProductoGuardado_Obt
(
  -------------------------------------------------------------------------
  Informacion del Objeto: General.Sp_ProductoGuardado_Obt
  
                     Abreviacion    Nombre Completo
                    -------------   ------------------------------------
  Base de Datos:     [Bd]           SOFOM
  Negocio:           [Neg]          producto
  Entidad:           [Entidad]      General.Sp_ProductoGuardado_Obt
  Accion:            [_Acc]         Insertar
  -------------------------------------------------------------------------------------------------------------------------------
  Funcion:
  > Proceso que obtiene el producto que ya esta guardado en la BD
  -------------------------------------------------------------------------------------------------------------------------------
  Modificaciones:
  Num.  Fecha         SSO        Autor           Descripcion
  ----  -----------   ---------  -------------   --------------------------------------------------------------------------------
  > 1  24 MARZO 2022   VERDIN	 Milagros verdin	 Creacion
  > 2  17 MAyo 2022    VERDIN	 Milagros verdin	 Se modifico el retorno de las columnas factoraje,tasa_variable,arrendamientop,arrendamientof para que regresen true o false en caso de ser NULL
  > 3  30 Ene 2023		AMINA						 Se agrego id_producto_condusef a la consulta 
  > 4  24 FEB 2023		4BYTES   EDI				SE AGREGO INFORMACIÃ“N SOBRE EL PAGO ANTICIPADO EN CONCEPTOS
  > 5  24 JUL 2023		4BYTES   AFONSECA			Se agrega funcionalidad de Tipo de Interes Moratorio para metodo Revolvente
  > 6  18 MAR 2024      4BYTES   CGPEREZ			Se aÃ±ade campo al insert del tipo automotriz
  
*/
begin 
	SET NOCOUNT ON;

SELECT
	  producto.id_producto
	, producto.id_producto_catalogo
	, producto.producto
	, producto.id_empresa
	, producto.id_linea_fondeo
	, producto.reca
	, producto.tasa_anual
	, producto.fact_seguro
	, producto.comision
	, producto.cat
	, producto.garantia_liquida
	, producto.tasa_fija
	, producto.causa_moratorios
	, producto.moratorios
	, producto.causa_gastos_cobranza
	, producto.gastos_cobranza
	, producto.iva
	, producto.tipo_pago_anticipado
	, producto.id_moneda
	, producto.id_instrumento_monetario
	, producto.id_regimen_fiscal
	, producto.id_nacionalidad
	, producto.seguro
	, producto.descripcion_seguro
	, producto.aseguradora
	, producto.clausula_seguro
	, producto.advertencia_seguro
	, producto.estado_cuenta
	, producto.id_tipo_aplicacion_pago
	, producto.id_regimen_fiscal_cedente
 
     , ISNULL(factoraje,0) AS factoraje 
	 , ISNULL(tasa_variable,0) AS tasa_variable 
   	 , ISNULL(arrendamientop,0) AS arrendamientop 
	 , ISNULL(arrendamientof,0) AS arrendamientof 
	 , coalesce(id_producto_condusef, 0) AS id_producto_condusef --#03
	
	,  ISNULL(producto.id_tipo_moratorio, 0) id_tipo_moratorio
	, producto.automotriz
FROM GENERAL.Producto AS producto 

	
         where 
			  producto.id_producto =  @id_producto
	 
		
	end
```