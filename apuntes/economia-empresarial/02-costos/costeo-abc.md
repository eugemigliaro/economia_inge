# Costeo basado en actividades (ABC)

El ABC (*Activity Based Costing*) asigna los costos indirectos en función de las
**actividades** que la empresa realiza para producir, en lugar de prorratearlos según una
base de volumen (horas-hombre, horas-máquina, unidades). Idea central: las actividades
consumen recursos, y los productos consumen actividades.

## Por qué surge

Los sistemas tradicionales (ej. costeo por absorción) se diseñaron para valorar inventarios,
no para la gestión interna. Reparten los costos indirectos según bases de volumen, que **no
reflejan con precisión** los recursos que consume cada producto. Esto "castiga" con más costo
a los productos simples de alto volumen y subcostea a los productos especiales de bajo
volumen y alta complejidad.

## Características

- Es un modelo **gerencial**, no contable.
- Los recursos son consumidos por las actividades, y estas por los objetos de costo
  (productos, servicios, clientes, regiones, procesos).
- Considera todos los costos y gastos como recursos.
- Ve la empresa como un conjunto de **actividades/procesos**, no como una jerarquía
  departamental.

## Pasos del método

1. Identificar las **actividades** que consumen recursos.
2. Asignar los costos a cada actividad.
3. Identificar los **cost drivers** (generadores de costo) de cada actividad.
4. Calcular la **tasa** de costo indirecto de cada actividad:

```
Tasa = Costo indirecto estimado de la actividad / Nº estimado de unidades de actividad
```

5. Asignar el costo a cada producto:

```
Costo del producto i = Tasa × Actividad actual consumida por i
```

## Comparación: tradicional vs ABC

La diferencia está en cómo cada uno resuelve el mayor problema del análisis de costos: la
**adjudicación de los costos indirectos de fabricación**.

- **Tradicional (absorción):** los reparte según una base de volumen/actividad
  (horas-hombre, horas-máquina, $-material).
- **ABC (contemporáneo):** los reparte según las **actividades relevantes** de la empresa.

### Ejemplo (Citrus S.A.)

Citrus produce un modelo *Lujo* y uno *Regular*. Costo indirecto total = $2.000.000.

| | Lujo | Regular |
|---|---|---|
| Material directo (MPD) | $150 | $112 |
| Mano de obra directa (MOD) | $16 | $8 |
| Tiempo de trabajo directo | 1,6 h | 0,8 h |
| Volumen esperado | 5.000 u | 40.000 u |

**Costeo tradicional** — base: horas de trabajo directo (HTD).
Total HTD = 5.000·1,6 + 40.000·0,8 = 8.000 + 32.000 = 40.000 h.
Tasa = $2.000.000 / 40.000 = **$50 por HTD**.

| | Lujo | Regular |
|---|---|---|
| MPD | 150 | 112 |
| MOD | 16 | 8 |
| CI ($50 × h) | 80 | 40 |
| **Costo unitario** | **$246** | **$160** |

**Costeo ABC** — se reparte el CI por actividad y su driver:

| Actividad | Driver | CI actividad | Unid. actividad | Tasa |
|---|---|---|---|---|
| Abastecimiento | Órdenes | $84.000 | 1.200 | $70/orden |
| Reprocesamiento | Órdenes | $216.000 | 900 | $240/orden |
| Testeo | Tests | $450.000 | 15.000 | $30/test |
| Máquinas | Horas | $1.250.000 | 50.000 | $25/hora |

CI asignado = unidades actuales de actividad × tasa → Lujo $720.000, Regular $1.280.000
(suman $2.000.000, el CI original). Por unidad: Lujo $720.000/5.000 = **$144**;
Regular $1.280.000/40.000 = **$32**.

| | Tradicional Lujo | ABC Lujo | Tradicional Regular | ABC Regular |
|---|---|---|---|---|
| MPD | 150 | 150 | 112 | 112 |
| MOD | 16 | 16 | 8 | 8 |
| CI | 80 | **144** | 40 | **32** |
| **Total** | $246 | **$310** | $160 | **$152** |

**Conclusión:** el ABC revela que el producto especializado de bajo volumen (Lujo) tiene
**más** costo indirecto que el estimado por el método tradicional, que lo subcosteaba.

> Apunte EPI, Parte 2 — Costos (2.3.4 y 2.3.5), doc p. 24–29.
