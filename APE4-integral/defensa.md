# Defensa del prototipo

## 1 Qué decisión cambió tras observar a los usuarios

P01 T2 vació la cantidad y no pudo recuperarla sin orientación; además creyó que los cambios estaban guardados. Se incorporaron Restablecer a 1 y mensajes de guardado manual y cambios pendientes. Se conservó la arquitectura de seis pantallas. La selección equivocada de P01 T1 motivó nombrar el producto en el acceso y el feedback.

## 2 Cómo se comunica el estado y se recuperan errores

El diseño diferencia edición, pendiente, guardado, espera, fallo y recibido. La cantidad inválida explica el formato y ofrece restablecer. La edición puede cancelarse; quitar y descartar requieren confirmar. Un fallo conserva la selección y ofrece reintentar o revisar. El comprobante comunica identificador y recibido, sin anunciar preparación terminada.

## 3 Cómo se identifica la contribución individual

Con enlaces del historial real a issues, ramas, commits y revisión de pull requests, relacionados con archivos concretos. El registro de moderación identifica a William Martínez en P01 y a Pablo Lozada en P02. [El registro de aportes](colaboracion/aportes.md) relaciona los integrantes con el contenido desarrollado y las áreas revisadas conforme al informe final. La evidencia Git se consulta en el historial real del repositorio.

## Secuencia de demostración

1. Abrir el menú y preparar un café y un sanduche por $4,25.
2. Editar, mostrar cero o vacío, recuperar el dato y dejar dos cafés y un sanduche por $5,75.
3. Explicar cambios pendientes y guardar. Mostrar la revisión con confirmación de guardado.
4. Demostrar procesamiento, fallo con selección conservada y confirmación en el escenario preparado. Explicar recibido frente a listo para retirar.
5. Iniciar otro pedido y mostrar selección vacía.
6. Abrir una comparación antes/después y relacionarla con el registro de prueba.
7. Cada integrante explica sus archivos y muestra sus enlaces reales de contribución.

Preparar el pedido base y el modificado como escenarios independientes; CU-104 por $4,25 y CU-104 por $5,75 son alternativas y no pedidos sucesivos.
