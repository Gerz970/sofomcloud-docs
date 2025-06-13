``` SQL title="l"
CREATE procedure GENERAL.Sp_producto_Ins 
(
      @id_producto int
    ,@id_producto_catalogo      INT 
	, @producto                  NVARCHAR (50) NULL
	, @id_empresa                INT NULL
	, @id_linea_fondeo           INT NULL
	, @reca                      NVARCHAR (50) NULL
	, @iva                       DECIMAL (18,0) NULL
	, @id_estatus                INT NULL
	, @id_usuario_actualiza      INT NULL
	, @tipo_pago_anticipado      INT NULL
	, @id_moneda                 INT NULL
	, @id_instrumento_monetario  INT NULL
	, @id_regimen_fiscal         INT NULL
	, @id_nacionalidad           INT NULL
	, @seguro                    BIT NULL
	, @descripcion_seguro        VARCHAR (300) NULL
	, @aseguradora               NVARCHAR (100) NULL
	, @clausula_seguro           NVARCHAR (100) NULL
	, @advertencia_seguro        NVARCHAR (100) NULL
	, @estado_cuenta             INT NULL
	, @id_tipo_aplicacion_pago   INT NULL
	, @factoraje                 BIT NULL
	, @tasa_variable             BIT NULL
	, @id_regimen_fiscal_cedente INT NULL
	, @arrendamientop             BIT NULL
	, @arrendamientof             BIT NULL
	, @id_producto_condusef		INT = 0 
	, @id_tipo_moratorio		INT = 0 
	, @automotriz				INT = 0
)

as 
/*
  use uno
  drop procedure GENERAL.Sp_producto_Ins
(
  -------------------------------------------------------------------------
  Informacion del Objeto: GENERAL.Sp_producto_Ins
  
                     Abreviacion    Nombre Completo
                    -------------   ------------------------------------
  Base de Datos:     [Bd]           SOFOM
  Negocio:           [Neg]          producto
  Entidad:           [Entidad]      GENERAL.Sp_producto_Ins
  Accion:            [_Acc]         Insertar
  -------------------------------------------------------------------------------------------------------------------------------
  Funcion:
  > Proceso que inserta el producto
  -------------------------------------------------------------------------------------------------------------------------------
  Modificaciones:
  Num.  Fecha         SSO        Autor           Descripcion
  ----  -----------   ---------  -------------   --------------------------------------------------------------------------------
  > 1  23 MARZO 2022   MVERDIN	 Milagros verdin	 Creacion
  > 2	30 Enero 2023	AMINA						Se agrego al guardado id_producto_condusef
  > 3 24 FEB 2023		4BYTES   EDI				SE AGREGO INFORMACIÃ“N SOBRE EL PAGO ANTICIPADO EN CONCEPTOS
  > 4 24 JUL 2023		4BYTES   AFONSECA			Se agrega el tipo de interes moratorio para credito revolvente (Tb_TipoMoratorioRevolvente)
  > 05 18 MAR 2024      4BYTES   CGPEREZ			Se aÃ±ade campo de tipo automotriz
*/
begin 
	SET NOCOUNT ON;
		 

	if @id_producto is null or  @id_producto= 0 
	begin 
	
	   INSERT INTO GENERAL.Producto
	(
	
	id_producto_catalogo
	, producto
	, id_empresa
	, id_linea_fondeo
	, reca
	, iva
	, id_estatus
	, id_usuario_actualiza
	, fecha_actualiza
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
	, arrendamientop
	, arrendamientof
	, id_producto_condusef
	, id_tipo_moratorio 
	, automotriz
	)
		values 
		(
	  @id_producto_catalogo
	, @producto
	, @id_empresa
	, @id_linea_fondeo
	, @reca
	, @iva
	, @id_estatus
	, @id_usuario_actualiza  
	, GETDATE()
	, @tipo_pago_anticipado
	, @id_moneda
	, @id_instrumento_monetario
	, @id_regimen_fiscal
	, @id_nacionalidad
	, @seguro
	, @descripcion_seguro
	, @aseguradora
	, @clausula_seguro
	, @advertencia_seguro
	, @estado_cuenta
	, @id_tipo_aplicacion_pago
	, @factoraje
	, @tasa_variable
	, @id_regimen_fiscal_cedente
	, @arrendamientop             
	, @arrendamientof 
	, @id_producto_condusef
	, @id_tipo_moratorio
	, @automotriz
		) 
		
		
		set @id_producto = @@IDENTITY
		
	   
		
	end 
	else 
	begin 
		update GENERAL.Producto 
	set 
	
   	
	id_producto_catalogo = @id_producto_catalogo
	, producto = @producto
	, id_empresa = @id_empresa
	, id_linea_fondeo = @id_linea_fondeo
	, reca = @reca
	, iva = @iva
	, id_estatus = @id_estatus
	, id_usuario_actualiza = @id_usuario_actualiza
	, fecha_actualiza =  getdate()
	, tipo_pago_anticipado = @tipo_pago_anticipado
	, id_moneda = @id_moneda
	, id_instrumento_monetario = @id_instrumento_monetario
	, id_regimen_fiscal = @id_regimen_fiscal
	, id_nacionalidad = @id_nacionalidad
	, seguro = @seguro
	, descripcion_seguro = @descripcion_seguro
	, aseguradora = @aseguradora
	, clausula_seguro = @clausula_seguro
	, advertencia_seguro = @advertencia_seguro
	, estado_cuenta = @estado_cuenta
	, id_tipo_aplicacion_pago = @id_tipo_aplicacion_pago
	, factoraje = @factoraje
	, tasa_variable = @tasa_variable
	, id_regimen_fiscal_cedente = @id_regimen_fiscal_cedente
    , arrendamientop = @arrendamientop
     ,arrendamientof = @arrendamientof
     ,id_producto_condusef = @id_producto_condusef
	, id_tipo_moratorio = @id_tipo_moratorio
	, automotriz = @automotriz
		where 
			id_producto = @id_producto
		
	end 
	
	
	select @id_producto id_producto
	
end
```