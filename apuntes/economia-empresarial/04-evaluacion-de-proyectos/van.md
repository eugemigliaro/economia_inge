# Método del Valor Actual Neto (VAN)

El **VAN** es el [[../03-valor-del-dinero-en-el-tiempo/valor-actual|valor actual]] de todos los
flujos de fondos del proyecto, menos las inversiones del comienzo. Mide cuánto valor **crea** el
proyecto, expresado en plata de hoy.

```
VAN(i) = − Inv_0 + Σ FFN_k / (1+i)^k        (k = número de período)
```

equivalentemente:

```
VAN(i) = − Inv_0 + VA(FFN del proyecto)
```

## Criterio de decisión

```
VAN > 0  →  Acepto el proyecto
VAN < 0  →  Rechazo el proyecto
VAN = 0  →  rinde exactamente lo exigido (ni crea ni destruye valor)
```

Aceptar todo proyecto cuyo VA de flujos supere su inversión inicial.

## Tasa de descuento

La tasa `i` es el **costo de oportunidad del dinero**: el rendimiento que se podría ganar en
otro proyecto de **riesgo similar**. En la práctica también se la llama **tasa de corte** o
**TREMA** (Tasa de Rendimiento Mínima Aceptable). Es el [[interes|interés como costo de
oportunidad]] aplicado a la evaluación.

## Ejemplo

`TREMA = 20%`.

| Año           | 0          | 1       | 2       | 3         |
|---------------|------------|---------|---------|-----------|
| Inversión     | −1.000.000 |         |         |           |
| FEO           |            | 450.000 | 600.000 | 700.000   |
| FEE Kt        |            |         |         | 400.000   |
| FEE BU        |            |         |         | 300.000   |
| **FFN**       | −1.000.000 | 450.000 | 600.000 | 1.400.000 |

```
VAN(20%) = −1.000.000 + 450.000/1,2^1 + 600.000/1,2^2 + 1.400.000/1,2^3
         = 601.852   →  VAN > 0, acepto el proyecto
```

La misma serie de flujos se usa para [[tir|TIR]], [[tirm|TIRM]] y [[payback|payback]].

> Apunte EPI, Parte 4 — Evaluación de Proyectos (4.4), doc p. 62–63.
