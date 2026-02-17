# Cómo ver el menú en tu PC (antes de subir a Vercel)

## Opción 1: Con VS Code / Cursor (recomendado)

1. Instala la extensión **"Live Server"** (busca "Live Server" en Extensiones).
2. Clic derecho en `index.html` → **"Open with Live Server"**.
3. Se abrirá el navegador en `http://127.0.0.1:5500` (o similar) y verás el menú.

## Opción 2: Con Node.js (si ya lo tienes)

En la carpeta del proyecto (`dulce marrano`) abre la terminal y ejecuta:

```bash
npx --yes serve .
```

Luego abre en el navegador: **http://localhost:3000**

## Opción 3: Solo abrir el archivo

Doble clic en `index.html` para abrirlo en el navegador.  
*Nota:* En algunos navegadores el menú puede no cargar bien porque `menu.json` se intenta cargar como archivo local. Si ves "Cargando menú…" y no pasa nada, usa Opción 1 o 2.
