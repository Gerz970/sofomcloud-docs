| Nombre de Columna    | Tipo de Dato | Longitud / Precisión | Permite Nulo | Descripción                                  |
| -------------------- | ------------ | -------------------- | ------------ | -------------------------------------------- |
| id_metodo_calculo    | INT          | —                    | NO           | Clave primaria del método de cálculo         |
| clave                | NVARCHAR     | 50                   | SÍ           | Clave o identificador corto del método       |
| descripcion          | NVARCHAR     | 50                   | SÍ           | Descripción del método de cálculo            |
| id_estatus           | INT          | —                    | SÍ           | Estado del método (activo/inactivo)          |
| id_usuario_actualiza | INT          | —                    | SÍ           | Usuario que realizó la última actualización  |
| fecha_actualiza      | DATETIME     | —                    | SÍ           | Fecha de la última modificación del registro |