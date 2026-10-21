# Hallazgos y mejoras de la simulación

Los hallazgos se modelan sobre V0 y se contrastan con soluciones ya visibles en V1.

| ID | Prioridad | Hallazgo V0 | Registro | Solución V1 | Evidencia |
| --- | --- | --- | --- | --- | --- |
| H1 | Alta | V0 no representa orientación junto a una cantidad inválida. | U2 T1 | Mensaje de entero mínimo 1 y acción Agregar deshabilitada. | E09 y E03 |
| H2 | Media | V0 muestra Quitar sin confirmación visible. | U1 T2 y U2 T2 | Modal que identifica el sanduche y permite cancelar o quitar. | E13 |
| H3 | Media | V0 no representa el intervalo entre confirmar y recibir éxito. | U1 T1 | Mensaje Enviando tu pedido, indicador y confirmación deshabilitada. | E16 y E06 |

## Recomendaciones

1. Mantener la validación junto al campo y recuperar el estado válido al corregir.
2. Identificar el producto en la confirmación de eliminación y conservarlo al cancelar.
3. Comunicar procesamiento y evitar confirmación duplicada.
4. Como mejora adicional, bloquear edición y cambios de carrito durante el envío: en E16 Editar pedido y Seguir comprando conservan apariencia activa. Esta recomendación no se presenta como aplicada.

Las tres soluciones principales están representadas visualmente; los efectos de los controles requieren prueba interactiva. Las comparativas PNG están en comparativas/mejoras.
