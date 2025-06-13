``` SQL title="Payload de entrada"
CREATE procedure GENERAL.Sp_producto_Del 
(

@id_empresa INT,
@id_producto INT,
@id_usuario_actualiza INT


)

as 
/*
  use uno
  drop procedure GENERAL.Sp_producto_Del
(
  -------------------------------------------------------------------------
  Informacion del Objeto: GENERAL.Sp_producto_Del
  
                     Abreviacion    Nombre Completo
                    -------------   ------------------------------------
  Base de Datos:     [Bd]           SOFOM
  Negocio:           [Neg]          producto
  Entidad:           [Entidad]      GENERAL.Sp_producto_Del
  Accion:            [_Acc]         Insertar
  -------------------------------------------------------------------------------------------------------------------------------
  Funcion:
  > Proceso que inserta el producto
  -------------------------------------------------------------------------------------------------------------------------------
  Modificaciones:
  Num.  Fecha         SSO        Autor           Descripcion
  ----  -----------   ---------  -------------   --------------------------------------------------------------------------------
  > 1  24 MARZO 2022   MVERDIN	 Milagros verdin	 Creacion
  > 2  19 MAYO 2022   MVERDIN	 Milagros verdin	  Se agregÃ³ la validaciÃ³n para que no permitar el eliminado logico cuando el producto tiene asignado algun credito o solicitud
*/
BEGIN 
	SET NOCOUNT ON;
	DECLARE @id_solicitud INT
    DECLARE @id_simulador INT
    DECLARE @id_credito INT
    DECLARE @respuesta INT


   SET @id_solicitud = (SELECT COUNT(id_producto) FROM CREDITO.Solicitud WHERE id_producto = @id_producto)
--SELECT @id_solicitud

SET @id_simulador = (SELECT COUNT(id_producto) FROM SIMULADOR.Simulacion WHERE id_producto = @id_producto)
--SELECT @id_simulador


SET @id_credito = (SELECT COUNT(S.id_producto) FROM CREDITO.Solicitud AS S INNER JOIN CREDITOS.Credito AS C ON C.id_solicitud = S.id_solicitud
 WHERE S.id_producto = @id_producto)
--SELECT @id_credito 


IF(@id_solicitud >0 OR @id_simulador >0 OR @id_credito>0)
SET @respuesta = 1

ELSE
BEGIN
SET @respuesta = 0


		update GENERAL.Producto 
		set 
			
	 
	  id_estatus = 2
	, id_usuario_actualiza = @id_usuario_actualiza
	, fecha_actualiza = GETDATE()
	
	
		where 
			 id_empresa = @id_empresa AND id_producto = @id_producto

END


SELECT @respuesta AS respuesta
   
   
	 
		
	END
```