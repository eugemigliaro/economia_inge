# Guía 5 — Contabilidad, amortizaciones, escudo fiscal e índices

> Resolución de la Guía 5 (transcrita de `Economía - Guía 5.xlsx`). 7 ejercicios que cubren
> casi toda la **Unidad 1 — Contabilidad** y tocan inventarios (Unidad 2 — Costos).

---

## Ejercicio 1 — Partida doble y armado del balance + cuadro de resultados

Se parte de un balance inicial y se registran ~9 operaciones por **partida doble**
(↑A / ↓P / ↓PN van al DEBE; ↓A / ↑P / ↑PN van al HABER), para llegar al balance final y al
cuadro de resultados.

**Balance inicial → final** (en $):

| | Inicial | Final |
|---|---|---|
| **Activos** | | |
| Disponibilidades | 200 | 80 |
| Inversiones | 600 | 200 |
| Créditos por ventas | 300 | 450 |
| Bienes de cambio (200 u) | 550 | 525 |
| Bienes de uso (V.O.) | 3500 | 3500 |
| Amortizaciones acum. | −250 | −330 |
| **Total activo** | **4900** | **4425** |
| **Pasivos** | | |
| Proveedores | 550 | 300 |
| Sueldos y cargas a pagar | 170 | 130 |
| Gastos varios a pagar | 80 | 140 |
| Deuda bancaria | 400 | 200 |
| **Total pasivo** | **1200** | **770** |
| **PN** | | |
| Capital | 3300 | 3300 |
| Resultados acumulados | 400 | 355 |
| **Total PN** | **3700** | **3655** |

**Cuadro de resultados:**

```
Ventas                 400
Costo de ventas       -275
─────────────────────────
Utilidad bruta         125
Sueldos               -100
Gastos varios          -60
Amortización           -80
─────────────────────────
Utilidad operativa    -115
Resultado extraord.   +100   ← venta del bono que tenía como inversión
─────────────────────────
Utilidad neta          -15
```

**Caso 5 (valuación de inventarios).** Existencia inicial 200 u @ 2,75 = 550; compras 100 u
@ 2,50 = 250; se venden 100 u, pero no sabemos *cuáles* salen. Tres métodos:

| Método | Sale (costo de ventas) | Queda (existencia) |
|---|---|---|
| **FIFO** ← elegido | 275 | 525 |
| Promedio ponderado | 266,67 | 533,33 |
| LIFO | 250 | 550 |

**Caso 7.** La empresa **ya tenía** bonos como inversión y los vende → el resultado es
**extraordinario**, no es que los emite como deuda (no es financiación).

**Concepto que se evalúa:** partida doble y ecuación patrimonial; cuadro de resultados;
distinción resultado operativo vs. extraordinario; métodos de valuación de inventario.
Teoría en [`partida-doble.md`](../../apuntes/economia-empresarial/01-contabilidad/partida-doble.md),
[`ecuacion-patrimonial.md`](../../apuntes/economia-empresarial/01-contabilidad/ecuacion-patrimonial.md),
[`cuadro-de-resultados.md`](../../apuntes/economia-empresarial/01-contabilidad/cuadro-de-resultados.md).

---

## Ejercicio 2 — Amortización y resultado por venta de bienes de uso

Tres bienes; para cada uno se calcula la amortización acumulada, el valor de libros y el
resultado por venta.

| | Muebles | Equipos | Terrenos |
|---|---|---|---|
| Valor de mercado | 80 | 120 | 300 |
| Valor original | 80 | 80 | 240 |
| Vida útil (años) | 5 | 10 | — |
| Años transcurridos | 5 | 5 | 5 |
| Amortizaciones acum. | 80 | 40 | 0 |
| **Valor de libros** | 0 | 40 | 240 |
| **Resultado por venta** | **80** | **80** | **60** |

```
Amort. acumulada = años × (valor original / vida útil)
Valor de libros  = valor original − amort. acumulada
Resultado venta  = valor de mercado − valor de libros
```

El **terreno no tiene vida útil** → no se amortiza (amort. acum. = 0).

**Concepto que se evalúa:** amortización de bienes de uso, valor de libros y resultado por
venta. Teoría en [`valor-de-mercado-vs-valor-de-libros.md`](../../apuntes/economia-empresarial/01-contabilidad/valor-de-mercado-vs-valor-de-libros.md).

---

## Ejercicio 3 — Dos formas de deducir la amortización (escudo fiscal y timing)

Un bien de 1.000.000, vida útil 10 años, valor residual 100.000, IG = 35 %. Se comparan dos
formas de imputar la deducción:

- **Deducción I:** amortización lineal, `(1.000.000 − 100.000)/10 = 90.000`/año durante 10 años.
- **Deducción II:** deducir todo de golpe en el año 0 (1.000.000).

| Año | 0 | 1..10 | Total |
|---|---|---|---|
| Deducción I | 0 | 90.000 c/u | 900.000 |
| Deducción II | 1.000.000 | 0 | 1.000.000 |
| Δ (II − I) | +1.000.000 | −90.000 c/u | 100.000 |
| 35 % × Δ (ahorro de IG) | +350.000 | −31.500 c/u | 35.000 |

El **total** de impuesto ahorrado es el mismo, pero la deducción II adelanta el ahorro al año 0
→ por el valor tiempo del dinero, **conviene deducir antes** (mayor VAN del escudo fiscal).

