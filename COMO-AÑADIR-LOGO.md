# Cómo añadir tu logo real al loader

El loader (pantalla de carga) actualmente muestra un placeholder. Para usar tu logo real:

## Opción 1: Logo como SVG

1. Abre el archivo `assets/logo.svg`
2. Reemplaza el contenido del `<svg>` con tu SVG completo del logo
3. Asegúrate de que el logo tenga `fill="white"` o `fill="#ffffff"` para que se vea blanco sobre el fondo negro

## Opción 2: Logo como imagen (PNG/JPG)

1. Coloca tu logo en `assets/logo.png` (o `.jpg`)
2. Abre `index.html` y busca la línea que dice:
   ```html
   <svg class="loader-logo" ...>
   ```
3. Reemplaza todo el `<svg>` por:
   ```html
   <img class="loader-logo" src="assets/logo.png" alt="Dulce Marrano">
   ```

El logo se mostrará en blanco sobre fondo negro durante 1 segundo al cargar el sitio.
