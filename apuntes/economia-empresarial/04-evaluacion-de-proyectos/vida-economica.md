# Aplicación: minimización de costos y vida económica

La **vida económica** de un bien es el momento óptimo para **reemplazarlo** por otro nuevo, en
función de sus crecientes costos de mantenimiento y de la pérdida de valor de reventa. No es lo
mismo que la vida técnica: una máquina puede durar 10 años pero convenir cambiarla a los 7.

La herramienta para decidir es el **Costo Anual Equivalente (CAE)**: se elige la opción de
recambio que **minimiza** el CAE.

## El problema

Comparar opciones de recambio (cambiar al año 1, al 2, … al 10) es comparar **proyectos
mutuamente excluyentes con distinta vida**. No se pueden comparar por VAN directo: no es lo mismo
usar la máquina 1 año que 10. Por eso se supone que **cada opción se repite indefinidamente** y
se calcula un valor anual equivalente.

## Valor Anual Equivalente (VAE) y CAE

Se reparte el VAN de cada opción como una anualidad equivalente a `n` años:

```
VAN = VAE × factor(n, i)        →        VAE = VAN / factor(n, i)
```

donde `factor(n, i)` es el factor de [[../03-valor-del-dinero-en-el-tiempo/anualidades|anualidad]]
a `n` años y tasa `i`. Cuando el VAN tiene **solo costos** (es negativo), el VAE se llama **Costo
Anual Equivalente (CAE)**, y el objetivo es **minimizar el CAE** (= maximizar el VAE negativo).

## Ejemplo

Máquina: adquisición $1.000, O&M del 1.er año $110 creciendo $50/año, tasa 10%, sin IG. Se calcula
el VAN de cada opción de recambio y luego su CAE:

| Año recambio (n) | 1    | 2    | 3    | 4    | 5    | 6    | **7** | 8    | 9    | 10   |
|------------------|------|------|------|------|------|------|-------|------|------|------|
| VAN(10%)         | −485 | −869 |−1.184|−1.456|−1.702|−1.933|−2.157 |−2.378|−2.596|−2.813|
| factor(n,10%)    | 0,9  | 1,7  | 2,5  | 3,2  | 3,8  | 4,4  | 4,9   | 5,3  | 5,8  | 6,1  |
| **CAE**          | −534 | −500 | −476 | −459 | −449 | −444 |**−443**| −446 | −451 | −458 |

El CAE **baja hasta el año 7** y después vuelve a subir. La **vida económica** que minimiza el
Costo Anual Equivalente es de **7 años**.

```
CAE │ −534
    │    ╲                       ╱
    │     ╲___                __╱
    │         ╲___        ___╱
    │             ╲──●──╱      ← mínimo en n = 7 (−443)
    └────┬────┬────┬────┬────┬──── n (años de uso)
         1    3    5    7    9
```

> El caso resuelto completo (armado de los VAN de cada opción) está en
> `practica/ejercicios/caso-04-evaluacion-de-proyectos.md`.

> Apunte EPI, Parte 4 — Evaluación de Proyectos (4.9), doc p. 74–77.
