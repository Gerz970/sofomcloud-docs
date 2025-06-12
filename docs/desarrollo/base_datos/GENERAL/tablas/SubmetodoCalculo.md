| Nombre de Columna | Tipo de Dato | Longitud / Precisión | Permite Nulo | Valor por Defecto | Descripción |
| --- | --- | --- | --- | --- | --- |
| id_submetodo_calculo | INT | — | NO | — | Clave primaria del submetodo de cálculo |
| clave | NVARCHAR | 50 | SÍ | — | Clave corta identificadora del submetodo |
| descripcion | NVARCHAR | 50 | SÍ | — | Descripción del submetodo de cálculo |
| id_estatus | INT | — | SÍ | — | Estatus del registro |
| id_usuario_actualiza | INT | — | SÍ | — | Usuario que actualizó el registro |
| fecha_actualiza | DATETIME | — | SÍ | — | Fecha de última actualización |
| diasxanio | INT | — | NO | 360 | Número de días considerados por año para el cálculo |