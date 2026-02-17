# Borrado de fondo en lote (Adobe Express)

Esta herramienta te ayuda a borrar el fondo de muchas fotos usando **Adobe Express Embed SDK** y exportar **PNG** con transparencia.

## 1) Configurar el Client ID

1. En Adobe Developer Console crea una app del **Embed SDK**.
2. Copia tu **Client ID**.
3. Copia `config.example.js` a `config.js` y pega tu Client ID:
   - `tools/express-bg-remove/config.js`

**Allowed origins (muy importante):** agrega al menos:

- `http://localhost:5500` (si usas Live Server)
- `https://dulce-marrano-menu.vercel.app` (tu Vercel)

Docs: `https://developer.adobe.com/express/embed-sdk/` y quick action remove background: `https://developer.adobe.com/express/embed-sdk/docs/guides/quick_actions`

## 2) Cómo usar

1. Abre `tools/express-bg-remove/index.html` con Live Server **o** en Vercel:
   - En local: `http://127.0.0.1:5500/tools/express-bg-remove/`
   - En Vercel: `https://dulce-marrano-menu.vercel.app/tools/express-bg-remove/`
2. Selecciona varias fotos.
3. Clic en **Procesar siguiente**.
4. En Adobe Express, clic en **Descargar PNG**.

## Nota importante (sobre “automático”)

Por seguridad del navegador, **no se pueden descargar 50 archivos sin interacción**. Por eso el flujo es: abrir → borrar fondo → **un clic** para descargar cada PNG.

