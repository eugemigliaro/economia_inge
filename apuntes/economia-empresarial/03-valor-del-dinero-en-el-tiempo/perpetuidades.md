# Perpetuidades

Una **perpetuidad** es una [[anualidades|anualidad]] que se repite **hasta el infinito**,
con un crecimiento porcentual anual `g`. Tiene una fórmula simple para su valor presente.

```
VP = F / (r − g)
```

- `F` = primer flujo
- `r` = tasa de descuento
- `g` = crecimiento porcentual anual del flujo

## Ejemplo

Tasa de descuento `r = 10%`, crecimiento `g = 5%`, flujo inicial `F = 100`:

```
VP            +5%
                        110.25
              105
        100                       …
        │      │      │      │
0       1      2      3      ∞
```

```
VP = 100 / (10% − 5%) = 2000
```

## Detalles

- Si `g = 0`, la fórmula queda `VP = F / r`: es una **anualidad hasta el infinito** (flujo
  constante para siempre).
- Igual que en la anualidad, el valor presente se obtiene **un período antes del primer flujo**.
- Requiere `r > g`; si no, la serie no converge.

> Apunte EPI, Parte 3 — El Valor del Dinero en el Tiempo (3.6), doc p. 52.
