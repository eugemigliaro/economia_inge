# Guía 7 — Evaluación de proyectos (flujo de fondos y VAN)

> Resolución de la Guía 7 (transcrita de `Economía - Guía 7.xlsx`). 7 ejercicios sobre
> **Unidad 4 — Evaluación de Proyectos**: armado del cuadro de resultados, flujo de fondos,
> escudo fiscal, valor residual, capital de trabajo y VAN.

**Esquema común a todos los ejercicios.** Se arma primero el **cuadro de resultados**
(EBITDA → resta amortización fiscal → EBIT → resta IG → utilidad neta) y luego el **flujo de
fondos**, partiendo del EBITDA y sumando/restando las partidas no operativas (inversión en BU,
capital de trabajo Kt, ventas de activos y el IG efectivo). Se descuenta a la TREMA para el VAN.

> Conceptos clave que se repiten:
> - **VRC** = valor residual contable (fiscal); **VRT/VRM** = valor residual técnico / de mercado.
> - **Resultado por venta de un activo** = valor de mercado − valor de libros → genera IG extra.
> - **Kt** (capital de trabajo): sale al inicio (−) y se recupera al final (× factor de recupero).
> - **Costo hundido**: no entra al flujo (ya está comprometido).

---

## Ejercicio 1 — VAN con venta de BU y Kt al cierre

Inversión BU 1.000 (VU contable 10, técnica 3), VRC fiscal 400, VRM 800, Kt 100 (recupero 0,8),
EBITDA 550/año, IG 30 %, TREMA 10 %. Amort. fiscal anual = 1.000/10 ... (se usa la VU contable
para amortizar; el proyecto dura 3 años).

```
FEO ≈ 403 /año
Año 3: venta BU = 800 con resultado extraordinario sobre (mercado 800 − libros 820) ;
       recupero Kt = 80
FF = {−1.100 ; 403 ; 403 ; 1.295}
VAN = 572,37   → se acepta
```

**Concepto que se evalúa:** armado del flujo, escudo fiscal de la amortización, valor residual
y recupero de Kt. Teoría en
[`armado-del-flujo-del-proyecto.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/armado-del-flujo-del-proyecto.md),
[`van.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/van.md).

---

## Ejercicio 2 — Proyecto de reemplazo (con costos incrementales)

Reemplazo de máquina. Inversión BU 48.000 + instalación/flete 2.000 = base 50.000; Kt 3.000
(recupero total); entrenamiento 4.000 (deducible, neto 2.400); venta de la máquina vieja
10.000 (neto 6.000). El proyecto trabaja con **incrementales**: +5.000 de ventas y −8.000 de
costos por año → EBITDA incremental 13.000. VU 5 años, VRT 15.000, VRC 0, IG 40 %, TREMA 10 %.

```
Amort. fiscal = 50.000/5 = 10.000/año
EBIT = 13.000 − 10.000 = 3.000 ;  UN = 1.800 ;  FEO = 11.800/año
Año 5: venta máquina nueva neta = 9.000 ; recupero Kt = 3.000
FF = {−49.400 ; 11.800 ×4 ; 23.800}
VAN = 2.782,34   → se acepta
```

**Concepto que se evalúa:** proyecto de reemplazo con flujos incrementales; capitalizar
instalación y flete en la base amortizable. Teoría en
[`armado-del-flujo-del-proyecto.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/armado-del-flujo-del-proyecto.md).

---

## Ejercicio 3 — Comparar dos planes de pago por su escudo fiscal (ΔVAN)

Dos formas de pagar un compromiso de 100.000 a 4 años, TREMA 15 %, IG 40 %. Cada pago genera
un **escudo fiscal** (40 % del pago) y se compara el VAN de cada plan.

| Año | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Pago A (constante) | 25.000 | 25.000 | 25.000 | 25.000 |
| Escudo A (40 %) | 10.000 | 10.000 | 10.000 | 10.000 |
| Pago B (decreciente) | 40.000 | 30.000 | 20.000 | 10.000 |
| Escudo B (40 %) | 16.000 | 12.000 | 8.000 | 4.000 |
| ΔVAN (B − A) | +5.217 | +1.512 | −1.315 | −3.431 |

```
ΔVAN total = 1.984   → el plan B (pagos altos al principio) tiene mejor VAN del escudo fiscal
```

Adelantar los pagos adelanta el escudo fiscal; por el VTD, eso vale más.

**Concepto que se evalúa:** escudo fiscal de los pagos y su sensibilidad al *timing*. Teoría en
[`armado-del-flujo-del-proyecto.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/armado-del-flujo-del-proyecto.md).

---

## Ejercicio 4 — Proyecto a 10 años con reinversión y prorrateo de costos fijos

