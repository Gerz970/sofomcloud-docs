| Campo | Tipo de Dato | Longitud | Clave Primaria | Obligatorio | Descripción |
| --- | --- | --- | --- | --- | --- |
| id_log | INT | N/A | Sí | Sí | Identificador único del log de cambios |
| id_registro | INT | N/A | No | No | ID del registro del concepto que fue modificado |
| tipo_evento | INT | N/A | No | No | Tipo de evento registrado (1=Alta, 2=Modificación, 3=Baja) |
| usuario | INT | N/A | No | No | ID del usuario que realizó el cambio |
| fecha | DATETIME | N/A | No | No | Fecha y hora en que ocurrió el evento |
| payload_inicial | NVARCHAR | MAX | No | No | Datos antes del cambio (JSON u objeto serializado) |
| payload_final | NVARCHAR | MAX | No | No | Datos después del cambio (JSON u objeto serializado) |