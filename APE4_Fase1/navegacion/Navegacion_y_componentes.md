# Navegación y componentes de CaféU

La navegación principal se apoya en Ver menú y Mi pedido. Todo, Bebidas y Comida filtran los productos dentro del catálogo. Los retornos permiten continuar la consulta sin perder la selección.

## Esquema de navegación

| Origen | Control o acción | Destino y comportamiento previsto |
| --- | --- | --- |
| P1 Inicio | Ver menú | P2 Menú; comenzar la consulta del catálogo. |
| P1, P2 y P3 | Mi pedido | P4 Revisión; consultar la selección acumulada. |
| P2 Menú | Volver al inicio | P1 Inicio; conservar el pedido existente. |
| P2 Menú | Buscar y filtrar | P2 Menú; actualizar los productos visibles. |
| P2 Menú | Ver detalle | P3 Detalle del producto seleccionado. |
| P3 Detalle | Volver al menú | P2 Menú; continuar consultando opciones. |
| P3 Detalle | Agregar al pedido | P4 Revisión; incorporar las unidades elegidas. |
| P4 Revisión | Seguir comprando | P2 Menú; mantener los productos ya seleccionados. |
| P4 Revisión | Editar pedido | P5 Edición; conservar las líneas y sus cantidades. |
| P4 Revisión | Confirmar pedido | P6 Confirmación cuando se recibe el pedido. |
| P5 Edición | Agregar otro producto | P2 Menú; agregar una opción a la selección existente. |
| P5 Edición | Guardar cambios y revisar | P4 Revisión; mostrar las cantidades y el total actualizados. |
| P5 Edición | Volver a mi pedido | P4 Revisión; volver a comprobar el estado actual del pedido. |

En Edición se especifica actualización inmediata del total al modificar cantidades o quitar productos. Guardar cambios y revisar consolida ese estado y abre el resumen.

## Componentes reutilizables

| Componente | Aplicación | Función y criterio de reutilización |
| --- | --- | --- |
| Encabezado y título | P1 a P6 | Identificar CaféU o la tarea actual con ubicación reconocible. |
| Acceso Mi pedido | P1 a P5 | Mostrar las unidades y mantener una ruta directa a Revisión. |
| Menú de categorías | P2 | Usar Todo, Bebidas y Comida para filtrar dentro del catálogo. |
| Campo de búsqueda | P2 | Permitir localizar productos por texto con una etiqueta comprensible. |
| Tarjeta de producto | P2 | Agrupar imagen, nombre, precio y Ver detalle; repetir la estructura para café y sanduche. |
| Formulario de selección | P3 y P5 | Reunir cantidad, precio y acciones del producto sin solicitar datos innecesarios. |
| Selector de cantidad | P3 y P5 | Reutilizar los controles menos, cantidad y más junto a cada producto. |
| Botones de acción | P1, P3, P4 y P5 | Distinguir la acción de avance con textos como Agregar o Confirmar pedido. |
| Enlaces de retorno | P2 a P5 | Mantener etiquetas que explican el destino y conservan la selección. |
| Línea y resumen del pedido | P4, P5 y P6 | Mostrar producto, cantidad e importe con la misma relación visual. |
| Mensajes de estado | P5 y P6 | Informar la actualización del total y la recepción; extender el patrón a avisos de error. |

## Justificación de usabilidad

| Criterio | Aplicación en CaféU |
| --- | --- |
| Claridad y jerarquía | Los títulos identifican la tarea; los productos se agrupan y el total se presenta antes de confirmar. |
| Consistencia | Se mantienen nombres, precios y controles similares en catálogo, edición y confirmación. |
| Lenguaje familiar | Menú, Mi pedido, Quitar y Confirmar pedido describen acciones del contexto de una cafetería. |
| Control del usuario | Editar pedido y los retornos permiten corregir la selección antes del envío. |
| Reconocimiento | Productos, cantidades e importes permanecen visibles para reducir lo que el usuario debe recordar. |
| Retroalimentación | Mi pedido muestra unidades y P6 comunica la recepción con mensaje, número y resumen. |
| Simplicidad y agrupación | La escala de grises y la proximidad entre nombre, precio y acción centran la atención en la tarea. |

## Errores y alternativas previstas

| Situación prevista | Respuesta de la interfaz | Continuación de la tarea |
| --- | --- | --- |
| Cantidad no válida | Mantener unidades enteras positivas y evitar disminuir por debajo de una unidad. | Usar Quitar para retirar el producto en P5. |
| Pedido vacío | Informar que debe agregarse al menos un producto. | Volver a P2 y seleccionar una opción. |
| Búsqueda sin coincidencias | Mostrar un aviso y conservar la posibilidad de cambiar la búsqueda o el filtro. | Permanecer en P2 y consultar otras opciones. |
| Error de envío | Indicar que no se recibió el pedido y conservar los productos. | Reintentar desde P4 sin duplicar una recepción confirmada. |

Los estados de error constituyen una especificación de comportamiento. Las capturas de Figma representan el recorrido normal y no son evidencias de ejecución de esos estados.
