# Interés: compuesto y simple

El **interés** es lo que rinde un capital invertido a lo largo del tiempo. Según qué pase
con los intereses ganados, hay dos esquemas: **compuesto** (se reinvierten) y **simple**
(se retiran).

La intuición base: si invierto $100 al 10% anual, en un año tengo $110. Entonces, suponiendo
que puedo invertir mi dinero, **$100 de hoy equivalen a $110 dentro de un año**, y a la
inversa, **$100 dentro de un año equivalen a ≈ $91 de hoy**.

```
HOY            EN UN AÑO
$100 ── ×(1+10%) ──▶ $110     (capitalizar: llevo al futuro)
$91  ◀── /(1+10%) ── $100     (descontar: traigo al presente)
```

## Interés compuesto

Los intereses **no se retiran**: se suman al capital y generan a su vez nuevos intereses
("interés sobre interés").

```
VF = VP × (1 + i)^n
```

- `VP` = valor presente (inversión inicial)
- `VF` = valor futuro (saldo final)
- `i` = tasa de interés efectiva del período
- `n` = cantidad de períodos
- Interés total: `I = VF − VP`

Cualquiera de las variables puede ser dato o incógnita.

**Ejemplo — $1000 al 10% anual, 3 años:**

| Año           | 0    | 1    | 2    | 3    |
|---------------|------|------|------|------|
| Saldo inicial | 0    | 1000 | 1100 | 1210 |
| Interés       | 0    | 100  | 110  | 121  |
| Saldo final   | 1000 | 1100 | 1210 | 1331 |

`VF = 1000 × (1+10%)^3 = 1331` → interés total `I = 331`.

Como la tasa está elevada a la `n`, **una pequeña diferencia de tasa causa una gran
variación** en el monto futuro.

## Interés simple

Los intereses **se retiran** cada período, así que siempre se calculan sobre el **mismo
capital original**. No hay interés sobre interés.

```
VF = VP × (1 + i × n)
```

- Interés total: `I = VP × i × n`

**Ejemplo — $1000 al 10% anual, 3 años:**

| Año             | 0    | 1    | 2    | 3    |
|-----------------|------|------|------|------|
| Saldo inicial   | 0    | 1000 | 1000 | 1000 |
| Interés         | 0    | 100  | 100  | 100  |
| Saldo fin de año| 1000 | 1000 | 1000 | 1000 |

A los 3 años: `VF = 1000 × (1 + 10%×3) = 1300`. Cada año se cobran $100 y se sacan del juego.

## Compuesto vs. simple

Mismo capital, misma tasa, mismos 3 años: el compuesto da **$1331** y el simple **$1300**.
La diferencia ($31) son los "intereses sobre los intereses" que el simple no genera, y crece
fuerte a medida que aumenta `n`.

> Convención de la materia: los flujos ocurren **al final** de cada período.

> Apunte EPI, Parte 3 — El Valor del Dinero en el Tiempo (3.2), doc p. 46–48.
