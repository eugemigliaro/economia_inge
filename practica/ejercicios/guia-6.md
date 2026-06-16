# Guía 6 — Valor del dinero en el tiempo

> Resolución de la Guía 6 (transcrita de `Economía - Guía 6.xlsx`). 10 ejercicios sobre
> **Unidad 3 — El Valor del Dinero en el Tiempo** (tasas, anualidades, perpetuidades,
> préstamos, inflación y comparación de financiamiento). Es la primera práctica de esta unidad.

---

## Ejercicio 1 — Tasas equivalentes y cuota de préstamo

Dos bancos con distinta capitalización. Banco A: TNA 14 %, capitaliza mensual (12 períodos).
Banco B: TNA 18 %, capitaliza trimestral (4 períodos).

**a) Tasas equivalentes:**

```
TEM_A = TNA/12 = 0,01167
TEM_B = (1 + TNA/4)^(1/3) − 1 = 0,01478     ← se baja la trimestral a mensual
TEA_A = (1 + TEM_A)^12 − 1 = 14,93 %
TEA_B = (1 + TEM_B)^12 − 1 = 19,25 %
```

**b) Cuota** de un préstamo de 5.000 a 24 cuotas (anualidad ordinaria, `C = i·PV / (1−(1+i)^−n)`):

- Cuota Banco A = **240,06**
- Cuota Banco B = **248,98**

→ Conviene el Banco A (menor TEA y menor cuota).

**Concepto que se evalúa:** tasas nominales vs. efectivas, equivalencia entre frecuencias de
capitalización, cuota de una anualidad. Teoría en
[`tipos-de-tasas.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/tipos-de-tasas.md),
[`anualidades.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/anualidades.md).

---

## Ejercicio 2 — Ahorro periódico para distintos objetivos (perpetuidades y anualidades)

Tasa 10 %, se ahorra durante 10 años (factor de acumulación `S = ((1+i)^10 − 1)/i = 15,937`).
El objetivo es financiar un cobro de 100.000. Se calcula cuánto hay que ahorrar por año
`A = PV/S` según qué se quiere financiar.

| Caso | Objetivo | PV | Ahorro anual A |
|---|---|---|---|
| A | Perpetuidad simple: `PV = C/i` | 1.000.000 | 62.745 |
| B | Perpetuidad creciente (g = 2 %): `PV = C/(i−g)` | 1.250.000 | 78.432 |
| C | Anualidad 20 años: `PV = C·(1−(1+i)^−20)/i` | 851.356 | 53.419 |

**Concepto que se evalúa:** valor presente de perpetuidades (simple y creciente) y
anualidades, y factor de acumulación de un ahorro periódico. Teoría en
[`perpetuidades.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/perpetuidades.md),
[`anualidades.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/anualidades.md).

---

## Ejercicio 3 — ¿Vender ahora o alquilar y vender después?

Venta hoy = 100.000. Alternativa: alquilar 15.000/año durante 3 años y vender al final por
80.000. Tasa de descuento 9 %.

```
VP alquiler (anualidad 3 años) = 15.000·(1−(1+i)^−3)/i = 37.969
VP venta final                 = 80.000/(1+i)^(3+1)     = 56.674
VP total alternativa           = 94.643   <  100.000     → conviene vender ahora
```

**Pregunta adicional:** si además se pudiera alquilar un 4.º "mes" extra, el VP nuevo
(94.643 + 10.626 = **105.270**) supera los 100.000 → ahí sí conviene alquilar y vender después.

**Concepto que se evalúa:** comparación de alternativas por valor actual, anualidades y
descuento de un valor terminal. Teoría en
[`valor-actual.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/valor-actual.md).

---

## Ejercicio 4 — Sistema francés y refinanciación

Préstamo 3.000.000, 60 cuotas, tasa 2 % mensual, **sistema francés** (cuota constante).

```
Cuota = i·PV/(1−(1+i)^−n) = 86.303,90
Cuota 1:  interés = 60.000   amort = 26.303,90   saldo = 2.973.696
Cuota 2:  interés = 59.474   amort = 26.830       (la amortización crece, el interés baja)
```

A los 20 meses la deuda pendiente es
`D = PV·(1+i)^t − C·((1+i)^t − 1)/i = 2.360.884`.

Se refinancia ese saldo a nueva tasa 2,5 %:
- Si se mantienen **40 cuotas**: nueva cuota = **94.048,74**.
- Si se mantiene la cuota y cambia la tasa: el plazo pasa a `n = −ln(1 − i'·D/C)/ln(1+i') ≈ 46,6`
  meses.

**Concepto que se evalúa:** sistema francés (composición interés/amortización), saldo
pendiente y refinanciación. Teoría en
[`tipos-de-prestamos.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/tipos-de-prestamos.md).

---

## Ejercicio 5 — Plan de pagos irregular (cuotas con refuerzo)

Venta de 200 en 8 cuotas, TNA 12 % → TE trimestral 3 %. Las cuotas no son iguales: valen `X`,
salvo la 4.ª y la 8.ª que valen `X + 2X = 3X` (refuerzos). Se descuenta cada cuota por su
factor `(1+i)^−n` y se iguala al precio de contado para despejar `X`.

