# Armado del flujo del proyecto

El **flujo de caja libre del proyecto (FCLP)** se construye con criterio **incremental**:
solo entran los ingresos y egresos que existen **por el proyecto**, comparando "con proyecto"
contra una base **"sin proyecto" optimizada**. Esta nota complementa [[flujos-de-fondos]] con
cuatro detalles del armado: el criterio incremental, el capital de trabajo por stock de caja,
el valor terminal y el tratamiento de impuestos.

El procedimiento de construcción es: **Identificar → Medir → Valorar → Ordenar** los impactos
relevantes del proyecto sobre la empresa, definiendo magnitud, signo, valor monetario y momento
de cada uno (los flujos ocurren al **final** de cada período; las inversiones iniciales en t=0).

## Criterio incremental con base optimizada

- Se identifican beneficios y costos **asociados únicamente con el proyecto**.
- No se incluye lo que existiría se haga o no el proyecto (ni los [[conceptos-clave|costos
  hundidos]]).
- La base de comparación es una situación **"sin proyecto" optimizada**, NO el "antes del
  proyecto". El "antes" no es la base apropiada: la empresa optimizaría su operación aunque no
  hiciera el proyecto, y eso es lo que hay que comparar.

```
Flujo incremental = (situación CON proyecto) − (situación SIN proyecto, optimizada)
```

## Capital de trabajo por stock de caja

El efectivo necesario para operar es un **uso de caja**. Se computan las **variaciones año a
año** (`Variación = Final − Inicial`):

- Un **incremento** del stock de caja → **egreso** de caja.
- Una **reducción** del stock de caja → **ingreso** de caja.

Si la política es, p. ej., mantener un stock de caja igual al **20% de las ventas**:

| Año                      | 1    | 2    | 3    | 4     | 5     |
|--------------------------|------|------|------|-------|-------|
| Ventas                   | 2000 | 2500 | 3200 | 5000  | 0     |
| Stock de caja (20%)      | 400  | 500  | 640  | 1000  | 0     |
| **Efecto sobre el F.C.** | −400 | −100 | −140 | −360  | +1000 |

Al cerrar el proyecto el capital de trabajo se **recupera** (el +1000 del año 5). Ojo: puede no
recuperarse íntegramente (inventarios obsoletos, créditos incobrables) → esa diferencia es una
**pérdida**.

## Valor terminal

Al término del **horizonte de planificación** se hace un corte artificial con fines de
evaluación. Hay tres formas de modelizar el valor terminal:

| Criterio | Qué se computa |
|----------|----------------|
| Liquidación a **valor libro** | se venden los activos a su valor contable (sin impacto en IG) |
| Liquidación a **valor comercial** | se venden a precio de mercado, con **impacto en IG** por la ganancia/pérdida de capital |
| **Valor presente de una perpetuidad** | la planta sigue operando: se descuenta el flujo perpetuo a t=n |

Suponer que se venden todos los activos genera un **flujo de efectivo extra en el último año**.
Como en la mayoría de los casos la planta seguirá operando, suele modelizarse un flujo perpetuo
más allá del horizonte, cuyo valor presente (ubicado en t=n) es el valor terminal.

## Tratamiento de impuestos (IG)

El impuesto a las ganancias grava el **resultado contable neto** del proyecto:

- Se calcula sobre ejercicios fiscales; tasa **35%** anual.
- **Quebrantos acumulables**: las pérdidas contables se reconocen como gasto y pueden
  **acumularse hasta 5 años** contra ganancias futuras.
- **Ganancia / pérdida de capital** en la liquidación de activos:

```
Valor de reventa > Valor libro  →  GANANCIA de capital (ingreso, gravado)
Valor de reventa < Valor libro  →  PÉRDIDA de capital  (egreso, deducible)
Ganancia/Pérdida = Valor de reventa − Valor libro
```

> La **amortización** no es un flujo de caja, pero reduce la base imponible y genera el
> [[conceptos-clave|escudo impositivo]] `Escudo = A · tax`. Ver [[flujos-de-fondos]].

Otros impuestos (Internos, Ingresos Brutos, Sellos) se toman como **un costo más** del proyecto.

## Qué NO entra en el FCLP

No se incluyen: depreciaciones y reservas (salvo por su escudo), ingresos/pagos de préstamos,
intereses, aportes de capital, dividendos, ni el ahorro de IG por intereses (eso ya está en la
[[trema|TREMA / WACC]] usada para descontar).

> Fuente: deck "EPI virtual (Palandella) — Proyectos · cash flow", y deck de clase "epi09_pc",
> p. 58–78 (material/).
