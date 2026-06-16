# Optimización del diseño minimizando costos

Al diseñar productos, procesos y servicios, el ingeniero busca el **mínimo costo de ciclo de
vida**. Como el potencial de ahorro está en las primeras etapas del proyecto (después es muy
difícil bajar el costo), la minimización de costos debe considerarse en **todas las etapas**.

## Procedimiento

1. **Identificar la variable de diseño** que guía el costo (la que explica la mayor parte del
   comportamiento del costo total).
2. **Escribir el costo en función de esa variable.** Forma simplificada:

```
Costo = a·X + b/X + k
```

- `X` = variable de diseño.
- `a` = parámetro del costo que varía en forma **directa** con X.
- `b` = parámetro del costo que varía en forma **indirecta** (inversa) con X.
- `k` = costos fijos.

3. Si **X es continua:** derivar el costo respecto de X e igualar a cero (`dC/dX = 0`).
4. Si **X es discreta:** evaluar el costo para cada valor posible de X; el menor da el óptimo.
   (Aquí termina el procedimiento para variables discretas.)
5. Si X es continua: resolver la ecuación del paso 3 despejando X.
6. Verificar con la **segunda derivada** que el punto hallado sea un mínimo (no un máximo).

## Ejemplo (cable a través del pantano)

Conectar un generador con una fábrica cruzando un pantano. El cable bajo el pantano cuesta
6 mil $/m; por tierra firme, 3 mil $/m. Con `a = 200 m` y la distancia total por tierra
`e + d = 400 m`, si `Y` es el tramo en diagonal sobre el pantano:

```
Costo = (200² + Y²)^(1/2) · 6 + (400 − Y) · 3
dC/dY = 6Y / (200² + Y²)^(1/2) − 3 = 0   →   Y = 115,5 m
Costo mínimo ≈ 2.240 mil $
```

Lo intuitivo (`Y = 0`, todo por tierra) cuesta **más**: minimiza el tramo caro pero alarga
el recorrido total. El óptimo equilibra ambos costos.

> Ver [costo-del-ciclo-de-vida.md](./costo-del-ciclo-de-vida.md) para el marco general.

> Apunte EPI, Parte 2 — Costos (2.9), doc p. 42–45.
