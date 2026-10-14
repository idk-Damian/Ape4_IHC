# Matriz de requisitos, usuarios y pantallas

CaféU atiende a un estudiante que necesita consultar productos y preparar un pedido durante su descanso. El diseño permite revisar la selección, corregirla y reconocer su recepción.

## Funcionalidades principales

| Funcionalidad principal | Necesidad del usuario | Pantallas necesarias |
| --- | --- | --- |
| F1 Consultar y seleccionar productos | Reconocer las opciones, comparar precios y elegir unidades. | P1 Inicio, P2 Menú y P3 Detalle. |
| F2 Revisar y modificar el pedido | Comprobar productos e importes y corregir la selección antes de enviarla. | P4 Revisión y P5 Edición. |
| F3 Confirmar y reconocer el resultado | Enviar lo revisado y saber que la cafetería recibió el pedido. | P4 Revisión y P6 Confirmación. |

## Requisitos funcionales

| Código | Requisito funcional | Usuario | Necesidad | Función y pantallas |
| --- | --- | --- | --- | --- |
| RF01 | Consultar productos disponibles con nombre y precio. | Estudiante | Elegir una opción con información suficiente. | F1 · P2 |
| RF02 | Buscar productos y filtrar por Todo, Bebidas o Comida. | Estudiante | Localizar una opción sin recorrer todo el listado. | F1 · P2 |
| RF03 | Revisar el detalle y seleccionar la cantidad de un producto. | Estudiante | Comprobar la elección y definir sus unidades. | F1 · P3 |
| RF04 | Agregar productos y revisar cantidades, importes y total. | Estudiante | Reconocer exactamente lo que se va a pedir. | F1 y F2 · P3, P4 |
| RF05 | Modificar cantidades o quitar productos antes de confirmar. | Estudiante | Corregir una selección sin empezar de nuevo. | F2 · P5, P4 |
| RF06 | Confirmar un pedido previamente revisado. | Estudiante | Enviar la selección con conocimiento del total. | F3 · P4, P6 |
| RF07 | Mostrar recepción, número de pedido y resumen confirmado. | Estudiante | Reconocer el resultado y conservar el identificador. | F3 · P6 |
| RF08 | Volver al catálogo o al pedido conservando la selección. | Estudiante | Continuar comprando o revisar sin perder lo elegido. | F1 y F2 · P1 a P5 |

## Identificación de pantallas

| Pantalla | Tipo | Función dentro de la estructura |
| --- | --- | --- |
| P1 Inicio | Principal | Presenta CaféU y ofrece el acceso al menú y al pedido. |
| P2 Menú | Principal | Agrupa el catálogo, la búsqueda, los filtros y los precios. |
| P3 Detalle del producto | Secundaria | Amplía un producto y permite seleccionar su cantidad. |
| P4 Revisión del pedido | Principal | Reúne la selección y permite decidir entre editar y confirmar. |
| P5 Edición del pedido | Secundaria | Permite corregir un pedido existente y volver a revisarlo. |
| P6 Confirmación | Principal | Comunica la recepción y muestra el identificador y el resumen. |

## Trazabilidad hacia los componentes

| Requisito | Pantallas | Componentes identificables | Recorrido |
| --- | --- | --- | --- |
| RF01 | P2 | Tarjetas, nombre del producto y precio. | Flujo 1: consultar el menú. |
| RF02 | P2 | Buscar productos y categorías. | Flujo 1: localizar la opción. |
| RF03 | P3 | Descripción, cantidad y precio unitario. | Flujo 1: revisar el detalle. |
| RF04 | P3, P4 | Agregar al pedido, líneas, importes y total. | Flujo 1: formar y revisar. |
| RF05 | P5, P4 | Selectores, Quitar y Guardar cambios y revisar. | Flujo 2: corregir y comprobar. |
| RF06 | P4, P6 | Confirmar pedido y mensaje de recepción. | Flujo 1: enviar y terminar. |
| RF07 | P6 | Pedido confirmado, CU-104 y resumen. | Flujo 1: reconocer el resultado. |
| RF08 | P1 a P5 | Mi pedido, retornos y Seguir comprando. | Ambos flujos: conservar la selección. |

## Reglas del escenario

- Café americano: $1,50 por unidad.
- Sanduche: $2,75 por unidad.
- Una unidad de cada producto: total de $4,25 y dos unidades en Mi pedido.
- El importe se calcula multiplicando el precio unitario por la cantidad; el total suma los importes.
- Las cantidades son enteras positivas y Quitar elimina una línea del pedido.
- Un pedido sin productos debe volver al menú antes de confirmarse.
- Los retornos al catálogo conservan la selección.

Los códigos P1 a P6 se mantienen en el sitemap, los recorridos y los wireframes.
