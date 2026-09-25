# COSTOS: Taller de Costos y Presupuestos

App escolar para armar el presupuesto de una obra: partidas, conceptos, matrices, básicos, cuadrillas, insumos, indirectos, utilidad, factor de sobrecosto y formatos impresos. Publicada en https://vmmterminus-star.github.io/costos/

## Cómo está hecha
- Todo vive en un solo `index.html` (HTML + CSS + JS juntos). No hay que instalar ni compilar nada.
- Fuentes: Alexandria e IBM Plex Mono. Color de tema: `#123C47`.
- Los íconos van embebidos en base64/SVG en el `<head>`.

## Datos (¡cuidado!)
- Se guardan en `localStorage` con la clave `costos_v3`.
- Tiene respaldo en `.json`, un "puente por código" (exportar/importar pegando texto) y sincronización con Supabase. La sincronización está desactivada porque `SUPA_URL` y `SUPA_KEY` están vacíos; la tabla sería `costos_sync`.
- **Vista para el profe:** con `?rev=1` la página carga `revision.json` en vez de los datos locales. Con `?rev=<nombre>` carga `<nombre>.json`. En este repo están `revision especifica.json` y `revisiongeneral.json`: no los borres ni los renombres sin avisar, porque el profe puede tener esos links.
- Nunca cambies nombres de claves ni la forma de los datos sin migrar lo que ya existe.

## Cómo trabajar con Valen
- Valen no programa. Explícale todo en español sencillo, sin tecnicismos.
- Antes de subir cualquier cambio: abre la app en el navegador integrado, prueba el cambio (también en tamaño celular) y revisa la consola.
- Enséñale el resultado. Haz commit y push a `main` solo cuando ella diga que sí. En ~1 minuto queda en línea.
- El repo es público: nada de contraseñas ni datos personales aquí.
