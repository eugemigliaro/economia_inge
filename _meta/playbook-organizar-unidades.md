# PLAYBOOK (ARCHIVADO) — Organizar una sección unidad por unidad

> **Estado: ARCHIVADO.** Economía empresarial está **100% organizada** (Unidades 1–4 hechas).
> Este archivo NO es trabajo pendiente y **no hace falta leerlo** salvo para una sola tarea:
> **organizar material de una sección/unidad nueva desde el PDF** (p. ej. microeconomía o
> macroeconomía). Para estudiar, repasar o responder preguntas, ignoralo y andá a `/apuntes`.
> Cuando organices una sección nueva: copiá el "Procedimiento por unidad" y el "Estilo de nota"
> tal cual, y agregá las fichas de esa sección (rango de páginas, comando de `pdftotext`).

Este documento es **autocontenido**. Está pensado para ejecutarse **una unidad por vez,
limpiando el contexto entre unidades**. Cada vez que arranques una unidad nueva, leé:

1. Este playbook (sobre todo la sección "Procedimiento por unidad" y la ficha de la unidad).
2. `apuntes/CONTEXT.md` (estilo y estructura de las notas).
3. El `index.md` de la unidad que vas a hacer.

No hace falta leer las otras unidades ni el resto del repo. Esa es justamente la idea: que
puedas organizar la Unidad 3 sin saber nada de lo que pasó cuando se hizo la Unidad 1.

## Fuente

PDF oficial: `material/apuntes-pdf/13-03-06 APUNTE EPI.pdf` (82 páginas, gitignoreado, local).
Es la sección **Economía empresarial** completa de la materia.

**Numeración:** la página impresa del apunte (doc) arranca en la primera página de contenido.
`pdftotext` usa páginas **físicas**. La conversión es **física = doc + 4**.

Para extraer el texto de una unidad usá su rango de páginas **físicas**:

```bash
cd /home/emigliaro/Documents/facultad/tercero/economia_inge
pdftotext -layout -f <pag_fisica_inicio> -l <pag_fisica_fin> \
  "material/apuntes-pdf/13-03-06 APUNTE EPI.pdf" -
```

(El flag `-layout` conserva tablas y columnas, importante para los estados contables y
los flujos de fondos. Si una tabla sale ilegible, reintentá esa página sin `-layout`.)

## Estado de avance

- [x] Unidad 1 — Contabilidad
- [x] Unidad 2 — Costos
- [x] Unidad 3 — El Valor del Dinero en el Tiempo
- [x] Unidad 4 — Evaluación de Proyectos

> Al terminar una unidad, marcá su casilla acá y marcá los conceptos hechos en el `index.md`
> de la unidad. Así el próximo contexto sabe por dónde seguir sin leer todo.

---

## Procedimiento por unidad (el mismo para las 4)

1. **Ubicarte.** Leé este `PLAN.md`, `apuntes/CONTEXT.md` y el `index.md` de la unidad.
2. **Extraer.** Corré `pdftotext -layout` con el rango de páginas físicas de la ficha de la unidad.
3. **Trocear.** Partí la unidad en conceptos atómicos. La lista de archivos sugerida está en la
   ficha de cada unidad (abajo) y en el `index.md`. Un archivo `.md` por concepto. Si al leer el
   texto descubrís un subtema que merece archivo propio, agregalo (y agregalo al `index.md`).
4. **Escribir cada nota** en `apuntes/economia-empresarial/<unidad>/<concepto>.md` siguiendo el
   **estilo de nota** (ver abajo). Español, definición corta arriba, detalle abajo.
5. **Casos / ejercicios resueltos** que aparezcan en el apunte (ej. el caso de Edenor en la U1,
   el caso integrador de la U4) **no** van como apunte teórico: van a
   `practica/ejercicios/caso-<unidad>-<tema>.md` con el estilo de `practica/CONTEXT.md`.
   En el apunte teórico dejás solo el concepto + un link mental a la resolución.
6. **Cerrar la unidad.** Actualizá el `index.md` (marcá `[x]` lo hecho, ajustá links/nombres si
   cambiaron) y marcá la casilla de la unidad en este `PLAN.md`.
7. **Reportar.** Mostrá al usuario un resumen: qué archivos se crearon y qué subtema cubre cada uno.
8. **Limpiar contexto** y pasar a la unidad siguiente.

### Estilo de nota (resumen — el detalle está en `apuntes/CONTEXT.md`)

- `# Encabezado` con el nombre del concepto.
- Definición de 1–3 oraciones arriba de todo.
- Secciones con detalle: fórmulas en texto plano legible (ej. `CMg = ∂CT / ∂Q`,
  `VAN = Σ FF_t/(1+i)^t − I_0`), ejemplos numéricos, tablas Markdown, diagramas ASCII.
- Si hay una fórmula clave, ponela en su propio bloque para que se encuentre rápido.
- Cerrar con la cita: `> Apunte EPI, Parte <n> — <tema>, doc p. <N>.`
- Si el concepto suele caer en parcial, agregá una sección `## Aparece en parciales` (cuando
  haya parciales viejos en `material/examenes/`).

### Reglas duras

- No editar nunca el PDF ni nada en `/material`. Solo se cita.
- No inventar contenido: si el apunte no lo dice, no lo pongas (o marcalo como duda para el usuario).
- No borrar archivos del usuario. Crear y, a lo sumo, appendear.
- Una nota = un concepto. Mejor varios archivos chicos y buscables que uno gigante.

---

## Ficha — Unidad 1: Contabilidad

