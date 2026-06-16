# Determinación de la TREMA / Costo de Capital

La **tasa de descuento** (TREMA o costo de capital) es la rentabilidad mínima que se le exige a
la inversión por renunciar a un uso alternativo de **riesgo similar**; es el
[[van#Tasa de descuento|costo de oportunidad del dinero]] aplicado al [[van|VAN]]. Esta nota
explica **cómo se calcula**: ponderando el costo de la deuda y el de los recursos propios
(WACC), y estimando el costo de los recursos propios con CAPM o el modelo de Gordon.

Visto desde el VTD, es la tasa `i` que hace al inversor indiferente entre $1 hoy y $(1+i) al
final de un período. La correcta elección de la tasa es crítica: define la **aprobación vs.
rechazo** de un proyecto (zona `TIR > TREMA` y `VAN > 0`) y la **selección entre alternativas**
(ver [[conflicto-van-tir|conflicto VAN vs TIR]] y la tasa de Fisher).

## Costo de Capital = promedio ponderado de las fuentes

El costo de capital combina las dos fuentes de fondos del proyecto:

| Fuente             | Costo                              | Cómo se estima              |
|--------------------|------------------------------------|-----------------------------|
| Deuda              | `kd` **después de impuestos**      | tasa del préstamo · (1−tax) |
| Recursos propios   | `re` (más caro, soporta el riesgo) | CAPM o modelo de Gordon     |

## WACC — Costo Promedio Ponderado del Capital

Se pondera el costo de cada fuente por su peso en la estructura de financiamiento:

```
WACC = kd·(1−tax)·(D / (D+E))  +  re·(E / (D+E))
```

- `kd` = costo de la deuda **antes** de impuestos; `kd·(1−tax)` es el costo **después** de IG,
  porque los intereses son deducibles y generan un escudo impositivo.
- `re` = costo de los recursos propios (acciones).
- `D` = monto de deuda, `E` = monto de recursos propios (equity); los pesos suman 1.
- `tax` = alícuota del impuesto a las ganancias.

### Ejemplo del deck

| Fuente    | Monto    | Costo        | Peso | Costo × Peso |
|-----------|----------|--------------|------|--------------|
| Deuda     | $10.000  | 6% (= 2% d.i.)| 1/3  | 2% × 1/3     |
| Acciones  | $20.000  | 9%           | 2/3  | 6%           |
| **WACC**  | $30.000  |              |      | **8%**       |

El 6% de la deuda es antes de impuestos; después de IG queda ≈ 2% sobre el total ponderado. El
costo de las acciones (9%) es mayor porque el accionista exige más por asumir el riesgo.

## CAPM — Capital Asset Pricing Model

Estima el costo de los **recursos propios** a partir del riesgo sistemático:

```
re = rF + (rM − rF)·β + riesgo país
```

- `rF` = tasa libre de riesgo (risk free).
- `rM` = rendimiento esperado del mercado; `(rM − rF)` es la **prima de riesgo de mercado**.
- `β` (beta) = sensibilidad del activo respecto del mercado (cuánto amplifica o amortigua sus
  movimientos).
- `riesgo país` = sobretasa que se suma al evaluar en economías emergentes (Argentina).

## Modelo de Gordon

Estima el costo de los recursos propios a partir de los dividendos y su crecimiento:

```
re = (D / P) + g
```

- `D` = dividendo esperado por acción.
- `P` = precio de la acción.
- `g` = tasa de crecimiento esperada de los dividendos.

> Fuente: deck "EPI virtual (Palandella) — Proyectos · TREMA", p. 5–7, y deck de clase
> "epi09_pc" (material/).
