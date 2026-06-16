# Método de la Tasa Interna Modificada (TIRM / TER)

La **TIRM** (también llamada **TER**) corrige el principal supuesto de la [[tir|TIR]]: en vez de
suponer que los flujos intermedios se reinvierten a la propia TIR, supone que se reinvierten a
una **tasa de reinversión realista** (normalmente la TREMA). Suele ser **menor que la TIR**.

## Por qué surge

La TIR asume implícitamente reinversión de los flujos intermedios **a la misma TIR**, que es una
tasa matemática y no de mercado. Si la TIR es del 48%, suponer que cada flujo se reinvierte al
48% no es real. La TIRM repara ese daño reinvirtiendo a una tasa disponible de verdad.

> Si un proyecto ya tiene TIR **menor** que la tasa de reinversión, no hace falta calcular la
> TIRM: el proyecto no es conveniente.

## Cálculo (4 pasos)

1. Identificar la **tasa de reinversión** disponible durante la vida del proyecto (suele
   adoptarse igual a la TREMA).
2. **Capitalizar** hasta el final del proyecto (período `n`) cada flujo intermedio **positivo**.
3. **Descontar a hoy** (período 0) cada flujo intermedio **negativo**.
4. Calcular la TIR de este flujo simplificado: un único flujo negativo en `t=0` y uno positivo en
   `t=n`. Esa tasa es la TIRM.

```
VAN(TIRM) = 0 = − VA(flujos negativos) + VF_n(flujos positivos) / (1+TIRM)^n
```

## Ejemplo

Proyecto a 4 años. Tasa de reinversión = 20%. TIR original = 42%.

| Año | 0        | 1        | 2        | 3        | 4        |
|-----|----------|----------|----------|----------|----------|
| FFN | −500.000 | 400.000  | −100.000 | 200.000  | 800.000  |

**Capitalizar los positivos al año 4:**

```
FFN_1 = 400.000 × 1,2^3 = 691.200
FFN_3 = 200.000 × 1,2^1 = 240.000
FFN_4 = 800.000          = 800.000
                          ─────────
VF total año 4         ≈ 1.731.000
```

**Descontar los negativos a hoy:**

```
FFN_0 = −500.000          = −500.000
FFN_2 = −100.000 / 1,2^2  =  −69.444
                            ──────────
VA flujos negativos        = −569.444
```

**Flujo simplificado y TIRM:**

```
   −569.444 (hoy)                       1.731.000 (año 4)
        ●───────────────────────────────────▲
        0                                    4

VAN(TIRM) = 0 = −569.444 + 1.731.000 / (1+TIRM)^4
TIRM = 32%   (< TIR = 42%)
```

> Apunte EPI, Parte 4 — Evaluación de Proyectos (4.6), doc p. 64–66.
