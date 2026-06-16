# El cash flow

El cash flow (flujo de caja) muestra el **dinero real** (cash) que entró y salió de la empresa
durante un período. No todo lo que figura en el estado de resultados es cash: hay que ajustar
las partidas que no mueven efectivo.

## Por qué el resultado ≠ caja

- Las **amortizaciones** son un costo en el estado de resultados (bajan la utilidad y el
  impuesto), pero **no son dinero que salió** en el período: el desembolso ocurrió al comprar
  la planta/equipo; el cargo por depreciación se reconoce año a año durante la vida útil
  contable (no necesariamente igual a la vida útil técnica real).
- Los **cambios en cuentas por cobrar, inventario y cuentas por pagar** representan
  diferencias de caja respecto del resultado contable.

## De la ecuación patrimonial al cash flow

Partiendo de `ACTIVO = PASIVO + PN`, se trabaja con las **variaciones** (Δ) hasta despejar la
variación de caja (ΔC):

```
A = P + PN            →   ΔA = ΔP + ΔPN
                          ΔC = ΔP + ΔPN − ΔA(≠C)

ΔC = ΔDcom + ΔDfin + Utilidades + Aportes − Dividendos
       − (ΔCréditos + ΔBienes de Cambio + ΔBU)

con   ΔBU = Inversiones − Amortizaciones

ΔC = [ Utilidades + Amortizaciones − ΔCréditos − ΔBienes de Cambio + ΔDcom ]   ← Flujos de la Operación
   + [ − Inversiones ]                                                          ← Flujos de Inversión
   + [ ΔDfin + Aportes − Dividendos ]                                           ← Flujos de Financiación
```

Donde `ΔDcom` = variación de deudas comerciales y `ΔDfin` = variación de deudas financieras.

**Variación del Activo** = Capital de Trabajo + Bienes de Uso

- **Capital de Trabajo** (distinto de caja):
  - aumenta cuando aumentan las cuentas por cobrar (Variación de Créditos),
  - aumenta cuando aumentan los stocks (Bienes de Cambio),
  - disminuye cuando aumentan las cuentas a pagar a proveedores (Deudas Comerciales).
- **Bienes de Uso**: aumentan con las inversiones, disminuyen con las amortizaciones
  (desgaste "contable" de las máquinas).

**Pasivos**: aumentan al tomar más préstamos, disminuyen con cada porción de **capital** que
se le paga al acreedor. Ojo: los **intereses NO van acá** — son un gasto del cuadro de resultados.

**Patrimonio Neto**: aumenta con aportes y utilidades positivas; disminuye con dividendos y
utilidades negativas.

## Cómo se arma la variación de caja (estructura del apunte)

El apunte ordena los flujos en tres bloques. `α` es la tasa de impuesto a las ganancias.

```
OPERACIÓN
  + Utilidad antes de impuestos e intereses (EBIT)
  − EBIT × α                       (impuesto a las ganancias sobre el EBIT)
  + Amortizaciones                 (se suman: se restaron para el EBIT pero no son cash)
  − ΔCréditos          ┐
  − ΔBienes de Cambio  ├─ − Variación del Capital de Trabajo (excluida la caja)
  + ΔDcom              ┘
  = Flujo de la Operación

INVERSIONES
  − Inversiones
  + Venta de Bienes de Uso         (mercado de usados)
  = Flujo de Inversiones

FINANCIAMIENTO
  + ΔDfin                          (toma neta de deuda financiera)
  − Intereses
  + Intereses × α                  (escudo fiscal: el interés es gasto y reduce el impuesto)
  + Aportes − Dividendos           (flujo del accionista)
  = Flujo de Financiamiento

ΔC = Flujo de fondos total = FF Operación + FF Inversiones + FF Financiamiento
```

### Dos "free cash flows"

- **FCFF — Free Cash Flow to the Firm** ("del Activo"): agrupa **Operación + Inversiones**.
  Es el flujo que genera el negocio independientemente de cómo se financie.
- **FCFE — Free Cash Flow to Equity** ("hacia el accionista"): es la línea
  `Aportes − Dividendos` dentro del financiamiento, el flujo que efectivamente queda para el socio.

### Claves

- Las **amortizaciones se suman** porque se restaron para llegar al EBIT y no son flujo de efectivo.
- La caja varía cuando se **invierte** y cuando se **venden** bienes de uso (mercado de usados).
- El financiamiento aporta el **escudo fiscal de los intereses** (`+ Intereses × α`): erogar
  más gasto (interés) reduce el impuesto a las ganancias.

> Apunte EPI, Parte 1 — Contabilidad (1.5), doc p. 6–7.
