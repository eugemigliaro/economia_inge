# Apuntes — mis notas organizadas

Esta es mi base de conocimiento curada. Lo que está acá es lo que estudio.

## Estructura
Primero por **sección** de la materia, después por **unidad**:

```
apuntes/
  economia-empresarial/   ← sección que se está organizando ahora
    01-contabilidad/
    02-costos/
    03-valor-del-dinero-en-el-tiempo/
    04-evaluacion-de-proyectos/
  microeconomia/          ← placeholder, pendiente
  macroeconomia/          ← placeholder, pendiente
```

Cada unidad lleva prefijo numérico que matchea el orden del PDF oficial. Dentro de cada unidad:
- un `index.md` con el TOC oficial de la unidad y links a cada concepto;
- un archivo `.md` por concepto importante, nombre en kebab-case en español.

Ejemplos:
- `apuntes/economia-empresarial/01-contabilidad/ecuacion-patrimonial.md`
- `apuntes/economia-empresarial/02-costos/punto-de-equilibrio.md`
- `apuntes/economia-empresarial/04-evaluacion-de-proyectos/van.md`

## Estilo de nota
- Encabezado con el concepto.
- Una definición corta arriba de todo (1–3 oraciones).
- Después, secciones con detalles, fórmulas, ejemplos numéricos y tablas/diagramas ASCII si aplica.
- Las fórmulas en texto plano legible (ej. `VAN = Σ FF_t / (1+i)^t − I_0`).
- Si la nota se construyó a partir de varias clases o fuentes, dejar la referencia al final.
- Al final, citar la página del apunte oficial (ej. "Apunte EPI, Parte 1, p. 2").

## Cómo se llena
Dos caminos:
1. **Desde el PDF oficial**: seguir el workflow por unidad de `PLAN.md` (raíz del repo).
2. **Vía workflow desde `inbox/`**: el workflow "organizá mis notas" appendéa contenido del inbox
   al archivo correspondiente. Cuando appendéa, deja un separador `---` y un subtítulo con la fecha.

## Para preguntas
Para responder una pregunta de la materia, leer primero los archivos de la unidad correspondiente
acá. Si no alcanza, recién ahí ir a `/material`.
