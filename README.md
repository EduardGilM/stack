# Stack

Colección de skills reutilizables para agentes de programación y diseño.

## Skills

| Skill | Propósito | Documentación |
| --- | --- | --- |
| [Trace Style](trace-style/README.md) | Diseñar, implementar y revisar interfaces con componentes planos, bordes discretos y jerarquía clara. | [Instalación](trace-style/docs/installation.md) · [Ejemplos](trace-style/docs/examples.md) |

## Instalación

Desde el proyecto que recibirá la skill:

```sh
npx skills add EduardGilM/stack --skill trace-style
```

Puedes indicar un agente concreto con `--agent codex`, `--agent claude-code` o `--agent cursor`. La [guía de instalación](trace-style/docs/installation.md) también explica la copia manual y la carga en otros agentes.

Cada carpeta contiene una distribución independiente, con su documentación, instrucciones y referencias. Conserva las carpetas ocultas `.agents/` al copiar o compartir el contenido.
