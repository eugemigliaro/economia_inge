# Tipos de préstamos (sistemas de amortización)

Dado un préstamo `P`, según **cómo se devuelve el capital** y **sobre qué base se calculan
los intereses**, hay distintos sistemas de amortización. Vocabulario base:

- **Amortización (A):** la parte de la cuota que devuelve capital.
- **Interés (I):** lo que se paga por la deuda viva del período.
- **Cuota (C):** lo que se paga en total cada período → `C = A + I`.

En todos, la suma de las amortizaciones a lo largo de la vida del préstamo es `P`.

## Resumen de los cuatro sistemas

| Sistema  | Qué es constante        | Cuota          | Interés                  |
|----------|-------------------------|----------------|--------------------------|
| Francés  | la **cuota**            | constante      | sobre saldo (decreciente)|
| Alemán   | la **amortización**     | decreciente    | sobre saldo (decreciente)|
| Directo  | cuota, amort. e interés | constante      | sobre `P` (constante)    |
| Bullet   | el **interés**          | mínima, salto final | sobre `P` (constante)|

## Sistema Francés — cuota constante (interés sobre saldos)

La cuota es fija; al principio se paga mucho interés y poco capital, y eso se va invirtiendo.

```
C = P / Factor(n, i) = constante      (Factor = el de la anualidad)
I_t = (saldo de deuda) × i
A_t = C − I_t
```

## Sistema Alemán — amortización constante (interés sobre saldos)

Se devuelve siempre la misma porción de capital; como el interés cae con el saldo, la cuota
**decrece**.

```
A = P / n = constante
I_t = (saldo de deuda) × i
C_t = A + I_t
```

## Sistema Directo — cuota constante, interés sobre el capital original

Amortización constante e interés **siempre sobre `P`** (no sobre el saldo), así que la cuota
también es constante. Se paga más interés que en el alemán, porque no baja con la deuda.

```
A = P / n = constante
I = P × i = constante
C = A + I = constante
```

## Sistema Bullet — todo el capital al final

Durante la vida del préstamo solo se pagan intereses; el capital se devuelve íntegro en la
última cuota.

```
I = P × i = constante
A = P  (todo al final)
```

## Ejemplo numérico — Préstamo 1000, TEA 10%, n = 4 años

**Francés** — Factor = 3.17 → Cuota = `1000 / 3.17 = 315.47`

| Año              | 1     | 2     | 3     | 4     |
|------------------|-------|-------|-------|-------|
| Cuota pagada     | 315.5 | 315.5 | 315.5 | 315.5 |
| Interés pagado   | 100.0 | 78.5  | 54.8  | 28.7  |
| Capital pagado   | 215.5 | 237.0 | 260.7 | 286.8 |
| Saldo de capital | 784.5 | 547.5 | 286.8 | 0.0   |

**Alemán** — Amortización = `1000 / 4 = 250`

| Año              | 1     | 2     | 3     | 4     |
|------------------|-------|-------|-------|-------|
| Capital pagado   | 250.0 | 250.0 | 250.0 | 250.0 |
| Interés pagado   | 100.0 | 75.0  | 50.0  | 25.0  |
| Cuota pagada     | 350.0 | 325.0 | 300.0 | 275.0 |
| Saldo de capital | 750.0 | 500.0 | 250.0 | 0.0   |

**Directo** — Amortización = `250`, Interés = `1000 × 10% = 100` (fijo)

| Año              | 1     | 2     | 3     | 4     |
|------------------|-------|-------|-------|-------|
| Capital pagado   | 250.0 | 250.0 | 250.0 | 250.0 |
| Interés pagado   | 100.0 | 100.0 | 100.0 | 100.0 |
| Cuota pagada     | 350.0 | 350.0 | 350.0 | 350.0 |
| Saldo de capital | 750.0 | 500.0 | 250.0 | 0.0   |

**Bullet** — Interés = `100` (fijo), Amortización = `1000` al final

| Año              | 1      | 2      | 3      | 4      |
|------------------|--------|--------|--------|--------|
| Capital pagado   | 0      | 0      | 0      | 1000   |
| Interés pagado   | 100.0  | 100.0  | 100.0  | 100.0  |
| Cuota pagada     | 100.0  | 100.0  | 100.0  | 1100.0 |
| Saldo de capital | 1000.0 | 1000.0 | 1000.0 | 0.0    |

> El factor del sistema francés es el mismo de las [[anualidades]] (la cuota es una anualidad
> cuyo VP es el préstamo). La tasa `i` debe ser efectiva del período de la cuota — ver
> [[tipos-de-tasas]].

> Apunte EPI, Parte 3 — El Valor del Dinero en el Tiempo (3.7), doc p. 52–56.
