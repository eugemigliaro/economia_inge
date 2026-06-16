# Método de la Tasa Interna de Retorno (TIR)

La **TIR** es la tasa de descuento para la cual el [[van|VAN]] del proyecto se hace **cero**. Es,
en otras palabras, la **tasa de rendimiento** del flujo de fondos del proyecto.

```
VAN(TIR) = − Inv_0 + Σ FFN_k / (1+TIR)^k = 0        (k = número de período)
```

## Criterio de decisión

Se compara contra la TREMA (la tasa mínima exigida, ver [[van]]):

```
TIR > TREMA  →  Acepto el proyecto
TIR < TREMA  →  Rechazo el proyecto
```

## Ejemplo

Con el mismo flujo del ejemplo del [[van|VAN]] (que daba VAN = 601.852 al 20%), se busca la tasa
que anula el VAN:

| Año     | 0          | 1       | 2       | 3         |
|---------|------------|---------|---------|-----------|
| **FFN** | −1.000.000 | 450.000 | 600.000 | 1.400.000 |

```
VAN(TIR) = 0   →   TIR = 48,7%

TIR (48,7%) > TREMA (20%)  →  acepto el proyecto
```

## Limitación

La TIR asume **implícitamente** que los flujos intermedios se **reinvierten a la propia TIR**
—una tasa matemática, no de mercado—. Con TIRes altas (48% en el ejemplo) esa hipótesis es
irreal: difícilmente se reinvierta al 48%. Esa corrección la resuelve la [[tirm|TIRM]].

> Apunte EPI, Parte 4 — Evaluación de Proyectos (4.5), doc p. 63–64.
