# Patrones de componentes

Consulta las secciones del componente que estés diseñando. Estos patrones desarrollan el lenguaje visual de la skill; las medidas son puntos de partida, no tamaños que deban copiarse literalmente.

## Proporciones de partida

Para una interfaz compacta de producto, un cuerpo de 14–16 px suele permitir esta escala. Ajusta al dispositivo, al contenido y a los componentes ya existentes.

| Elemento | Tratamiento |
| --- | --- |
| Título de pantalla | Mayor que el texto de interfaz, peso regular o medio, sin efectos tipográficos |
| Título de grupo | Cercano al cuerpo, peso medio o seminegrita |
| Etiqueta breve | Menor que el cuerpo, espaciado moderado si va en mayúsculas |
| Valor protagonista | 2–4 veces el cuerpo si hay una métrica que lo justifique |
| Unidad y detalle | Menores que el valor; alineados a su línea base |
| Radio de panel | Aproximadamente 16–20 px |
| Radio de campo o control | Aproximadamente 10–12 px |
| Padding de panel | Aproximadamente 14–20 px |
| Separación interna | Aproximadamente 6–12 px; incrementarla entre grupos distintos |
| Acción táctil frecuente | Área de interacción cómoda, como referencia 44–52 px de alto |

No reduzcas el texto o el área táctil para encajar estos rangos. Las etiquetas secundarias necesitan contraste suficiente; «discreto» no significa difícil de leer.

## Tarjetas y paneles

Fondo sólido, radio consistente y, si hace falta separación adicional, borde fino uniforme. El título puede compartir fila con una acción auxiliar. El contenido comienza cerca del título y conserva una alineación común.

Una sección que comparte contexto debe parecer un grupo: por ejemplo, un panel con varias métricas y divisores interiores. Si el fondo, el espaciado y el título ya delimitan una sección, no necesita obligatoriamente otra caja.

Evita sombras ambientales, degradados apenas visibles, líneas luminosas en el borde superior, pseudo-elementos con halos y esquinas de tamaños distintos sin una función.

## Botones y acciones

- Primario: relleno sólido con contraste claro respecto al entorno y etiqueta concisa. Puede usar un tono de marca o un neutro del producto.
- Secundario: relleno sólido de menor protagonismo o contorno fino, con la misma familia de proporciones.
- Auxiliar: texto o icono con una superficie simple cuando sea necesaria para reconocer la interacción.
- Destructivo: jerarquía proporcionada a su uso y semántica visible. No compite permanentemente con la tarea principal.

En hover, cambia discretamente entre dos colores planos o refuerza el contorno. En pulsación, una variación mínima de escala es suficiente si encaja en el sistema. Un botón deshabilitado sigue siendo reconocible. Ninguno de estos estados añade brillo, sombra difusa ni degradado.

## Listas, ajustes y formularios

Usa un contenedor compartido para filas relacionadas. Mantén el título a la izquierda y el valor, estado o acción alineado en una columna previsible. Separa filas con líneas discretas o espacio, sin apilar múltiples contornos por fila.

En ajustes, el nombre del campo y el valor pueden compartir fila cuando caben; en anchos pequeños o textos largos, permite que se apilen. No recortes el valor esencial para conservar una composición horizontal.

Campos con relleno uniforme, borde fino y foco visible. La ayuda y el error pertenecen al campo al que se refieren. No uses el placeholder como única etiqueta.

## Chips, segmentos y navegación

Las pastillas encajan en filtros, pequeños estados y selectores. Su radio no obliga a hacer circular todo el sistema.

Para una selección, usa un relleno sólido alternativo y una marca, un cambio de peso o un contorno claro. Para navegación, un indicador corto puede señalar la sección actual sin colorear todo el contenedor. Conserva una señal de selección que no dependa únicamente del matiz.

La navegación inferior es adecuada para destinos frecuentes en una app móvil; una vista de escritorio puede usar una barra lateral o superior. Cambia la estructura según la tarea, conservando el tratamiento de superficies, tipografía e indicadores.

## Métricas, tablas y gráficos

En métricas, el dato destaca, la unidad acompaña y la etiqueta explica. Las columnas de números comparables mantienen alineación y formato. No agrandes todos los números ni inventes estadísticas para llenar una pantalla.

Gráficos con trazos de grosor consistente, marcas puntuales y retícula discreta. Series y áreas usan colores planos, sin degradados bajo la curva, líneas con halo ni efectos 3D. Si dos series deben distinguirse, combina color con tipo de trazo, marcador o etiqueta.

En tablas, usa encabezados claros, alineación por tipo de dato y separadores sobrios. No asignes un fondo y una tarjeta independiente a cada celda.

## Cabeceras, diálogos y estados

Cabecera compacta con título claro y pocas acciones. Si permanece visible durante el scroll, dale un fondo sólido y reserva espacio para que no oculte contenido. No necesita desenfoque ni un fundido hacia la página.

Diálogos y paneles superpuestos con superficie sólida y límites reconocibles. Un fondo de atenuación uniforme puede separar el contexto; no lo conviertas en una textura o efecto de cristal. Conserva el comportamiento accesible de diálogo, incluido foco y cierre.

Estado vacío: explicación breve, icono opcional y una acción útil cuando exista. Carga: indicador simple o placeholders sólidos, sin bandas de brillo animadas. Error: mensaje junto al contexto afectado y una recuperación concreta cuando esté disponible.

## Trasladar el estilo a otros productos

| Contexto | Aplicación del lenguaje |
| --- | --- |
| Gestor de proyectos | Tareas agrupadas en filas, prioridad reconocible, acciones planas y detalle progresivo |
| Biblioteca de contenido | Tipografía y alineación que ordenan títulos y metadatos; imágenes como contenido, no como decoración de controles |
| Herramienta de análisis | Dato principal destacado, métricas agrupadas, tablas y trazos planos |
| Formulario de servicio | Secciones por tarea, etiquetas legibles, campos consistentes y una acción principal clara |

La misma composición debe poder funcionar con tema claro u oscuro y con marcas distintas. Cambiar la paleta no requiere añadir efectos para recuperar identidad.

## Traducción a estilos de implementación

Define los valores de estas variables con el sistema visual del producto. Este ejemplo describe el acabado de componentes propios; no es un reset global ni una paleta prefijada.

```css
.panel {
  background-color: var(--surface);
  background-image: none;
  border: 1px solid var(--border);
  border-radius: var(--radius-panel);
  padding: var(--space-panel);
  box-shadow: none;
}

.action {
  background-color: var(--action);
  background-image: none;
  color: var(--on-action);
  border: 1px solid var(--action-border);
  border-radius: var(--radius-control);
  box-shadow: none;
  text-shadow: none;
}

.action:focus-visible {
  outline: 2px solid var(--focus);
  outline-offset: 2px;
}

.action[aria-pressed="true"] {
  background-color: var(--selected);
  color: var(--on-selected);
  border-color: var(--selected-border);
}
```

Completa los demás estados con los mismos roles semánticos. En sistemas con clases de utilidad, componentes nativos o estilos encapsulados, expresa estas mismas decisiones con las primitivas disponibles. Comprueba que las variantes y pseudoelementos tampoco añadan efectos decorativos.
