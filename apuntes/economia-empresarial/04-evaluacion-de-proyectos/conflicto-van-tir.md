# Conflicto VAN vs TIR

En proyectos **mutuamente excluyentes** el [[van|VAN]] y la [[tir|TIR]] pueden recomendar
proyectos distintos. **Cuando hay conflicto se prioriza siempre el VAN**, porque su hipótesis de
reinversión es más realista. El conflicto se origina por diferencias de **escala** y de
**timing** entre los proyectos, y geométricamente se delimita con la **tasa de Fisher**.

## Por qué difieren VAN y TIR

| | VAN | TIR |
|---|-----|-----|
| Qué mide | ganancia en **pesos absolutos** | rendimiento en **%** del período |
| Tasa | propia del **inversor** (la elige) | propia de la **inversión** |
| ¿Sesga el resultado? | sí, depende de cada inversor | no, no cambia con el inversor |
| Hipótesis de reinversión | flujos se reinvierten al **costo del capital** | flujos se reinvierten a la **misma TIR** |

La hipótesis del VAN (reinvertir al costo del capital por la vida remanente del proyecto) es
**más realista** que la de la TIR (reinvertir a la propia TIR), de ahí que el VAN prevalezca.

## Causas del conflicto

1. **Diferencia de escala** entre los proyectos.
2. **Diferencia de timing**: los proyectos que recuperan antes el dinero entregan flujos más
   temprano para reinvertir, lo que la TIR sobrevalora.

> La única solución correcta es calcular el VAN.

## Ejemplo numérico (del deck)

Tasa de rendimiento requerida = 10%.

| Año | Proyecto A | Proyecto B |
|-----|------------|------------|
| 0   | $(10.000)  | $(10.000)  |
| 1   | 0          | 6.000      |
| 2   | 13.924     | 7.200      |
| **TIR** | **18%**   | **20%**   |
| **VAN(10%)** | **$1.501** | **$1.401** |

Conflicto: la **TIR recomienda B** (20% > 18%) pero el **VAN recomienda A** ($1.501 > $1.401).

Para desempatar se calcula el **valor futuro** de los ingresos reinvertidos al costo del capital
(10%):

```
VF(A) = 13.924
VF(B) = 6.000·(1+10%) + 7.200 = 13.800
```

A genera mayor riqueza → se elige **A**, coherente con el VAN. La TIR fallaba al asumir que los
$6.000 de B se reinvierten al 20%, cuando en realidad solo rinden el 10%.

## Tasa de Fisher (tasa de cruce o de intersección)

Es la tasa de descuento a la cual **ambos proyectos tienen el mismo VAN** (sus perfiles de VAN
se cruzan). En el ejemplo gráfico del deck, con dos proyectos:

| r   | VAN₁ | VAN₂ |
|-----|------|------|
| 0%  | 50   | 40   |
| 5%  | 33   | 29   |
| 10% | 19   | 20   |
| 15% | 7    | 12   |
| 20% | (4)  | 5    |

```
Tasa de Fisher = 8,7%      TIR₁ = 18,1%      TIR₂ = 23,6%
```

- **A la izquierda** de la tasa de Fisher los rankings se invierten → **hay conflicto** y se
  decide por VAN.
- A la derecha de la tasa de Fisher ambos métodos coinciden.
- En **proyectos independientes** (no excluyentes) no hay conflicto: se acepta todo proyecto con
  `TIR > TREMA` y `VAN > 0`.

## TIR múltiples

Cuando los flujos de caja **cambian de signo más de una vez**, la ecuación `VAN(i) = 0` puede
tener **varias raíces** → varias TIR. El método no resuelve cuál aceptar, así que **se descarta
la TIR** y se usa la [[tirm|TIRM / TER]].

### Ejemplo (del deck)

| Año | Flujo de caja |
|-----|---------------|
| 0   | −1.000        |
| 1   | +1.000        |
| 2   | +1.100        |
| 3   | +1.300        |
| 4   | +1.000        |
| 5   | −3.700        |

Hay dos cambios de signo (+ → −), por eso aparecen **dos TIR**:

```
TIR₁ = 5,070%      (la función IRR de Excel devuelve esta)
TIR₂ = 82,425%     (NPV también da VAN = 0 con esta tasa)
```

Ambas hacen `VAN = 0`, pero ninguna sirve para decidir → se recurre a la
[[tirm|TIRM]] (TER).

> Fuente: deck "EPI virtual (Palandella) — Proyectos · TIR", p. 12–26, y deck de clase
> "epi09_pc", p. 28–39 (material/).
