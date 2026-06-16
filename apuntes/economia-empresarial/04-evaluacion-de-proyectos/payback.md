# Método del Payback (período de repago)

El **payback** mide **cuánto tarda** el proyecto en devolver al inversor el importe de la
inversión. Suele usarse como método **complementario** del [[van|VAN]] / [[tir|TIR]]: un
proyecto puede tener buen VAN pero acumular casi todos sus ingresos al final, cuando las
condiciones de mercado pueden haber cambiado.

Hay dos modalidades: **simple** y **compuesto (descontado)**.

## Payback simple

Se van **acumulando los flujos** (sin descontar) y se busca el período en que el acumulado pasa
a ser positivo.

| Año          | 0          | 1        | 2        | 3         |
|--------------|------------|----------|----------|-----------|
| FFN          | −1.000.000 | 450.000  | 600.000  | 1.400.000 |
| **FFN Acum** | −1.000.000 | −550.000 | **50.000** | 1.450.000 |

El acumulado se vuelve positivo **durante el año 2**. Para más exactitud, interpolando
linealmente dentro del año, se estima en qué mes se recupera la inversión.

## Payback compuesto (descontado)

Igual que el simple, pero acumulando el **valor actual** de cada flujo (incorpora el
[[../03-valor-del-dinero-en-el-tiempo/valor-actual|valor tiempo del dinero]]). Es más exigente
que el simple.

| Año             | 0          | 1        | 2         | 3         |
|-----------------|------------|----------|-----------|-----------|
| FFN             | −1.000.000 | 450.000  | 600.000   | 1.400.000 |
| VA(FFN, 20%)    | −1.000.000 | 375.000  | 416.667   | 810.185   |
| **VA Acum**     | −1.000.000 | −625.000 | −208.333  | **601.852** |

Acá el acumulado descontado recién se vuelve positivo en el **año 3** (más tarde que el simple,
porque cada flujo "vale menos" traído a hoy).

> Apunte EPI, Parte 4 — Evaluación de Proyectos (4.7), doc p. 66–68.
