# Anualidades

Una **anualidad** es un flujo del **mismo valor que se repite en intervalos iguales** de
tiempo. En vez de descontar flujo por flujo (ver [[valor-actual]]), hay una fórmula directa
para su valor presente.

```
VP = Flujo × Factor(n, r)

Factor = [(1+r)^n − 1] / [(1+r)^n × r] = [1 − (1+r)^(−n)] / r
```

donde `n` = cantidad de flujos y `r` = tasa del período **entre dos flujos**.

## Ejemplo

Tres flujos de 20, descontados al 10%:

```
VP
        20      20      20
        │       │       │
0       1       2       3
```

```
Factor = [(1+10%)^3 − 1] / [(1+10%)^3 × 10%] = 2.48
VP = 20 × 2.48 = 49.74
```

## Detalles que importan

- **Ubicación del VP:** al multiplicar flujo × factor, el valor presente queda **un período
  antes del primer flujo** (en el ejemplo, en el período 0). Si después se lo quiere mover
  hacia el futuro, hay que multiplicarlo por `(1+r)^n`.
- **Control de coherencia:** el factor **nunca puede ser mayor que la cantidad de períodos**
  `n`, porque al traer los flujos al presente el total debe ser menor a su valor nominal sumado.
- **Tasa correcta:** usar la tasa correspondiente al intervalo que hay entre dos flujos
  (si los flujos son mensuales, tasa mensual — ver [[tipos-de-tasas]]).

Si la anualidad se repitiera hasta el infinito, pasaríamos a una [[perpetuidades|perpetuidad]].

> Apunte EPI, Parte 3 — El Valor del Dinero en el Tiempo (3.5), doc p. 51.
