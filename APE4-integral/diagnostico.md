# Diagnóstico de CaféU

## Usuario y necesidad

Estudiante universitario con un descanso breve que necesita reconocer productos y precios, preparar una selección, corregir equivocaciones y saber si la cafetería recibió el pedido. El alcance comprende selección, edición y confirmación. No incluye pago, autenticación, administración ni un estado de preparación terminada.

## Tres tareas

1. T1: localizar café americano y sanduche, agregar una unidad de cada uno y revisar 2 unidades por $4,25.
2. T2: editar el pedido base, comprobar una cantidad inválida y terminar con dos cafés y un sanduche por $5,75.
3. T3: enviar un pedido base independiente de T2, reconocer CU-104 recibido e iniciar otra selección vacía.

[Enunciados y criterios completos](pruebas/protocolo.md).

## Requisitos de esta actividad

La siguiente matriz coincide con el apartado 2.7.2 del informe.

| Código | Necesidad y comportamiento | Pantalla | Evidencia |
| --- | --- | --- | --- |
| RF01 | Consultar productos con nombre y precio unitario. | P2 | C02–C04 |
| RF02 | Buscar y filtrar; recuperar el catálogo sin coincidencias. | P2 | C03–C06 |
| RF03 | Revisar el producto y definir una cantidad entera válida. | P3 | C07–C10 |
| RF04 | Agregar y revisar líneas, unidades y total antes del envío. | P3–P4 | C11–C13 |
| RF05 | Editar cantidades, quitar productos y guardar el borrador. | P5–P4 | C14–C21; C30–C33 |
| RF06 | Confirmar y mostrar procesamiento o fallo recuperable. | P4–P6 | C22–C24; C26 |
| RF07 | Mostrar identificador y estado de recepción. | P6 | C25; C27; C29 |
| RF08 | Volver al menú o al pedido conservando el contexto. | P1–P5 | C01; C20; C32–C33 |

## Revisión del wireframe

Se mantienen seis pantallas: Inicio, Menú, Detalle, Revisión, Edición y Confirmación. La construcción agrega estados y mensajes dentro de ellas: cantidad inválida, búsqueda vacía, borrador vacío, procesamiento y recuperación. Los [wireframes originales](wireframes/README.md) se incluyen como antecedentes del diseño.

## Cinco problemas priorizados

| ID | Nivel | Problema y evidencia | Decisión |
| --- | --- | --- | --- |
| D01 | Alta | P01 T2: vació la cantidad y no identificó cómo recuperar un dato válido. | K01: restablecer a 1 y validar junto al campo. |
| D02 | Alta | P01 T2: creyó que los cambios ya estaban guardados. | K02: distinguir edición, cambios pendientes y guardado. |
| D03 | Media | P01 T1: selección inicial incorrecta, recuperada en revisión; accesos genéricos. | K03: nombrar el producto en la acción y el feedback. |
| D04 | Media | P02 T2: incremento adicional del café, corregido sin ayuda. | K04: mostrar cantidad × precio y total del borrador. |
| D05 | Baja | Inspección: Mi pedido 0 en la confirmación puede confundirse con las unidades del comprobante. | Oportunidad de aclaración; sin fallo observado en T3 ni corrección específica acreditada. |

La prioridad considera el impacto en la tarea: D01 y D02 coincidieron en la ejecución que necesitó ayuda. D03 y D04 fueron recuperables. D05 procede de inspección, no de un error registrado. Introducir cero de forma deliberada en T2 no se contabiliza por sí mismo como error espontáneo.

## Reglas del escenario

- Café americano: $1,50 por unidad. Sanduche: $2,75 por unidad.
- La cantidad es un entero desde 1. El campo vacío o cero requiere corregirse.
- El contador expresa unidades; dos cafés y un sanduche suman 3 unidades, aunque existan dos líneas.
- Un pedido base vale $4,25; el modificado vale $5,75; tres cafés y un sanduche valen $7,25.
- La edición es provisional hasta guardar. Cancelar o descartar debe preservar el pedido guardado.
- No se confirma una selección vacía ni se guarda un borrador inválido.
- Recibido significa que la cafetería recibió la orden; no significa que esté lista para retirar.
