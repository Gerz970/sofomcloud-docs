``` SQL title="l"
CREATE procedure GENERAL.Sp_Productos_Obt 
(
    @id_empresa INT,
	@id_estatus INT
	 
)
as
/*
  use uno
  drop procedure GENERAL.Sp_Productos_Obt
(
  -------------------------------------------------------------------------
  Informacion del Objeto: GENERAL.Sp_Productos_Obt
  
                     Abreviacion    Nombre Completo
                    -------------   ------------------------------------
  Base de Datos:     [Bd]           SOFOM
  Negocio:           [Neg]          PRODUCTO
  Entidad:           [Entidad]      GENERAL.Sp_Productos_Obt
  Accion:            [_Acc]         Consultar
  -------------------------------------------------------------------------------------------------------------------------------
  Funcion:
  > Proceso que obtiene los productos de cada empresa mediante el id_estatus
   
  -------------------------------------------------------------------------------------------------------------------------------
  Modificaciones:
  Num.  Fecha         SSO        Autor           Descripcion
  ----  -----------   ---------  -------------   --------------------------------------------------------------------------------
  > 01  29 Mar 2022   MVERDIN	 Milagros Verdin	 Creacion
  > 02	22 Mar 2024	  4bytes	 Yahir			 Se agrego dos subconsultas para traer el tipo de producto (amortizado o saldo insoluto) y para ver si pertenece a OB
*/
begin 
	SET NOCOUNT ON;
  	
  	DECLARE @id_metodoCalculo INT
	DECLARE @id_submetodoCalculo INT
	
	SELECT @id_metodoCalculo = id_metodo_calculo FROM GENERAL.MetodoCalculo WHERE descripcion = 'AMORTIZADO'
	SELECT @id_submetodoCalculo = id_submetodo_calculo FROM GENERAL.SubmetodoCalculo WHERE descripcion = 'SALDOS INSOLUTOS'
   
    SELECT
	id_producto
	, producto.id_producto_catalogo
	,ProductoCatalogo.producto AS descripcionProductoCatalogo
	, producto.producto
	, producto.id_empresa
	,empresa.nombre_comun AS empresa
	, producto.id_linea_fondeo
	,linea.clave
	,linea.descripcion AS descripcionLinea
	, reca
	, tasa_anual
	, fact_seguro
	, comision
	, cat
	, garantia_liquida
	, tasa_fija
	, causa_moratorios
	, moratorios
	, causa_gastos_cobranza
	, gastos_cobranza
	, iva
	, producto.id_estatus
	, producto.id_usuario_actualiza
	, producto.fecha_actualiza
	, tipo_pago_anticipado
	, id_moneda
	, id_instrumento_monetario
	, id_regimen_fiscal
	, id_nacionalidad
	, seguro
	, descripcion_seguro
	, aseguradora
	, clausula_seguro
	, advertencia_seguro
	, estado_cuenta
	, id_tipo_aplicacion_pago
	, factoraje
	, tasa_variable
	, id_regimen_fiscal_cedente
	, (CASE WHEN producto.id_producto IN (SELECT p.id_producto FROM GENERAL.Producto p
		INNER JOIN GENERAL.ProductoMetodosCalculo pmc ON producto.id_producto = pmc.id_producto
		INNER JOIN GENERAL.MetodoCalculo mc ON PMC.id_metodo_calculo = MC.id_metodo_calculo
		INNER JOIN GENERAL.SubmetodoCalculo smc on pmc.id_submetodo_calculo = smc.id_submetodo_calculo
		WHERE mc.id_metodo_calculo = @id_metodoCalculo AND smc.id_submetodo_calculo = @id_submetodoCalculo AND (producto.arrendamientop IS NULL or producto.arrendamientop = 0) and (producto.arrendamientof = 0 or producto.arrendamientof IS NULL) and (producto.factoraje = 0 or producto.factoraje IS NULL))
 	  THEN 1 ELSE 0 
 	  END) AS es_onboarding,
 	  (CASE WHEN producto.id_producto IN (SELECT p.id_producto FROM GENERAL.Producto p
 	   INNER JOIN ONBOARDING.tb_simulacion s ON s.id_producto_ob = p.id_producto)
 	   THEN 1 ELSE 0
 	   END) AS ob_configurado
 	  
	
	
	
FROM GENERAL.Producto  AS producto INNER JOIN GENERAL.LineaFondeo AS linea on producto.id_linea_fondeo = linea.id_linea_fondeo 
INNER JOIN GENERAL.ProductoCatalogo AS ProductoCatalogo ON producto.id_producto_catalogo = ProductoCatalogo.id_producto_catalogo
INNER JOIN GENERAL.Empresa AS empresa ON producto.id_empresa = empresa.id_empresa
 WHERE producto.id_empresa = @id_empresa  AND producto.id_estatus = @id_estatus

  
    
end
```