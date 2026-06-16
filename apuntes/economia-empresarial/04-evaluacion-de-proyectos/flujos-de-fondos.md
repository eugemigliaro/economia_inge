# Cálculo de flujos de fondos

El **flujo de fondos** de un proyecto registra el efectivo que entra y sale de la caja en cada
período. No es lo mismo que el resultado contable: solo cuentan los conceptos que son **cash**
(las amortizaciones, puramente contables, no lo son). El **Flujo de Fondos Neto (FFN)** de un
período es la suma de sus flujos operativos y extraordinarios.

```
FFN_k = FEO_k + FEE_k
```

## Inversiones

- **Bienes de Uso:** valor de adquisición + costos de instalación y flete (si los hubiera).
- **Capital de Trabajo (Kt):** desembolsos en Activos Corrientes (créditos por venta y bienes
  de cambio, principalmente) que **no** nos financian terceros (p. ej. proveedores).

## Flujos de Fondos Operativos (FEO)

Parten del [[../01-contabilidad/cuadro-de-resultados|cuadro de resultados]] pero quedándose
solo con lo que es efectivo. El cuadro de resultados operativo tiene esta forma:

```
   Ventas
 − Costo de Venta (CV)
 − Gastos Fijos (GF)
 − Amortización (A)      ← contable, NO es cash
 = UAIG  (utilidad antes de impuesto a las ganancias)
 − IG    (impuesto a las ganancias)
 = U neta
```

Hay **tres enfoques** para calcular el FEO; los tres dan el mismo resultado.

### Enfoque ascendente

Se parte de la Utilidad Neta y se le **suma** todo concepto no efectivo incluido en ella. Aguas
arriba de la U neta el único no-cash es la amortización:

```
FEO = U neta + A
```

### Enfoque descendente

Se baja desde las Ventas contemplando solo los conceptos que son efectivo:

```
FEO = V − CV − GF − IG
```

### Enfoque fiscal

Toma el cash que queda después del IG y le suma el **escudo impositivo** que generan las
amortizaciones (la A reduce la base imponible, ahorrando `tasa_IG × A` de impuesto):

```
FEO = (V − CV − GF) × (1 − tasa_IG) + tasa_IG × A
```

## Flujos de Fondos Extraordinarios (FEE)

Surgen de las **ventas extraordinarias** de Bienes de Uso y del **recupero del Capital de
Trabajo** al final del proyecto. Su cuadro de resultados es:

```
   VM   (valor de mercado / reventa)
 − VL   (valor de libros)
 = UAIG
 − IG
 = U neta
```

- **Valor de Libros (VL):** para un BU, Valor Original − Amortizaciones Acumuladas. Para el Kt,
  es directamente el valor de la inversión (el Kt no se amortiza).
- **Valor de Mercado (VM):** valor de reventa. Para el Kt suele darse con un **coeficiente de
  recuperación** `m`: `VM = m × VL` (qué porcentaje de la inversión se recupera al final).

Los tres enfoques, análogos a los del FEO:

```
Ascendente:   FEE = U neta + VL
Descendente:  FEE = VM − IG
Fiscal:       FEE = VM × (1 − tasa_IG) + tasa_IG × VL
```

## Esquema resumen

Las flechas que se alejan de la línea de tiempo son **egresos** (inversiones); las que apuntan
hacia ella son **ingresos** (FEO, FEE).

```
 Inv BU + Kt
   │
   ▼
───┬─────┬─────┬─────┬─────┬──── tiempo
   0     1     2     3     ...   n
         ▲     ▲     ▲           FEO_1 … FEO_n
                                 ▲ FEE Kt (recupero)
                                 ▲ FEE BU (reventa)
```

> Apunte EPI, Parte 4 — Evaluación de Proyectos (4.2), doc p. 58–61.
