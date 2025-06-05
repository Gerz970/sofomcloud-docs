## ARCHIVO CRUD locations.py
### Funciones
#### get_payment_period_method

Prepara el payload recibido para ejecutar el SP GENERAL.Sp_PeriodoPagoMetodo_Obt que obtiene los registros filtrados por el método de calculo de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductometodoscalculo"> 
    <strong>GENERAL.PeriodoPago</strong>
  </a>.
  
``` json title="Payload de entrada"
{
    "method_key": "arrendamiento"
}
```
#### get_payment_periods

Obtiene todos los registros de la tabla <a href="../../../../../sistema/direccion/direccion/#generalproductometodoscalculo"> 
    <strong>GENERAL.PeriodoPago</strong>
  </a>. 