**Concepto que se evalúa:** escudo fiscal de la amortización y efecto del *timing* en el VTD.
Se reusa en la Guía 7 (evaluación de proyectos). Teoría en
[`cuadro-de-resultados.md`](../../apuntes/economia-empresarial/01-contabilidad/cuadro-de-resultados.md)
y [`armado-del-flujo-del-proyecto.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/armado-del-flujo-del-proyecto.md).

---

## Ejercicio 4 — Intereses devengados (empresa vs. banco)

Operación a tasa 10 %: ingreso 2.000.000 en el año X; pagos de −200.000 (X+2) y −2.200.000
(X+3). Se separa el **devengamiento** de intereses del flujo de caja.

| Año | X | X+1 | X+2 | X+3 |
|---|---|---|---|---|
| Ingreso / pago | +2.000.000 | 0 | −200.000 | −2.200.000 |
| Intereses devengados | 0 | 200.000 | 200.000 | 0 |
| Utilidad empresa | 0 | −200.000 | −200.000 | 0 |
| Utilidad banco | 0 | +200.000 | +200.000 | 0 |

Los intereses se **devengan** en el período en que se generan (X+1 y X+2), con independencia
de cuándo se cobran/pagan. Lo que es gasto para la empresa es ingreso para el banco.

**Concepto que se evalúa:** principio de devengado vs. percibido. Teoría en
[`operaciones-basicas.md`](../../apuntes/economia-empresarial/01-contabilidad/operaciones-basicas.md).

---

## Ejercicio 5 — Reconstruir balance y cuadro de resultados a partir de índices

Dados varios índices, se reconstruye el balance completo y el cuadro de resultados.

**Datos (índices):** cobertura de intereses 8; liquidez corriente 1,4; liquidez seca 1,0;
liquidez absoluta 0,2; deuda LP/capital 0,5; ROE 0,4; índice de existencia 72 días; plazo
prom. de crédito 90 días; año = 360 días.

**Balance resuelto** (en $):

| Activo | | Pasivo + PN | |
|---|---|---|---|
| Disponibilidades | 11 | Deudas comerciales | 30 |
| Créditos por ventas | 44 | Deudas bancarias | 25 |
| Bienes de cambio | 22 | **Pasivo corriente** | **55** |
| **Activo corriente** | **77** | Deuda a largo plazo | 20 |
| Activo fijo neto | 38 | Capital | 40 |
| **Total** | **115** | **Total** | **115** |

**Cuadro de resultados resuelto:** Ventas 176 · CMV 110 · Gastos com. y adm. 10 · Amort. 20 →
EBIT 36 · Intereses 4,5 · UAI 31,5 · IG 15,5 · **Utilidad neta 16**.

**Fórmulas usadas (orden de despeje):**

```
Pasivo corriente          = deuda comercial + bancaria
Liquidez corriente        = AC / PC                       → AC = 1,4 · 55 = 77
Liquidez seca             = (AC − inventario) / PC        → inventario (BdC) = 22
Liquidez absoluta         = disponibilidades / PC          → disp = 0,2 · 55 = 11
Créditos x ventas         = AC − disp − inventario
Activo fijo neto          = total activo − AC
Deuda LP + capital        = total − PC = 60 ;  Deuda LP/Capital = 0,5  → Deuda LP = 0,5·Capital
Índice de existencia      = (inventario prom / CMV) · 360
Plazo prom. de crédito    = (CxV / ventas) · 360
EBIT                      = ventas − CMV − gastos − amort.
Cobertura de intereses    = EBIT / intereses
UAI                       = EBIT − intereses
Utilidad neta             = ROE · PN          (acá PN = capital)
IG                        = UAI − utilidad neta
```

**Concepto que se evalúa:** análisis por índices (liquidez, endeudamiento, actividad,
rentabilidad) y reconstrucción de estados a partir de ratios. Teoría en
[`analisis-por-indices.md`](../../apuntes/economia-empresarial/01-contabilidad/analisis-por-indices.md).

---

## Ejercicio 6 — Cobertura de intereses (¿le renuevan el préstamo?)

**Datos:** deuda 500.000 al 10 % → intereses 50.000; ventas 2.000.000; IG 30 %; margen
utilidad/ventas 5 %.

```
Utilidad neta = (margen) · ventas = 0,05 · 2.000.000 = 100.000
Utilidad neta = (EBIT − intereses) · (1 − IG)  →  EBIT = UN/(1−IG) + intereses = 192.857
Cobertura     = EBIT / intereses = 192.857 / 50.000 = 3,86
```

Como la cobertura **3,86 < 5**, no le renovarían el préstamo.

**Concepto que se evalúa:** índice de cobertura de intereses como señal de riesgo crediticio.
Teoría en [`analisis-por-indices.md`](../../apuntes/economia-empresarial/01-contabilidad/analisis-por-indices.md).

---

## Ejercicio 7 — Capital de trabajo y necesidad de financiamiento

Balance dado (AC 2500, PC 1900, BU 4500, PN 2900...). Se analiza qué pasa al crecer las ventas.

- **a) Capital de trabajo** = AC − PC = 2500 − 1900 = **600**.
- **b)** Si las ventas pasan a 6000, CxV y BdC crecen proporcionalmente:
  CxV 1200→1440 (+240), BdC 900→1080 (+180) → **+420** de activos operativos.
- **c)** La deuda comercial (compras) crece 1100→1320 → **+220** de financiamiento espontáneo.
- **d) Necesidad neta** = activos adicionales − pasivos adicionales = 420 − 220 = **200**.
- **e)** Ese extra de 200 es una **necesidad operativa de corto ciclo** → se financia con
  **deuda de corto plazo**. Si las ventas no se sostienen, CxV y BdC bajan y la necesidad
  desaparece; tomar deuda de largo plazo dejaría pagando intereses innecesarios.

**Concepto que se evalúa:** capital de trabajo, necesidades operativas de fondos (NOF) y
calce de plazos (corto con corto). Teoría en
[`ciclo-de-caja-y-nof.md`](../../apuntes/economia-empresarial/01-contabilidad/ciclo-de-caja-y-nof.md).
