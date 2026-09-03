# Documentación de Voltic

Este repositorio contiene la documentación pública de Voltic, publicada con
[Mintlify](https://mintlify.com). Los archivos `.mdx` son la fuente de verdad;
`docs.json` define la navegación, los idiomas y los productos.

## Estructura

La navegación está organizada por oferta y, dentro de cada oferta, por el
recorrido del lector:

- **Hotel Room Control**: empezar, instalar, operar, referencia y soporte.
- **Voltic FrostLine**: producto independiente para viviendas y otras
  instalaciones, con instalación, compatibilidad y funcionamiento.
- **Cooling Patrol**: empezar, instalar y soporte. Su ampliación funcional,
  especialmente la operación con capturas de la app, queda planificada para
  una tarea posterior.

Hotel Room Control integra FrostLine cuando se instala en un hotel, mientras
que la guía independiente cubre viviendas y hubs Tuya. Las rutas de las
páginas se mantienen estables aunque cambie su posición en la navegación. La
versión española vive en la raíz y la inglesa bajo `en/`.

## Edición local

Requisitos: Node.js y la CLI de Mintlify.

```bash
mint dev
mint validate
mint broken-links
mint a11y
```

Abre la URL local que muestre `mint dev` para previsualizar los cambios. Antes
de añadir una página, crea el `.mdx`, añade su ruta en `docs.json` para ambos
idiomas y comprueba los enlaces internos.

## Criterios de contenido

- Mantén el contenido equivalente en español e inglés.
- Conserva las URLs existentes; si una URL debe cambiar, añade una redirección
  explícita en `docs.json`.
- Usa nombres de producto canónicos: **Voltic Freeline** es el control de
  habitación y **Voltic FrostLine** es el termostato.
- Toda instrucción que implique 230 V debe indicar personal cualificado,
  aislamiento y verificación del circuito, además de la normativa local.
- No inventes especificaciones. Para las cifras comerciales de ahorro, enlaza
  a [voltic.es](https://voltic.es) y deja claro que son datos internos de Voltic.
- Usa texto alternativo descriptivo en imágenes y valida los enlaces antes de
  publicar.

Las capturas y la ampliación operativa de Cooling Patrol se incorporarán en
una tarea independiente cuando estén disponibles las pantallas de la app.
