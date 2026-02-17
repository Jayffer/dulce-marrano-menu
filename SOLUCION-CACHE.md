# El sitio no se actualiza - Solución

Si abriste `index.html` y no ves los cambios nuevos, el navegador está usando una versión guardada (caché).

## Solución rápida

1. **Cierra completamente el navegador** (todas las ventanas).
2. **Vuelve a abrir** el archivo `index.html`.

## Si aún no funciona

### Opción 1: Recarga forzada (sin caché)
- Presiona **Ctrl + F5** (o **Ctrl + Shift + R**)
- Esto fuerza al navegador a descargar todo de nuevo

### Opción 2: Limpiar caché manualmente
- **Chrome/Edge:** Presiona **F12** → pestaña "Network" → marca "Disable cache" → recarga
- **Firefox:** Presiona **Ctrl + Shift + Delete** → marca "Caché" → "Limpiar ahora"

### Opción 3: Usar servidor local (recomendado)
En lugar de abrir directamente el archivo, usa un servidor:

**En Cursor:**
1. Instala la extensión **"Live Server"**
2. Clic derecho en `index.html` → **"Open with Live Server"**
3. Se abrirá en `http://127.0.0.1:5500` y siempre verás la versión más reciente

**O desde terminal:**
```bash
npx --yes serve .
```
Luego abre: **http://localhost:3000**

---

## Verificar que los cambios están

Abre `index.html` en un editor de texto y busca:
- Línea 6: `<meta name="theme-color" content="#654418">` (debe ser #654418)
- Línea 25: `--texto: #654418;` (debe ser ese color)
- Línea 26: `--fondo: #f0e8db;` (debe ser ese color)

Si ves esos valores, el archivo está actualizado y solo necesitas limpiar la caché del navegador.
