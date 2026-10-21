# Recorridos y controles

## Recorrido 1

Pedido vacío → Inicio → Menú → Detalle del café → Agregar 1 → Revisión $1,50 → Seguir comprando → Detalle del sanduche → Agregar 1 → Revisión $4,25 → Confirmar → Procesamiento → Confirmación CU-104.

Evidencias: E01, E02, E03, E12, E08, E04, E16 y E06. La secuencia conserva el pedido; E03 y E04 no son pasos consecutivos sin seleccionar el sanduche.

## Recorrido 2

Revisión de 1 café y 1 sanduche → Editar → Aumentar café a 2 → Total $5,75 → Guardar cambios y revisar → Revisión actualizada. Puede continuar hasta Confirmación por $5,75.

Evidencias: E04, E05, E15 y E17. Quitar abre un modal con confirmación; Cancelar lo cierra sin eliminar. Cancelar edición debe descartar el borrador; Guardar aplica los cambios.

## Reglas de consistencia

- Café $1,50 por unidad; sanduche $2,75 por unidad.
- 1 café + 1 sanduche = $4,25 y contador 2.
- 2 cafés + 1 sanduche = $5,75 y contador 3.
- Quitar el sanduche del pedido base deja 1 café y $1,50 como resultado esperado.
- Cantidad: entero desde 1. Pedido vacío: confirmar y guardar no disponibles.
- Enviar debe bloquear doble confirmación y cambios concurrentes del pedido.
- Hacer otro pedido debe iniciar una selección vacía.

Las capturas acreditan estados visibles, no ejecución de conexiones ni persistencia. En E16, Editar pedido y Seguir comprando conservan apariencia activa; se recomienda impedir cambios durante el envío.

[Abrir Figma](https://www.figma.com/design/ss4QSeSgvs6viguebi9r95/Sin-t%C3%ADtulo?node-id=0-1&t=pA8bATQ3rJBqZrOr-1)
