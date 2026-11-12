# Prototipo de diseño · Ficha de club y alta (no oficial)

**Prototipo no oficial.** Experimento de diseño front-end hecho por Hanzo (hanzo.es) para explorar mejoras en el producto digital de un cliente. No es una página oficial de la marca que aparece, no está publicada ni respaldada por ella y no es un producto en funcionamiento. No hay registro, acceso de usuarios ni pago reales: la página no contiene formularios ni campos de texto, los "campos" se rellenan con datos de ejemplo al tocarlos y no se envía ni se guarda nada. No hace peticiones a terceros. Las marcas pertenecen a sus respectivos propietarios.

## Qué es

Un único `index.html` autocontenido (estilos, scripts e imágenes en línea; la tipografía Inter se sirve desde `fonts/`, licencia OFL). Pensado para móvil (320–440 px); en escritorio se muestra como una columna de móvil centrada.

Rutas por hash: `#inicio`, `#extras`, `#contacto`, `#datos`, `#pago`, `#visita`, `#confirmacion`.

## Reglas anti-phishing que cumple (no romperlas al editar)

- Ningún `<form>`, `<input>`, `<select>` ni `<textarea>`, tampoco generados por JS. Los campos son `<span class="fx-in|fx-chk|fx-sel">` con un pequeño shim que les da `.value` / `.checked`.
- Sin campos de tarjeta, sin login, sin enlaces externos (los de mapas muestran un aviso).
- Cero peticiones cross-origin (nada de Google Fonts ni CDNs).
- `<meta name="robots" content="noindex,nofollow">`; sin `og:*`, `twitter:*`, canonical ni JSON-LD.
- `robots.txt` permite el rastreo a propósito, para que Google pueda leer el `noindex`.
