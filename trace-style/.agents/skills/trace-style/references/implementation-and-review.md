# Integración y revisión

Usa esta guía para adaptar una interfaz existente o comprobar el resultado de una implementación. El objetivo es conservar sus funciones mientras los componentes adoptan el acabado de Trace Style.

## Delimita el cambio

Identifica las pantallas y estados afectados, los componentes compartidos y los tokens que ya utiliza el proyecto. Distingue una variante local de una primitiva común antes de modificarla.

Una petición sobre un componente no justifica sustituir el framework, rehacer la navegación o cambiar toda la marca. Si un estilo compartido produce una desviación localizada, usa una variante o un ajuste acotado cuando sea la solución adecuada.

## Examina el estilo efectivo

No te quedes con la primera regla CSS que encuentres. Comprueba las variantes del sistema, los estilos aplicados en ejecución y los estados interactivos.

| Lugar | Qué comprobar |
| --- | --- |
| Fondo y borde | Rellenos uniformes; ausencia de degradados y bordes decorativos |
| Pseudoelementos | Halos, capas con reflejos, líneas luminosas y fondos añadidos |
| Hover, foco y selección | Sombras o efectos que reaparecen solo en esos estados |
| Bibliotecas de componentes | Valores por defecto de elevación, gradientes, animaciones y anillos difusos |
| SVG y canvas | Rellenos con degradado, filtros de brillo, sombras y efectos 3D |
| Carga | Bandas de brillo animadas o superficies decorativas que rompen el acabado plano |

Corrige el origen de la desviación. Evita resets globales como eliminar todos los filtros, sombras o fondos de la aplicación: pueden afectar a contenido, legibilidad y estados accesibles ajenos al encargo.

## Conserva los contratos de interacción

Mantén etiquetas, nombres accesibles, validaciones, acciones, orden de foco y relaciones entre controles. Un cambio de aspecto no debe alterar silenciosamente qué hace un botón, qué datos guarda un campo o cómo se selecciona una opción.

Expresa selección, errores y estados mediante una señal adicional al color cuando sea necesaria: texto, marca, indicador o forma. Un contorno de foco sólido es parte de la interacción y debe seguir siendo visible.

## Comprueba el resultado

Con navegador o vista previa, revisa los estados pertinentes con contenido representativo:

- Ancho pequeño y ancho amplio; textos largos, unidades, fechas y cifras reales.
- Estado normal y variantes de hover, foco, pulsación, selección y deshabilitado.
- Vacío, carga y error cuando existan.
- Navegación con teclado, texto ampliado y ausencia de contenido esencial oculto.
- Alineación, espaciado, radios e iconos coherentes entre componentes equivalentes.
- Rellenos planos y ausencia de brillos o degradados en todos los estados comprobados.

Ejecuta las comprobaciones pertinentes del proyecto si el cambio altera comportamiento o su sistema de componentes. Una modificación de estilo localizada no necesita una batería de pruebas que solo replique sus valores CSS.

Sin vista previa, comprueba los estilos y contratos que puedas observar. Una captura estática permite evaluar composición y acabado, pero no demuestra que funcionen foco, formularios, navegación ni estados ocultos.

## Entrega una revisión útil

Si el encargo es revisar, identifica desviaciones concretas y su efecto. Cita el componente, archivo, selector o estado que las demuestra y propone una corrección proporcionada. Distingue incumplimientos de Trace Style de preferencias opcionales.

Si el encargo incluye corregir, aplica los cambios y comprueba el resultado. Resume qué cambió y qué pudiste verificar. No afirmes que se ha probado un dispositivo, un tema o una interacción que no hayas observado.