```
Suma de factores agrupada → Término1 + Término2 + Término3 = 10,375
Monto base X = 200/10,375 = 19,28
Pago del 4.º trimestre (refuerzo, 3X) = 57,83
```

**Concepto que se evalúa:** valor presente de un flujo de cuotas irregulares; descuento
término a término. Teoría en
[`anualidades.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/anualidades.md),
[`valor-actual.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/valor-actual.md).

---

## Ejercicio 6 — Cancelación anticipada y ahorro de intereses

30 cuotas de 10.000 al 6 %. `Monto = C·(1−(1+i)^−n)/i = 137.648`.

Tras pagar 12 cuotas, el saldo es `S = C·(1−(1+i)^−18)/i = 108.276`. Se hace un **pago extra**
del 50 % del saldo (54.138) y se recalcula la cuota para las 18 restantes:

```
Nueva cuota = 0,5·saldo·i/(1−(1+i)^−18) = 5.000
Pagos totales realizados = 264.138
Intereses pagados        = 264.138 − 137.648 = 126.490
Intereses sin pago extra = 30·10.000 − 137.648 = 162.352
Ahorro por el pago extra = 35.862
```

**Concepto que se evalúa:** saldo pendiente, cancelación parcial anticipada y ahorro de
intereses. Teoría en
[`tipos-de-prestamos.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/tipos-de-prestamos.md).

---

## Ejercicio 7 — TIR/costo efectivo de un crédito con comisión y flujo irregular

Crédito de 100 con comisión 2 (se recibe neto 98) y 2 cuotas de 50, TNA 20 %.
El flujo semestral es `{+98, −10, −60, −5, −55}` a 0; 0,5; 1; 1,5; 2 años. La consigna fija
TE semestral ≈ 11 %, y se anualiza:

```
TEA = (1 + TE_sem)^2 − 1 = (1,11)^2 − 1 = 23,21 %
```

→ El costo efectivo real del crédito (con comisión) es bastante mayor que la TNA del 20 %.

**Concepto que se evalúa:** costo financiero total / tasa efectiva de un flujo irregular;
efecto de las comisiones. Teoría en
[`tipos-de-tasas.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/tipos-de-tasas.md).

---

## Ejercicio 8 — Tasa real (descontar la inflación)

**a)** Tasa de 2 % a 30 días, escalada a 80 días: `(1,02)^(80/30) − 1 = 5,42 %`; anualizada
da TR anual ≈ 4,00 %.

**b)** TNA 7 % con capitalización semestral (2/año):

```
TEA = (1 + TNA/2)^2 − 1 = 7,1225 %
Inflación = 3 %
1 + TReal = (1 + TEf)/(1 + Infl)  →  TReal ≈ 4,00 %        (anual)
TReal a 30 días = 0,323 %
```

> La fórmula de Fisher se aplica con tasas **efectivas**, no nominales: hay que pasar primero
> la nominal a efectiva y recién ahí dividir por la inflación.

**Concepto que se evalúa:** tasa real vs. nominal (ecuación de Fisher), inflación. Teoría en
[`inflacion-y-tasas.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/inflacion-y-tasas.md).

---

## Ejercicio 9 — Comparar fuentes de financiamiento por su valor presente

Compra de 710.000 financiada con varias fuentes; costo de oportunidad 3,25 % mensual. Se
trae cada fuente a valor presente y se compara contra pagar al contado.

- **HSBC (método alemán, amortización constante):** saldo 100.000 que baja 25.000/mes, interés
  3 % sobre saldo → cuotas decrecientes (28.000; 27.250; ...). `PV(HSBC) = 99.413`.
- **RIO (francés):** 200.000 al 2,5 %, 6 meses → cuota 36.310; sumando los 6 PV → `PV(RIO) = 195.079`.
- **Crédito proveedor:** 30.000 al 3,5 % a 3 meses → monto a pagar 33.150; `PV = 29.169`.
- **Financiamiento propio:** el resto.

```
PV total de los préstamos = 703.661  <  710.000  → conviene financiar (no pagar al contado)
```

**Concepto que se evalúa:** comparación de financiamiento por valor presente; sistema alemán
vs. francés; costo de oportunidad como tasa de descuento. Teoría en
[`tipos-de-prestamos.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/tipos-de-prestamos.md),
[`valor-actual.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/valor-actual.md).

---

## Ejercicio 10 — Deuda como suma de varios flujos descontados

La deuda total es la suma de los valores presentes de tres componentes, con TNA 6 % → TEM 0,5 %:

| Componente | Descripción | PV |
|---|---|---|
| Pagos base | anualidad ordinaria de 50 por 17 meses | 812,93 |
| Refuerzos | 80 cada uno, 5 pagos cada 3 meses | 382,53 |
| Pago final | 95,25 en el mes 18 | 87,07 |
| **Deuda total** | suma de los PV | **1.282,53** |

**Concepto que se evalúa:** descomposición de un plan de pagos complejo en anualidades +
pagos puntuales y su valor presente. Teoría en
[`anualidades.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/anualidades.md),
[`valor-actual.md`](../../apuntes/economia-empresarial/03-valor-del-dinero-en-el-tiempo/valor-actual.md).
