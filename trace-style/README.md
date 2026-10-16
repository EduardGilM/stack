# Trace Style

Una skill de diseño de interfaces para agentes: componentes planos, bordes discretos, proporciones cuidadas y jerarquía clara. Funciona con la marca, el tema, las fuentes y el stack de cada producto.

[Instalación para agentes](docs/installation.md) · [Ejemplos](docs/examples.md) · [Instrucciones de la skill](.agents/skills/trace-style/SKILL.md)

## Inicio rápido

Desde la raíz del **proyecto de destino**, instala la skill desde su repositorio:

```sh
npx skills add EduardGilM/stack --skill trace-style
```

Selecciona el agente y el alcance de instalación. También puedes indicar un agente concreto:

```sh
npx skills add EduardGilM/stack --skill trace-style --agent codex
```

El gestor admite fuentes locales y selección de skills y agentes. Consulta sus [opciones oficiales](https://github.com/vercel-labs/skills#options) para otros destinos. Para instalación manual o agentes sin descubrimiento de skills, sigue la [guía de instalación](docs/installation.md).

## Pide el trabajo

> Usa Trace Style para diseñar e implementar una pantalla de reservas. Conserva la marca, los datos y el stack del proyecto.

La skill sirve para crear pantallas, refinar componentes existentes o revisar su acabado visual. El agente consulta las referencias pertinentes y entrega el resultado solicitado.

## Lenguaje visual

- Superficies y controles con rellenos planos.
- Bordes finos, radios consistentes y agrupaciones claras.
- Jerarquía mediante tipografía, proporción, alineación y espacio.
- Estados accesibles y transiciones contenidas.
- Acabado sin degradados, brillos, halos ni ornamentación de cristal.

Los colores, el tema claro u oscuro y las fuentes pertenecen al producto. No se requiere una aplicación de referencia.

## Estructura

```text
trace-style/
├── README.md
├── docs/
│   ├── installation.md
│   └── examples.md
└── .agents/skills/trace-style/
    ├── SKILL.md
    ├── agents/openai.yaml
    └── references/
        ├── visual-language.md
        ├── component-patterns.md
        └── implementation-and-review.md
```

El contenido que se instala es `.agents/skills/trace-style/`. El README y `docs/` explican cómo distribuirlo y usarlo; las instrucciones de diseño son autónomas.

La skill sigue el [formato Agent Skills](https://agentskills.io/specification). Leerla y aplicarla no necesita dependencias ni servicios externos. La instalación mediante `npx` utiliza Node.js y npm; la copia manual no los necesita.

## Compartir y mantener

Comparte esta carpeta completa o su ZIP. También puedes distribuir únicamente la carpeta de la skill si el receptor ya sabe cómo instalarla. Conserva las referencias junto a `SKILL.md`.

La distribución está en [EduardGilM/stack](https://github.com/EduardGilM/stack/tree/main/trace-style). También puedes instalar una copia local sustituyendo `EduardGilM/stack` por la ruta de esta carpeta.

La versión de las instrucciones se declara en el frontmatter de `SKILL.md`. Para comprobar el descubrimiento sin instalar, ejecuta desde esta carpeta:

```sh
npx skills add . --skill trace-style --list
```
