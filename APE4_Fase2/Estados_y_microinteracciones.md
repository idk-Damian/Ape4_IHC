# Estados feedback y microinteracciones

## Cuatro estados

- Inicial: E01 y E07, contador 0 y pedido vacío.
- Procesamiento: E16, Enviando tu pedido e indicador de carga.
- Error: E09, cantidad 0 y validación; E14, edición sin productos.
- Éxito: E06 y E17, CU-104 y resumen confirmado.

E11 es ausencia de coincidencias con recuperación por Limpiar búsqueda; no representa un error de envío. E14 no es la consecuencia directa de quitar solo el sanduche de E13: para quedar vacío también debe retirarse el café.

## Microinteracciones documentadas

| Código | Estados | Retroalimentación | Alcance |
| --- | --- | --- | --- |
| M1 Selección | E02 → E10 | Filtro Bebidas activo y catálogo reducido a café. | Cambio de estado visible; pulsación no verificada. |
| M2 Agregado | E03 → E12 | Mensaje Producto agregado, contador 1 y total $1,50. | Estados documentados; continuidad temporal no medida. |
| M3 Cantidad y guardado | E04 → E05 → E15 | Contador 2 a 3, total $4,25 a $5,75 y Cambios guardados. | Importes comprobados en capturas. |
| M4 Procesamiento | E04 → E16 → E06 | Envío en curso, confirmación deshabilitada y éxito. | Duración y animación no comprobadas. |
| M5 Eliminación | E13 | Apertura de modal con Quitar producto y Cancelar. | Apariencia visible; efectos de pulsaciones definidos. |

## Validación y accesibilidad

La cantidad debe ser entera desde 1 y la acción de agregar permanece deshabilitada mientras sea inválida. No se confirma un pedido vacío. Los mensajes acompañan iconos y color. Contraste, foco, lectura asistida y áreas táctiles requieren revisión interactiva; no se declara una auditoría normativa superada.
