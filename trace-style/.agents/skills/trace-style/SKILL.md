---
name: trace-style
description: "Diseña, implementa o refina interfaces web y de aplicaciones con superficies planas, sin degradados ni brillos, bordes discretos y jerarquía tipográfica clara. Úsala cuando se pida Trace Style, diseño plano y sobrio o controles de aspecto nativo; también para revisar componentes frente a ese lenguaje visual. No se aplica a tareas de frontend sin esta dirección visual."
metadata:
  version: "1.0.0"
---

# Trace Style

Resuelve la interfaz solicitada con un lenguaje plano, sobrio y preciso. Define la identidad mediante composición, proporciones, tipografía y comportamiento de los controles. Usa las herramientas disponibles en tu entorno; esta skill aporta instrucciones y referencias, sin requerir servicios, plugins ni una aplicación de origen.

## Parte del encargo

Identifica qué necesita hacer la persona, qué contenido existe y qué parte de la interfaz debe cambiar. Conserva la marca, el stack y los comportamientos del producto. En un proyecto nuevo, toma las decisiones que falten según su propósito. La paleta, el tema claro u oscuro, las fuentes y la estructura de navegación son variables del producto.

Aplica los cambios al alcance solicitado. Las instrucciones explícitas del usuario prevalecen; limita cualquier excepción visual a lo que haya pedido.

## Mantén el acabado plano

- Rellenos sólidos y uniformes en fondos, tarjetas, controles, etiquetas y selecciones.
- Sin gradientes ni degradados en superficies, texto, bordes o gráficos decorativos.
- Sin brillos en bordes, halos, neón, reflejos, resplandores ni biseles. Evita sombras decorativas, glassmorphism y desenfoque de fondo.
- Separa grupos mediante espacio, diferencias de relleno plano y bordes finos uniformes. Evita multiplicar cajas y contornos dentro del mismo grupo.
- Repite familias de radios, espaciado, pesos tipográficos e iconos. Usa tamaño, posición y agrupación para establecer jerarquía.
- Mantén estos criterios en hover, foco, pulsación, selección, carga y error. El foco accesible es un contorno sólido visible, sin halo difuso.

## Elige la ruta de trabajo

| Encargo | Actuación y referencias |
| --- | --- |
| Crear una pantalla o componente | Compón desde la tarea principal. Consulta [lenguaje visual](references/visual-language.md) y las secciones necesarias de [patrones de componentes](references/component-patterns.md). |
| Refinar una interfaz existente | Reutiliza sus componentes y contratos. Consulta [integración y revisión](references/implementation-and-review.md) para delimitar los cambios y comprobar estados heredados. |
| Revisar el estilo | Compara los componentes con estas reglas y usa los criterios de [integración y revisión](references/implementation-and-review.md). Entrega hallazgos; aplica correcciones cuando se hayan solicitado. |

Lee solo las guías pertinentes al encargo. Resuelve todas las referencias desde la carpeta que contiene este archivo.

## Compón e implementa

1. Establece un foco claro y agrupaciones que respondan al contenido. No inventes métricas, gráficos ni secciones para llenar la pantalla.
2. Define roles semánticos de fondo, superficies, texto, borde, acción, selección y error. Usa los tokens del proyecto o crea el conjunto mínimo necesario.
3. Construye con el sistema de componentes existente y sus convenciones. Prioriza alineación, proporción y legibilidad frente a ornamentación.
4. Completa los estados relevantes y la adaptación a dispositivos. Conserva la selección de texto, el zoom, el uso con teclado y las áreas táctiles cómodas.
5. Comprueba el resultado y corrige las desviaciones observadas. Examina también estilos en ejecución, bibliotecas, pseudoelementos, SVG y canvas.

Si tienes una vista previa, revisa la interfaz renderizada con contenido real y los estados disponibles. Si solo puedes leer código o capturas estáticas, indica el alcance de esa comprobación. No equipares una revisión del código con haber probado la interacción.

## Entrega el resultado

Entrega la implementación, el prototipo, la especificación o la revisión solicitada. Explica brevemente qué decisiones afectan al resultado y qué se ha comprobado. Antes de cerrar, verifica que la tarea original está resuelta y distingue los límites pendientes de lo que has podido validar.
