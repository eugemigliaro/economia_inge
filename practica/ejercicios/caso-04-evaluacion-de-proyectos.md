# Caso 04 — Evaluación de proyectos (RL S.A.)

> **Enunciado (Apunte EPI, Parte 4 — Evaluación de Proyectos, 4.8, doc p. 68–74):**
> RL S.A. evalúa un proyecto a **12 años** para comercializar un producto nuevo.
>
> - Ventas constantes: **1.000 u/año** a **1 $/u**.
> - Costo variable: **0,5 $/u**. Costos fijos propios del proyecto: **100 $/año**.
> - El Gerente de Administración prorratea **50 $/mes** de sueldos de oficinas centrales (CEO/CFO).
> - Tabla de equipos del fabricante:
>
>   | Unidades  | Inversión | Vida técnica | Valor rezago técnico |
>   |-----------|-----------|--------------|----------------------|
>   | 1–800     | 200 $     | 3 años       | 31 $                 |
>   | 800–1200  | 300 $     | 6 años       | 51 $                 |
>   | 1200–1800 | 400 $     | 7 años       | 61 $                 |
>
> - Se instalan en 200 m² desocupados de la planta (alquiler 0,2 $/m²-año), **que no puede
>   destinarse a otros usos** por seguridad.
> - Amortización: vida fiscal/contable **5 años**, valor de rezago fiscal **10%** del valor original.
> - Inversión en Kt (Bienes de Cambio): **100 $** al inicio; al final se recupera el **80%**.
> - IG: **35%/año**, pagado el mismo año en que se devenga.
> - Canibalización: el producto a canibalizar (−75 $ de ingresos netos) estará **discontinuado**
>   desde el período 1.
> - Investigación: 150 $ comprometidos (50 $ en año −1, 50 $ en t=0, 50 $ en t=1).
> - Costo de oportunidad del dinero: **20% anual**.
>
> **Se pide:** a) armar el flujo de fondos; b) evaluar con VAN, TIR, TER, PRS y PRCA.

## Paso 1 — Ordenar los datos (qué entra y qué no)

Acá se aplica el [[../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/conceptos-clave|análisis marginal]]:

| Dato | ¿Entra al flujo? | Por qué |
|------|------------------|---------|
| Ventas 1.000 u × 1 $ | **Sí** | son del proyecto |
| Canibalización −75 $ | **No** | el otro producto ya está discontinuado → no hay superposición, no se hace efectiva |
| Costo variable 1.000 u × 0,5 $ | **Sí** | marginal |
| Costos fijos propios 100 $/año | **Sí** | existen gracias al proyecto |
| Prorrateo 50 $/mes oficinas centrales | **No** | se pagan con o sin proyecto → costo hundido, no marginal |
| Alquiler del espacio | **No** | el espacio no puede destinarse a otro uso → no hay costo de oportunidad |
| Investigación 150 $ | **No** | comprometida se haga o no el proyecto → costo hundido |

**Inversión en BU:** para 1.000 u/año conviene la máquina de **800–1200 u (300 $)**. Comprar dos
de 800 u sería más caro en precio y en vida útil. La vida **técnica** es 6 años → hay que
**recomprar** la máquina al final del año 6 (otra inversión de 300 $).

**Amortización** (vida fiscal 5 años, rezago fiscal 10% × 300 = 30):

```
A = (Valor Original − Valor Rezago) / vida = (300 − 30) / 5 = 54 $/año
```

## Paso 2 — Cuadros de resultados operativos y FEO

Todos los años son iguales salvo el **6 y el 12**: la máquina dura 6 años pero se amortiza en 5,
así que en los años 6 y 12 ya **no hay amortización**.

| Concepto | Años 1–5, 7–11 | Años 6 y 12 |
|----------|----------------|-------------|
| Ventas   | 1.000          | 1.000       |
| CV       | −500           | −500        |
| CF       | −100           | −100        |
| A        | −54            | **0**       |
| UAIG     | 346            | 400         |
| IG (35%) | −121           | −140        |
| U neta   | 225            | 260         |

