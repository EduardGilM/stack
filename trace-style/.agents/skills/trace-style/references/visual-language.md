# Lenguaje visual

Consulta esta guía para decidir el acabado de una pantalla o resolver inconsistencias entre componentes. Los valores concretos de color y fuente pertenecen al producto.

## Rellenos planos y acabado mate

- Usa colores sólidos y uniformes en fondos, tarjetas, botones, campos, etiquetas y estados de selección.
- Sin gradientes ni degradados, incluidos fondos radiales, mallas, texto degradado, bordes con degradado y fundidos decorativos. Aplica el criterio tanto a CSS como a SVG, canvas y componentes de terceros.
- Sin brillo en los bordes, halos, neón, resplandores interiores o exteriores, reflejos, destellos ni superficies de aspecto metálico o cristalino.
- Sin glassmorphism, desenfoque de fondo, velos decorativos o texturas de ruido. Usa cabeceras sólidas. Una imagen de contenido puede conservar sus luces naturales; no añadas estos efectos para vestir los controles.
- Evita las sombras decorativas, los biseles y el relieve de neumorfismo. Separa superficies mediante espacio, un cambio de relleno plano o un borde fino. Un fondo uniforme de atenuación para un diálogo es funcional, no un acabado de cristal.

## Bordes y geometría

- Bordes de grosor uniforme, normalmente 1 px, con contraste moderado. No añadas dobles contornos ni ribetes luminosos.
- Usa pocas familias de radios: paneles amplios, campos y controles algo más contenidos, y pastillas para chips o acciones cuando encajen. Mantén la misma geometría para el mismo tipo de componente.
- Alinea bordes, textos, iconos y valores con una retícula reconocible. Los márgenes internos deben responder al contenido, sin cambios arbitrarios de tarjeta a tarjeta.
- Agrupa elementos relacionados en una superficie compartida con separadores finos. Evita convertir cada dato o fila en una tarjeta y encadenar tarjetas dentro de tarjetas.

## Jerarquía y densidad

- Define qué debe ver o hacer primero la persona. Dale protagonismo mediante tamaño, posición y espacio; mantén las acciones auxiliares en segundo plano.
- Usa títulos claros, texto de interfaz de tamaño cómodo y metadatos discretos. Reserva mayúsculas con espaciado para etiquetas breves; no las extiendas a frases, párrafos o todos los botones.
- Cuando haya métricas reales, haz que el valor domine sobre su etiqueta y su unidad. Alinea las cifras comparables y usa números tabulares. Una variante condensada o monoespaciada es opcional, no una identidad obligatoria.
- Combina contenido compacto dentro de cada grupo con espacio suficiente entre grupos. La sobriedad no exige vaciar la pantalla ni reducir todo a texto diminuto.
- Deja el énfasis cromático para acciones, selección y estados que lo necesiten. La jerarquía también debe entenderse por tamaño, peso, posición y agrupación.

## Controles e iconos

- Botones simples, de relleno plano o contorno discreto. La acción principal se distingue por contraste y posición; no necesita brillo ni un color concreto.
- Iconos de una familia coherente, con grosor y tamaño óptico consistentes. No uses emojis decorativos como sustituto de los iconos de interfaz.
- Selecciones mediante una combinación de relleno sólido, contorno, marca o indicador breve. Mantén distinguibles los estados sin depender únicamente del color.
- Navegación discreta y estable. Elige pestañas, navegación inferior o barra lateral según los destinos, la frecuencia de uso y el espacio disponible.
- En formularios, prioriza etiquetas visibles, campos alineados y errores junto al control. En listas, usa filas legibles con título, detalle y acción o valor alineado.

## Movimiento y profundidad

- Transiciones breves para cambios de estado, apertura y pulsación; como referencia, 120–200 ms. Evita animación continua decorativa, efectos de brillo al pasar el cursor y elevaciones de tarjetas en hover.
- Si usas una respuesta de pulsación, que sea mínima y no mueva el contenido circundante. Respeta la preferencia de movimiento reducido.
- El foco de teclado es un contorno sólido y visible, sin desenfoque. No lo elimines para conservar la estética.
