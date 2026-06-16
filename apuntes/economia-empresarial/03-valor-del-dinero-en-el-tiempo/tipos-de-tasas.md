# Tipos de tasas: nominal, efectiva y equivalentes

La **tasa nominal** es la que se publica; la **tasa efectiva** es la que realmente se paga
o cobra una vez contada la capitalización. Solo la efectiva sirve para comparar y calcular.

## Tasa nominal anual (TNA) y capitalización

Por motivos comerciales, el mercado suele convertir el interés en capital **más de una vez
por período**. Una TNA puede tener distintas capitalizaciones:

- **Mensual:** los intereses se capitalizan 12 veces al año.
- **Trimestral:** se capitalizan 4 veces al año.

Al cabo de un año:

```
VF = VP × (1 + TNA/m)^m
```

donde `m` = cantidad de veces que se capitaliza el interés en el año.

## Tasa efectiva anual (TEA)

Es la tasa que realmente se paga/recibe en el año, ya con el efecto de la capitalización
incorporado.

**Ejemplo — TNA 12% con capitalización mensual:**

```
VF = 1000 × (1 + 12%/12)^12 = 1000 × (1.01)^12 = 1126.8
```

Se pagaron $126.8 de interés en el año → **TEA = 12.68%** (no 12%). La capitalización
mensual hace que la efectiva supere a la nominal.

## Pasar entre tasas efectivas de distinto período

Las tasas efectivas se relacionan elevándolas a la cantidad de veces que entran en el año.
La regla: **el exponente es la cantidad de períodos de esa tasa que hay en el año común**.

**Ejemplo — TNA 16% con capitalización trimestral:**

`16%/4 = 4%` es la Tasa Efectiva Trimestral. Para llevarla a un año:

```
(1 + 16%/4)^4 = (1 + TEA)^1 = (1 + TEM)^12
(1.04)^4 = 1.170
```

Despejando:

```
TEA = 17.0%
TEM = (1.17)^(1/12) − 1 = 1.3%
```

> Para que estas igualdades valgan, todas las tasas efectivas deben estar **referidas al
> mismo período de tiempo** (acá, un año).

## Tasas equivalentes

Distintas tasas nominales con distintas capitalizaciones que producen **la misma TEA** se
llaman **equivalentes**: tienen el mismo efecto financiero.

Por ejemplo, una **TNA 15.8% con capitalización mensual** también llega a una **TEA 17.0%**,
igual que la TNA 16% trimestral del ejemplo anterior. Son equivalentes.

> Apunte EPI, Parte 3 — El Valor del Dinero en el Tiempo (3.3), doc p. 48–49.