FEO por enfoque ascendente (`FEO = U neta + A`):

```
FEO (años 1–5 y 7–11) = 225 + 54 = 279
FEO (años 6 y 12)     = 260 + 0  = 260
```

## Paso 3 — Cuadros extraordinarios y FEE

**Reventa de BU (fin de años 6 y 12).** VM = 51; VL = valor de rezago técnico = 30 (al venderla
ya está totalmente amortizada):

```
VM    51
VL   −30
UAIG  21
IG    −7
Uneta 14    →    FEE BU = U neta + VL = 14 + 30 = 44   (años 6 y 12)
```

**Recupero de Kt (fin de año 12).** Inversión 100, se recupera el 80% → VM = 80:

```
VM     80
VL   −100
UAIG  −20
IG      7     (la pérdida genera crédito fiscal)
Uneta −13    →    FEE Kt = U neta + VL = −13 + 100 = 87   (año 12)
```

## Paso 4 — Flujo de fondos neto (FFN)

| Año | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 |
|-----|---|---|---|---|---|---|---|---|---|---|----|----|----|
| Inv BU | −300 | | | | | | −300 | | | | | | |
| Inv Kt | −100 | | | | | | | | | | | | |
| FEO | | 279 | 279 | 279 | 279 | 279 | 260 | 279 | 279 | 279 | 279 | 279 | 260 |
| FEE BU | | | | | | | 44 | | | | | | 44 |
| FEE Kt | | | | | | | | | | | | | 87 |
| **FFN** | **−400** | 279 | 279 | 279 | 279 | 279 | **4** | 279 | 279 | 279 | 279 | 279 | **391** |

> Año 6: 260 + 44 − 300 (recompra) = **4**.  Año 12: 260 + 44 + 87 = **391**.

## Paso 5 — Evaluación

Tasa de descuento = 20%.

- **VAN:** traer todo el FFN a hoy al 20% → **VAN = 758 > 0 → se acepta.**
- **TIR:** tasa que anula el VAN → **TIR = 68% > 20% → se acepta.**
- **TER / TIRM:** capitalizar al año 12 todos los FFN positivos (todos salvo el de t=0). Quedan
  dos flujos: −400 en t=0 y **10.329** en t=12.

  ```
  VAN(TER) = 0 = −400 + 10.329 / (1+TER)^12   →   TER = 31% anual
  ```

- **PRS (Payback Simple):** acumular el FFN sin descontar.

  | Año | 0 | 1 | 2 |
  |-----|---|---|---|
  | FFN | −400 | 279 | 279 |
  | FF Acum | −400 | −121 | 158 |

  Se recupera **durante el año 2**. Regla de tres: `121/279 × 12 ≈ 5,2 meses ≈ 0,4 años`.
  **PRS ≈ 1,4 años (1 año y 5 meses).**

- **PRCA (Payback Compuesto/Actualizado):** acumular el **valor actual** de los FFN al 20%.

  | Año | 0 | 1 | 2 |
  |-----|---|---|---|
  | FFN | −400 | 279 | 279 |
  | VA(FFN) | −400 | 232 | 194 |
  | VA Acum | −400 | −168 | 26 |

  Se recupera **durante el año 2**. Regla de tres: `168/232 × 12 ≈ 10,4 meses ≈ 0,9 años`.
  **PRCA ≈ 1,9 años (1 año y 10 meses).**

## Concepto que se evalúa

Caso integrador de la unidad: combina
[[../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/flujos-de-fondos|cálculo de flujos de fondos]]
(FEO, FEE, enfoque ascendente),
[[../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/conceptos-clave|análisis marginal / costos hundidos / costo de oportunidad]]
y los cuatro criterios:
[[../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/van|VAN]],
[[../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/tir|TIR]],
[[../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/tirm|TER/TIRM]] y
[[../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/payback|payback simple y descontado]].
