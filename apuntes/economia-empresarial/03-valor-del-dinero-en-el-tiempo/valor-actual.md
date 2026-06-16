# Cálculo del valor actual (VA)

El **valor actual** de un proyecto es la suma de todos sus flujos futuros **traídos al
período 0** (descontados). Es el mismo concepto que el "valor presente" del [[interes]],
aplicado a una serie de flujos.

```
VA(r) = FF_1/(1+r)^1 + FF_2/(1+r)^2 + … + FF_n/(1+r)^n
```

donde `FF_t` es el flujo de fondos del período `t` y `r` la tasa de descuento.

## La idea: el interés como costo de oportunidad

El interés es lo que dejo de ganar por **no** invertir el dinero a una tasa dada. Atribuyéndole
ese costo, puedo mover cualquier flujo en el tiempo:

```
Año -1     Año 0     Año 1     Año 2
0.91   ◀── 1.00 ──▶ 1.10 ──▶ 1.21
       /(1+10%)  ×(1+10%)  ×(1+10%)
```

- **Descontar** (traer al presente): dividir por `(1+r)^n`.
- **Capitalizar** (llevar al futuro): multiplicar por `(1+r)^n`.

El **factor de descuento** del período `t` es `1/(1+r)^t`.

> Notación: la tasa de descuento se nota `i` para préstamos y `r` para proyectos.

## Ejemplo

Rendimiento exigido por el inversor `r = 10%`:

| Año                   | 1            | 2            | 3            |
|-----------------------|--------------|--------------|--------------|
| Flujo de fondos       | 20           | 30           | 20           |
| Factor de descuento   | /(1+10%)^1   | /(1+10%)^2   | /(1+10%)^3   |
| VA del flujo          | 18.18        | 24.79        | 15.03        |

```
VA total = 18.18 + 24.79 + 15.03 = 58.0
```

```
$ │ 58
  │              30
  │   20                    20
  │
  └───┬─────┬─────┬─────┬──── año
      0     1     2     3
```

Llevar todos los flujos al período 0 permite **evaluar la conveniencia** de un proyecto.
Es la base del [[../04-evaluacion-de-proyectos/van|VAN]].

> Apunte EPI, Parte 3 — El Valor del Dinero en el Tiempo (3.4), doc p. 50–51.
