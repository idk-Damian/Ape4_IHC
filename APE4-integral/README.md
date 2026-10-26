# APE 4 integral CaféU

Universidad Técnica de Ambato · FISEI · Carrera de Software  
Interacción Humano Computador · Quinto A · Grupo 6  
Ciclo académico julio–diciembre de 2026

CaféU permite consultar un menú, seleccionar productos, editar el pedido y reconocer su recepción. Esta actividad documenta seis pantallas principales, tres recorridos, pruebas con dos participantes y las correcciones resultantes.

## Accesos principales

- [Prototipo actual de Figma](https://www.figma.com/design/HQZqFztrL0HeQ6E9h60LZm/Sin-t%C3%ADtulo?node-id=0-1&t=jy5K6mJ05BjNvsxM-1)
- [Informe institucional en PDF](Docs/Guia_4_IHC_Grupo6.pdf)
- [Repositorio del proyecto](https://github.com/idk-Damian/Ape4_IHC)
- [Registro de aportes del equipo](colaboracion/aportes.md)

## Equipo

| Integrantes |
| --- |
| Abril Lara Emilio Alexander |
| Cusme Velez Manuel Steven |
| Gamboa Guaman Jonathan Alexis |
| Lozada Marcial Pablo Damian |
| Martínez Jiménez William Fernando |

## Recorrido de lectura

| Actividad | Archivos y evidencias |
| --- | --- |
| Diagnóstico | [Usuario, tareas, requisitos y cinco problemas](diagnostico.md) |
| Arquitectura | [Diseño visual](arquitectura.md), [sitemap](sitemap.png), [user flow](user-flow.png), [wireframes](wireframes/README.md) |
| Construcción | [Figma y alcance](prototipo/README.md), [recorridos](prototipo/recorridos.md), [estados y microinteracciones](prototipo/estados-y-microinteracciones.md) |
| Prueba | [Protocolo](pruebas/protocolo.md), [datos CSV](pruebas/resultados.csv), [resumen CSV](pruebas/resumen.csv), [comentarios](pruebas/observaciones.md), [hallazgos](pruebas/hallazgos.md) |
| Heurísticas y accesibilidad | [Tres heurísticas y dos condiciones](pruebas/heuristicas-accesibilidad.md) |
| Iteración | [Antes/después](iteracion/antes-despues.md), [cambios](cambios.md), [verificación](iteracion/verificacion.md) |
| Evidencias | [30 capturas iniciales y 33 corregidas](evidencias/README.md) |
| Cierre | [Objetivos, conclusiones y recomendaciones](conclusiones.md), [defensa](defensa.md) |
| Colaboración | [Registro de aportes](colaboracion/aportes.md) |

## Escenarios

- Pedido base: 1 café americano ($1,50) y 1 sanduche ($2,75) = 2 unidades, $4,25.
- Pedido modificado: 2 cafés y 1 sanduche = 3 unidades, $5,75.
- Incremento adicional: 3 cafés y 1 sanduche = 4 unidades, $7,25.
- Confirmación: CU-104 recibido; otra selección comienza vacía. Las variantes de CU-104 son alternativas de escenario, no envíos sucesivos.

## Resultados de la prueba inicial

| Tarea | Éxitos | Tasa | Promedio s | Errores | Con ayuda |
| --- | --- | --- | --- | --- | --- |
| T1 | 2 de 2 | 100,0 % | 59,0 | 1 | 0 |
| T2 | 1 de 2 | 50,0 % | 93,5 | 3 | 1 |
| T3 | 2 de 2 | 100,0 % | 46,5 | 0 | 0 |
| Global | 5 de 6 | 83,3 % | 66,3 | 4 | 1 |

Fecha: 24 de octubre de 2026. Dos participantes ajenos al diseño. La edición concentró tres errores y la única ayuda. Se incorporaron recuperación de cantidad, claridad del guardado, identificación del producto y lectura de cantidad por precio. Las capturas muestran los ajustes; no se dispone de mediciones posteriores con participantes.

## Informe final y organización

El [informe institucional final](Docs/Guia_4_IHC_Grupo6.pdf) reúne el desarrollo de la guía APE integral, sus resultados y evidencias. La documentación de esta carpeta corresponde exclusivamente a la actividad integral de CaféU. Las entregas anteriores permanecen en sus carpetas del repositorio y el README de la raíz funciona como presentación general del proyecto.

El [registro de aportes](colaboracion/aportes.md) presenta la participación del equipo conforme a la tabla 18 del informe. La evidencia de autoría en GitHub corresponde al historial real de contribuciones del repositorio.
