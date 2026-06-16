# Impacto de la inflación en las tasas

Cuando hay inflación, la tasa efectiva que calculamos (ver [[tipos-de-tasas]]) sigue siendo
**"nominal respecto de la inflación"**. Hay que descontarle la inflación para obtener la
**tasa real**, que es la que mide la ganancia en poder adquisitivo.

## De dónde sale la fórmula

Sin inflación, lo que obtengo al invertir es:

```
Capital × (1 + tasa efectiva) = Monto obtenido
```

Con inflación, el poder adquisitivo de ese monto se deteriora, así que hay que dividir por
`(1 + inflación)`:

```
Capital × (1 + tasa efectiva) / (1 + inflación) = Monto obtenido (en poder adquisitivo)
```

De ahí sale la relación clave (equivalente a la **ecuación de Fisher**):

```
(1 + tasa real) = (1 + tasa combinada) / (1 + inflación)
```

## Tasa combinada vs. tasa real

- **Tasa combinada** (o "nominal respecto de la inflación"): la tasa efectiva que **no**
  ajusta por inflación. Es la que normalmente ofrece el mercado.
- **Tasa real:** lo que realmente gano en poder adquisitivo, ya descontada la inflación.

Si hay inflación, **la tasa real es menor que la combinada**.

> Como las tasas de mercado suelen ser combinadas (no se ajustan por inflación), la tasa real
> recién se conoce **una vez transcurrido el préstamo y medida la inflación del período**.

**Despeje útil:**

```
tasa real = (1 + tasa combinada) / (1 + inflación) − 1
```

> Cuidado de no confundir esta tasa "nominal respecto de la inflación" (que ya es efectiva)
> con la TNA del mercado: son dos sentidos distintos de "nominal". La cadena completa es
> TNA → TEA (ajuste por capitalización) → tasa real (ajuste por inflación).

> Apunte EPI, Parte 3 — El Valor del Dinero en el Tiempo (3.8), doc p. 56.
