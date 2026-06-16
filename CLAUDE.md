# Economía para Ingenieros (EPI — ITBA)

Repo de estudio para la materia. El idioma de trabajo es español.

La materia se divide en **tres secciones grandes**:

1. **Microeconomía**
2. **Macroeconomía**
3. **Economía empresarial** ← sección que se está organizando ahora

## Workspaces

- `/inbox` — captura rápida durante la clase. Notas crudas, sin formato, sin clasificar.
- `/material` — material oficial de la cátedra (PDF de apuntes, guías, parciales viejos). Solo lectura, fuente de verdad.
- `/apuntes` — mis notas organizadas, separadas por sección y por unidad. Esta es la base de conocimiento curada.
- `/practica` — mis resoluciones de ejercicios, casos y parciales.

## Secciones y unidades

Los `apuntes` se organizan primero por sección y después por unidad:
`apuntes/<seccion>/<NN-unidad>/<concepto>.md`.

### Economía empresarial (según el PDF oficial de apuntes)

| # | Unidad | Carpeta | Páginas del PDF (doc / físicas) |
|---|--------|---------|---------------------------------|
| 1 | Contabilidad (ecuación patrimonial, balance, cuadro de resultados, cash flow, cuentas, partida doble) | `apuntes/economia-empresarial/01-contabilidad` | 1–17 / 5–21 |
| 2 | Costos (clasificación, costeo absorción/directo/ABC, punto de equilibrio, análisis marginal, ciclo de vida) | `apuntes/economia-empresarial/02-costos` | 18–45 / 22–49 |
| 3 | El Valor del Dinero en el Tiempo (interés, tasas, VA, anualidades, perpetuidades, préstamos, inflación) | `apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo` | 46–56 / 50–60 |
| 4 | Evaluación de Proyectos (flujos de fondos, VAN, TIR, TIRM, payback, casos) | `apuntes/economia-empresarial/04-evaluacion-de-proyectos` | 57–77 / 61–81 |

> El PDF oficial empieza la numeración de páginas en la primera página de contenido.
> **Página de documento N = página física N+4** (las 4 primeras son tapa, autores e índice).
> `pdftotext` usa páginas físicas. La bibliografía está en doc p.78 / física 82.

### Microeconomía y Macroeconomía

Pendientes de organizar. Las carpetas `apuntes/microeconomia/` y `apuntes/macroeconomia/`
existen como placeholder. Cuando llegue su material se replica la misma estructura.

## Ruteo de tareas

| Tarea | Ir a | Leer primero |
|-------|------|--------------|
| Tomar nota en clase | `/inbox` | `inbox/CONTEXT.md` |
| "Organizá mis notas" | `/inbox` → `/apuntes/<seccion>/<unidad>` | `inbox/CONTEXT.md`, `apuntes/CONTEXT.md` |
| "Organizá la unidad N" (desde el PDF) | `/material` → `/apuntes/economia-empresarial/<unidad>` | `_meta/playbook-organizar-unidades.md`, `apuntes/CONTEXT.md` |
| Estudiar / repasar un tema | `/apuntes/<seccion>/<unidad>` | `apuntes/CONTEXT.md` |
| Responder una pregunta teórica | `/apuntes/...` y, si falta info, `/material` | `apuntes/CONTEXT.md` |
| Resolver un ejercicio, caso o parcial | `/practica` | `practica/CONTEXT.md` |

## Convenciones de nombres

- Notas crudas en `inbox/`: `YYYY-MM-DD-tema-corto.md` (la fecha es la del día de la clase).
- Archivos en `apuntes/<seccion>/<unidad>/`: nombre del concepto en kebab-case, en español.
  Ej: `ecuacion-patrimonial.md`, `punto-de-equilibrio.md`, `van.md`, `interes-compuesto.md`.
- Cada unidad tiene un `index.md` con el TOC oficial y links a sus conceptos.
- Resoluciones en `practica/`: `caso-<unidad>-<tema>.md`, `parcial-YYYYqN-tema.md` o `guia-N-ej-M.md`.

## Workflow para organizar una unidad desde el PDF

> Solo aplica al **organizar material nuevo** (Economía empresarial ya está completa; quedan
> microeconomía y macroeconomía). Para estudiar o responder preguntas no hace falta este workflow.

El procedimiento detallado, unidad por unidad, está en el playbook **archivado**
`_meta/playbook-organizar-unidades.md`. La idea es hacer una unidad por vez, limpiando el
contexto entre unidades. Resumen:

1. Extraer el texto de la unidad del PDF oficial (rango de páginas en la tabla de arriba).
2. Partir la unidad en conceptos atómicos (uno por subtema del TOC).
3. Escribir un `.md` por concepto en `apuntes/economia-empresarial/<unidad>/`, en español,
   con definición corta arriba y detalle abajo.
4. Actualizar el `index.md` de la unidad marcando los conceptos hechos.
5. Citar siempre la página del apunte oficial al final de cada nota.

## Workflow para "organizá mis notas" (desde el inbox)

1. Leer cada archivo en `inbox/`.
2. Identificar sección, unidad y tema.
3. Apendear el contenido al archivo correspondiente en `apuntes/<seccion>/<unidad>/<tema>.md`
   (crearlo si no existe), preservando la fecha original como subtítulo.
4. Mover el archivo procesado a `inbox/_archivado/` (no borrarlo).
5. Mostrar un resumen de qué nota fue a qué archivo antes de tocar nada irreversible.

**Regla dura:** nunca se descarta contenido del inbox. Si una nota no encaja claramente, se
deja en el inbox y se pregunta al usuario.

## Reglas generales

- El material en `/material` es solo lectura. Nunca se edita ni se reescribe; se cita.
- Los binarios (`.pdf`, `.zip`, `.docx`, `.xlsx`) están gitignoreados. No commitearlos.
- Cuando se responda usando el PDF de apuntes, citar la sección/unidad y, si es posible, la página.
