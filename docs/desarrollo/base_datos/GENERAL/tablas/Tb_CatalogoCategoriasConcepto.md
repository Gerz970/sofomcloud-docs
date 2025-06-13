| Campo | Tipo de dato | ¿Permite nulos? | Descripción |
| --- | --- | --- | --- |
| id_categoria | INT (IDENTITY) | NO | Identificador único de la categoría de concepto (clave primaria, auto incremental). |
| clave | VARCHAR(10) | SÍ | Clave corta o código identificador de la categoría. |
| nombre | VARCHAR(50) | SÍ | Nombre de la categoría de concepto. |
| descripcion | VARCHAR(500) | SÍ | Descripción detallada de la categoría. |
| orden_cobro | INT | NO | Orden secuencial para aplicar el cobro. Este campo es único en la tabla. |
| aplica_caracteristicas | INT | SÍ | Indicador o relación con características aplicables (posible FK o booleano). |
| fecha_actualiza | DATETIME | SÍ | Fecha de la última actualización. |
| id_estatus | INT | SÍ | Referencia al estatus de la categoría (activo/inactivo u otro). |