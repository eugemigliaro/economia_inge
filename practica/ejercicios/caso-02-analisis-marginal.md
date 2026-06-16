# Caso 02 — Casos de aplicación del análisis marginal

> **Enunciado (Apunte EPI, Parte 2 — Costos, 2.5.4, doc p. 35–39):** cuatro aplicaciones del
> análisis marginal combinadas con el análisis del punto de equilibrio.

## Gráfico de equilibrio con costos fijos separados

Se separan los costos fijos en dos grupos: los **propios** del producto `Fi` y los de
**estructura** prorrateados `Fei`. Aparecen así dos puntos:

- **Punto de equilibrio:** los ingresos del producto `i` igualan a *todos* sus costos
  (variables + fijos propios + fijos asignados).
- **Punto de pseudoequilibrio:** los ingresos igualan solo a los variables + fijos propios.

```
$ │                         IT
  │                       /
  │   equilibrio ──→    *──── CT total (cv + Fi + Fei)
  │                   / /
  │ pseudoeq. ──→   *  /──── cv + Fi
  │               / /
  │   A   │  B  │   C
  └────────────────────────── q
```

- **Zona A** (debajo del pseudoequilibrio): los ingresos no cubren ni los variables ni los
  fijos propios → medida urgente (subir volumen o eliminar el producto).
- **Zona B** (entre pseudoequilibrio y equilibrio): no cubre *todo*, pero sí los variables y
  los fijos propios y **aporta algo** a los gastos generales. **Discontinuarlo sería un error
  grave** (esos gastos generales no desaparecen con el producto). No todos los productos
  pueden estar en B, o no se cubrirían los fijos.
- **Zona C** (sobre el equilibrio): conviene mantenerlo sin dudas.

## Caso 1 — Costeo marginal (¿vender por debajo del costo unitario?)

| Producto ×10 u | $/u | wi | fei |
|---|---|---|---|
| MP | 38 | 38 | |
| MOD | 10 | 10 | |
| GGF | 15 | 3 | 12 |
| **Costo industrial** | 63 | | |
| GGACyF | 27 | 8 | 19 |
| **Costo comercial** | ci = 90 | wi = 59 | 31 |
| Precio de venta | pi = 80 | | |

Acá `pi (80) < ci (90)` → el costeo tradicional diría "no vender una unidad más". **Error.**
Como `pi (80) > wi (59)`, la unidad adicional aporta utilidad marginal (80 − 59 = 21 $/u).

> **Regla:** se puede vender por debajo del costo unitario `ci` siempre que `pi > wi` (costo
> marginal unitario). No todos los productos pueden venderse a su `wi`, porque los costos
> fijos totales igual deben cubrirse.

*(GGACyF = gastos generales de administración, comercialización y finanzas.)*

## Caso 2 — Introducción de un nuevo producto

Conviene incorporar el producto `i` si **aumenta** las utilidades de la compañía:

```
(pi − wi) · Qi − Fi > 0      (estar en zona B o C)
```

No se consideran los fijos de estructura prorrateados `Fei`: castigarían al producto con
gastos que no genera su incorporación y que tampoco se evitan en las otras líneas.

## Caso 3 — Eliminación de un producto

Conviene eliminar el producto si la **utilidad marginal que aporta es menor** que los gastos
fijos propios que se ahorran al eliminarlo:

```
(pi − wi) · Qi < Fi    →    discontinuar    (zona A)
```

## Caso 4 — Calidad de ventas

Partiendo de `Ui = mi · Vi − (Fi + Fei)`: la utilidad depende de la cantidad vendida, de la
tasa marginal `mi` y de los costos fijos. El coeficiente `mi` define la **calidad de ventas**
(cuánta utilidad aporta cada peso vendido).

Con `ma = 46 %` y `mb = 50 %`, cada peso vendido de `b` aporta más utilidad que el de `a`. Si
la empresa desplaza ventas de productos de **menor margen** a productos de **mayor margen**,
puede **aumentar la utilidad sin vender más unidades**.

## Concepto que se evalúa

Análisis marginal: utilidad marginal unitaria `ei = pi − wi`, tasa de utilidad marginal
`mi = ei/pi`, y su combinación con el punto de equilibrio.
Teoría en [`apuntes/.../02-costos/analisis-marginal.md`](../../apuntes/economia-empresarial/02-costos/analisis-marginal.md)
y [`punto-de-equilibrio.md`](../../apuntes/economia-empresarial/02-costos/punto-de-equilibrio.md).
