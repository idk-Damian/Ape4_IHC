# Criterios de aceptación de las correcciones

| ID | Antes V0 | Después V1 | Comprobación definida |
| --- | --- | --- | --- |
| H1 | Selector sin estado inválido representado. | E09 explica entero mínimo 1 y deshabilita agregar. | 0 bloquea agregar; 1 recupera subtotal $1,50. |
| H2 | Quitar sin confirmación visible. | E13 identifica sanduche y ofrece cancelar. | Cancelar mantiene el pedido; confirmar retira solo la línea. |
| H3 | Confirmar sin procesamiento representado. | E16 muestra envío y confirma deshabilitado. | No hay doble envío; éxito conserva importes. |

La presencia visual está documentada. Los resultados de ejecución corresponden a criterios y a la reevaluación simulada, no a pruebas en vivo.
