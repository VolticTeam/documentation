# Guía para agentes y colaboradores

## Antes de editar

1. Lee `README.md`, `docs.json` y las páginas relacionadas con el cambio.
2. Comprueba si la página tiene equivalente en el otro idioma.
3. Conserva las URLs existentes y revisa los enlaces que apunten a la página.

## Organización

- Las ofertas de `docs.json` combinan verticales y producto: `Hotel Room
  Control` y `Cooling Patrol` son soluciones; `Voltic FrostLine` es un producto
  independiente que también forma parte de Room Control.
- Dentro de cada producto, ordena las páginas por intención: empezar, instalar,
  operar, referencia y soporte.
- No mezcles una página de producto con otra solo para completar un grupo:
  enlázala desde el contenido o crea la página específica cuando exista.

## Contenido técnico

- Mantén la terminología: **Voltic Freeline** = room control; **Voltic
  FrostLine** = termostato.
- FrostLine se vende también de forma independiente para viviendas y puede
  vincularse con VolticHub o con hubs Zigbee compatibles con Tuya. La guía debe
  contemplar fan coils de 2 y 4 tubos y fan coil con suelo radiante hidráulico,
  pero nunca inventar el mapa de bornes: depende de versión, firmware y
  esquema validado.
- La topología oficial del Room Control es un Hub por planta: aprox. 150
  dispositivos como referencia, 10–15 habitaciones recomendadas por Hub y
  habitaciones en la misma planta; usa repetidores y añade otro Hub solo si el
  estudio de cobertura lo requiere.
- El Hub usa por defecto Zigbee en el canal 25. Recomienda evitar el canal 11
  de Wi-Fi del hotel para reducir colisiones e interferencias.
- Las instrucciones de 230 V deben advertir que la instalación corresponde a
  personal electricista cualificado, con circuito aislado y verificado, y según
  la normativa local.
- Las cifras de ahorro son datos internos de Voltic; enlaza a
  [voltic.es](https://voltic.es) y evita presentarlas como garantía.

## Validación

Ejecuta, como mínimo:

```bash
mint validate
mint broken-links
mint a11y
```

Si la CLI no está instalada globalmente, usa `npx mintlify <comando>`.