- **Carpeta:** `apuntes/economia-empresarial/01-contabilidad/`
- **Páginas:** doc 1–17 · **físicas 5–21**
- **Comando:** `pdftotext -layout -f 5 -l 21 "material/apuntes-pdf/13-03-06 APUNTE EPI.pdf" -`
- **Conceptos / archivos sugeridos:**
  - `la-empresa-y-la-contabilidad.md` — qué es la empresa, para qué sirve la contabilidad
  - `ecuacion-patrimonial.md` — `Activo = Pasivo + Patrimonio Neto`
  - `balance.md` — estructura del balance (activo / pasivo / PN), corriente vs no corriente
  - `cuadro-de-resultados.md` — ingresos, costos, resultado del ejercicio
  - `cash-flow.md` — flujo de caja, diferencia con el cuadro de resultados
  - `valor-de-mercado-vs-valor-de-libros.md`
  - `cuentas.md` — patrimoniales (activo/pasivo/PN), de resultado, regularizadoras
  - `partida-doble.md` — debe/haber, por qué siempre balancea
  - `operaciones-basicas.md` — asientos típicos
- **A `practica/`:** `caso-01-edenor.md` — el ejemplo de estados contables de Edenor S.A.
  (anexo 1.7). Es un caso aplicado, no teoría.

## Ficha — Unidad 2: Costos

- **Carpeta:** `apuntes/economia-empresarial/02-costos/`
- **Páginas:** doc 18–45 · **físicas 22–49**
- **Comando:** `pdftotext -layout -f 22 -l 49 "material/apuntes-pdf/13-03-06 APUNTE EPI.pdf" -`
- **Conceptos / archivos sugeridos:**
  - `clasificacion-de-costos.md` — fijos/variables, marginal, recurrentes/no recurrentes,
    directo/indirecto, estándar, contable/efectivo, hundido, de oportunidad
    (si alguno es muy denso, partilo en su propio archivo)
  - `costeo-por-absorcion.md`
  - `costeo-directo.md` — incluir la comparación directo vs absorción
  - `costeo-abc.md` — costeo basado en actividades + comparación con el tradicional
  - `punto-de-equilibrio.md` — fórmula y gráfico ASCII
  - `analisis-marginal.md` — utilidad unitaria, utilidad marginal unitaria, tasa de utilidad
    marginal, casos de aplicación
  - `costo-del-ciclo-de-vida.md`
  - `gasto-vs-inversion.md`
  - `estimacion-de-costos.md`
  - `optimizacion-del-diseno.md` — minimización de costos en el diseño
- **A `practica/`:** los "casos de aplicación" del análisis marginal (2.5.4), si son ejercicios
  numéricos resueltos → `caso-02-analisis-marginal.md`.

## Ficha — Unidad 3: El Valor del Dinero en el Tiempo

- **Carpeta:** `apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/`
- **Páginas:** doc 46–56 · **físicas 50–60**
- **Comando:** `pdftotext -layout -f 50 -l 60 "material/apuntes-pdf/13-03-06 APUNTE EPI.pdf" -`
- **Conceptos / archivos sugeridos:**
  - `introduccion.md`
  - `interes.md` — interés compuesto e interés simple (fórmulas + ejemplo de los $1000 al 10%)
  - `tipos-de-tasas.md` — nominal vs efectiva, tasas equivalentes
  - `valor-actual.md` — cálculo del VA, factor de descuento
  - `anualidades.md`
  - `perpetuidades.md`
  - `tipos-de-prestamos.md` — sistemas de amortización (francés, alemán, americano si aparecen)
  - `inflacion-y-tasas.md` — tasa real vs nominal, Fisher

## Ficha — Unidad 4: Evaluación de Proyectos

- **Carpeta:** `apuntes/economia-empresarial/04-evaluacion-de-proyectos/`
- **Páginas:** doc 57–77 · **físicas 61–81**
- **Comando:** `pdftotext -layout -f 61 -l 81 "material/apuntes-pdf/13-03-06 APUNTE EPI.pdf" -`
- **Conceptos / archivos sugeridos:**
  - `introduccion.md` — para qué se evalúa, estructura típica de un proyecto
  - `flujos-de-fondos.md` — inversiones, flujo de fondos operativo (FEO), extraordinario (FEE)
  - `conceptos-clave.md` — análisis marginal, costo de oportunidad, costos hundidos, ubicación
    temporal de fondos (apuntan a lo visto en U2/U3; linkear)
  - `van.md` — Valor Actual Neto: fórmula, tasa de descuento, criterio de decisión, ejemplo
  - `tir.md` — Tasa Interna de Retorno: definición, cálculo, criterio, limitaciones
  - `tirm.md` — Tasa Interna Modificada (TER/TIRM): por qué surge, cálculo, ejemplo
  - `payback.md` — período de repago simple y descontado
  - `vida-economica.md` — aplicación: minimización de costos y vida económica (4.9)
- **A `practica/`:** el caso integrador (4.8, enunciado + flujos + VAN/TIR/TIRM/payback) →
  `caso-04-evaluacion-de-proyectos.md`. Es el ejercicio central de la unidad.

---

## Después de las 4 unidades

- Revisar `apuntes/economia-empresarial/` y verificar que cada `index.md` tenga todo en `[x]`.
- Bibliografía (doc p.78 / física 82): no necesita apunte; si querés, una nota corta
  `apuntes/economia-empresarial/bibliografia.md`.
- Cuando aparezca material de **microeconomía** o **macroeconomía**, replicar esta misma
  estructura bajo `apuntes/microeconomia/` y `apuntes/macroeconomia/`, y agregar su ficha acá.
