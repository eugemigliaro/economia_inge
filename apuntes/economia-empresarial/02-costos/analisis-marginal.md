# Análisis marginal

Estudia el aporte de cada **producto / servicio / cliente** a las utilidades de la empresa.
Su gran ventaja: razona con costos variables y márgenes, **sin necesidad de prorratear los
costos fijos** (que es la principal fuente de error del costeo tradicional).

Permite responder preguntas como:

- ¿A partir de qué volumen mínimo conviene lanzar un nuevo producto?
- ¿Conviene dejar de producir un producto existente?
- ¿Conviene seguir atendiendo a un cliente, o cerrar una sucursal/fábrica?
- ¿Cuál es el precio mínimo de una unidad adicional?
- ¿Conviene usar capacidad ociosa para vender a precio menor (*dumping*)?
- ¿Conviene tercerizar una producción?

## Utilidad unitaria (enfoque tradicional, con prorrateo)

Conociendo ventas, costos y cantidad de un producto `i`:

```
Utilidad:           Ui = Vi − Ci
Utilidad unitaria:  ui = (Vi − Ci) / Qi
Ventas:             Vi = pi · Qi          (precio constante)
```

El costo del producto tiene tres partes:

```
Ci = wi · Qi + Fi + Fei
```

- `wi` = costo variable unitario de producción.
- `Fi` = costos fijos **propios** del producto.
- `Fei` = costos fijos **de estructura prorrateados** al producto.

Reemplazando:

```
Ui = pi · Qi − (wi · Qi + Fi + Fei)
ui = (pi − wi) − (Fi + Fei) / Qi
```

**Ejemplo:** Q = 3.000 u, p = 20 $/u, w = 10 $/u, Fi = 5.000 $, Fei = 5.000 $.

```
Ui = 3.000 · (20 − 10) − 5.000 − 5.000 = 20.000 $
ui = (20 − 10) − (5.000 + 5.000)/3.000 = 6,67 $/u
```

> **Limitación:** este enfoque sirve poco para analizar. Si se vendiera **una unidad más**,
> NO se ganarían 6,67 $ extra, porque los costos fijos no cambian: solo aumenta el costo
> variable. Para eso sirve la utilidad marginal.

## Utilidad marginal unitaria

Indica cuánto aumenta la utilidad total al vender **una unidad más**. Es la derivada de la
utilidad respecto de la cantidad:

```
ei = ∂U / ∂Q = pi − wi          (utilidad marginal unitaria)
Ei = ei · Qi                    (utilidad marginal del producto)
```

En el ejemplo: `ei = 20 − 10 = 10 $/u`. Vender una unidad más aumenta la utilidad en
**10 $**, no en 6,67 $. Válido dentro del rango donde los costos fijos son constantes.

## Tasa de utilidad marginal

Cociente entre la utilidad marginal unitaria y el precio unitario:

```
mi = ei / pi
```

Reemplazando `ei = mi · pi` en la utilidad: `Ui = mi · Vi − (Fi + Fei)`. Derivando respecto
de las ventas, `mi` es esa derivada:

```
mi = ∂U / ∂V
```

Indica **cuánto aumenta la utilidad por cada peso adicional vendido** (a precio constante,
por variación de volumen). En el ejemplo: `mi = 10/20 = 50 %` → cada 100 $ extra de venta
generan 50 $ más de utilidad. `mi` define la **calidad de ventas** del producto.

## Casos de aplicación

Los ejemplos numéricos de aplicación (costeo marginal, introducción y eliminación de
productos, calidad de ventas) están resueltos en
[`practica/ejercicios/caso-02-analisis-marginal.md`](../../../../practica/ejercicios/caso-02-analisis-marginal.md).

> Apunte EPI, Parte 2 — Costos (2.5 a 2.5.4), doc p. 32–39.
