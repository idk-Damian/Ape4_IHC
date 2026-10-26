# Estados feedback y microinteracciones

| Estado | Respuesta | Evidencia |
| --- | --- | --- |
| Normal | Productos, cantidades e importes para decidir y revisar. | C02; C12; C15 |
| Error de cantidad | Regla de entero, campo señalado, importe no calculado y acción inactiva. | C09; C30 |
| Procesamiento | Enviando tu pedido, indicador de espera y acciones atenuadas. | C22; C24; C26 |
| Fallo recuperable | Selección conservada; Reintentar o Volver a revisar. | C23 |
| Éxito | Identificador, Recibido, detalle y siguiente acción. | C25; C27; C29 |

## Microinteracción principal

El cambio de cantidad se refleja en el subtotal: 1 café × $1,50 = $1,50; 2 cafés × $1,50 = $3,00. En el borrador, junto al sanduche, se representan 3 unidades y $5,75. Un café adicional produce 4 unidades y $7,25. La respuesta permite comprobar la consecuencia antes de guardar.

## Feedback complementario

- Categoría activa: nombre, marca y cambio de tratamiento visual.
- Búsqueda: foco visible, coincidencia o explicación sin resultados.
- Agregado: aviso con producto y cantidad.
- Edición: no hay guardado automático; cambios pendientes hasta guardar.
- Guardado: mensaje Cambios guardados al volver a revisión.
- Envío: espera, fallo con selección conservada o comprobante recibido.

## Conservación de datos

Buscar o filtrar no debe eliminar la selección. Un campo vacío no se trata como una cantidad válida. El borrador se mantiene separado del pedido guardado. Cancelar un modal conserva su estado previo. Un fallo de envío no confirma recepción ni vacía la selección. Hacer otro pedido genera una selección nueva, diferenciada del comprobante recibido.

Las capturas muestran la respuesta visual; el funcionamiento de los controles y la duración de las transiciones se comprueban en Figma.