Inversión BU 200.000 (VU técnica 5, se reinvierte en el año 5; VRC fiscal a 4 años = 20.000,
VRM 25.000), Kt 80.000 (recupero 0,8), volumen 35.000 u, precio 20, costo variable 8/u, costos
fijos 60.000 (prorrateo 5.000), IG 30 %, TREMA 15 %.

```
EBITDA = 700.000 − 280.000 − 60.000 = 360.000/año
Amort. fiscal = 180.000/4 = 45.000 (en los años con bien amortizable)
Año 5: resultado venta máquina vieja (+5.000) y reinversión −200.000
Año 10: venta BU 25.000, recupero Kt 64.000, pérdida Kt −16.000
FF = {−280.000 ; 265.500 ×... ; 75.500 (año 5) ; ... ; 344.300 (año 10)}
VAN = 977.498   → se acepta
```

**Concepto que se evalúa:** proyecto largo con reinversión intermedia, base amortizable parcial,
recupero parcial de Kt (pérdida) y costos fijos prorrateados. Teoría en
[`armado-del-flujo-del-proyecto.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/armado-del-flujo-del-proyecto.md),
[`vida-economica.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/vida-economica.md).

---

## Ejercicio 5 — Proyecto de ahorro de costos (costo de estudio hundido)

Costo de estudio 5.000 (**hundido, no entra al flujo**), inversión BU 80.000, ahorros anuales
22.000, VU 5, VRM 20.000, VRC 0, IG 34 %, TREMA 10 %.

```
EBITDA = 22.000/año (los ahorros)
Amort. fiscal = 80.000/5 = 16.000
Año 5: venta BU 20.000 (genera IG porque valor de libros = 0)
FF = {−80.000 ; 19.960 ×4 ; 33.160}
VAN = 3.860,27   → se acepta
```

**Concepto que se evalúa:** el costo del estudio es **hundido** y no se incluye; proyecto
justificado por ahorro de costos. Teoría en
[`conceptos-clave.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/conceptos-clave.md),
[`armado-del-flujo-del-proyecto.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/armado-del-flujo-del-proyecto.md).

---

## Ejercicio 6 — VAN con tres enfoques (FEO / FEE) — resuelto solo el directo

Inversión BU 1.000 (VU contable 10), estudio 105 (hundido), ventas 700/año, costos 100/año,
VRM 100, Kt 200 (recupero 0,8), IG 35 %, TREMA 20 %.

```
EBITDA = 600/año ;  Amort. fiscal = 100
Año 5: resultado venta = −400 (mercado 100 < libros 500) ; pérdida Kt = −40
FF = {−1.200 ; 425 ×4 ; 839}
VAN = 237,39   → se acepta
```

> Nota del Excel: solo se hizo el enfoque directo (FF); los enfoques FEO/FEE
> (separando flujo operativo y flujo de la inversión) quedaron sin desarrollar.

**Concepto que se evalúa:** equivalencia entre enfoques (FF total vs. FEO + FEE de BU y Kt).
Teoría en [`flujos-de-fondos.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/flujos-de-fondos.md),
[`armado-del-flujo-del-proyecto.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/armado-del-flujo-del-proyecto.md).

---

## Ejercicio 7 — Proyecto "tapitas" (con preguntas conceptuales)

Inversión BU 200.000 (VU técnica 20, VRC a 10 años = 0, VRM 40.000), Kt 20.000 (recupero 0,5),
ahorro por tapitas 2.500.000/año, costo tapitas 2.000.000/año, sueldo ing. 12.000/año,
capacitación 2.000, IG 20 %, TREMA 10 %, horizonte 5 años.

```
EBITDA ≈ 488.000/año
Amort. fiscal = 200.000/10 = 20.000
Año 5: venta BU 40.000 con resultado −60.000 (libros > mercado) ; recupero Kt 10.000, pérdida −10.000
FF = {−221.600 ; 394.400 ×4 ; 458.400}
VAN = 1.313.225   → se acepta
```

**Respuestas conceptuales:**

- **c)** El costo del estudio **no afecta el VAN** porque es un **costo hundido**: ya fue
  comprometido e incurrido, y existe independientemente de que se haga o no el proyecto, así
  que no cambia el flujo de fondos.
- **d)** Si el escudo impositivo es mayor en los primeros años y menor en los últimos, aunque
  la **suma algebraica** de impuestos sea la misma, por el **valor tiempo del dinero** el valor
  presente del flujo de impuestos es menor → **aumenta el VAN**.

**Concepto que se evalúa:** costo hundido y efecto del *timing* del escudo fiscal sobre el VAN.
Teoría en [`conceptos-clave.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/conceptos-clave.md),
[`van.md`](../../apuntes/economia-empresarial/04-evaluacion-de-proyectos/van.md).
