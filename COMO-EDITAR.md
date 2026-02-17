# Cómo editar el menú sin saber programar

Tu sitio es **estático**: solo muestra el menú. No hay pedidos ni formularios. Todo se edita cambiando archivos de texto.

---

## 1. Cambiar precios, nombres o descripciones de platos

Abre el archivo **`menu.json`** con el Bloc de notas (o cualquier editor de texto).

- **Nombre del restaurante:** busca `"nombre": "Dulce Marrano"` y cámbialo si quieres.
- **Precio:** busca el plato por nombre y cambia el número en `"precio": 40000` (solo el número, sin puntos ni comas).
- **Descripción:** edita el texto entre comillas en `"descripcion": "..."`.
- **Añadir plato:** copia un bloque completo de otro plato (desde `{` hasta `},`) y pégalo en la misma lista; cambia `"id"`, `"nombre"`, `"precio"` y `"descripcion"`. El `"id"` debe ser en minúsculas, sin espacios (ej: `nuevo-plato`).
- **Quitar plato:** borra todo el bloque de ese plato (incluida la coma anterior si la hay). Revisa que no queden comas dobles `,,`.

Guarda el archivo y vuelve a desplegar en Vercel (o recarga la página si estás probando en local).

---

## 2. Añadir o cambiar fotos de los platos

1. **Sube la foto** a la carpeta **`menu-imagenes`** (mismo nivel que `menu.json`).
2. Abre **`menu-imagenes/TAGS.txt`**.
3. Cada línea que **no** empiece por `#` debe tener este formato:
   ```
   id-del-plato|nombre-del-archivo.jpg
   ```
   El **id del plato** es el que aparece en `menu.json` en cada plato (por ejemplo `bondiola-hawaiana`, `bombas-maduro`). El **nombre del archivo** es el de la foto que subiste.

**Ejemplos en TAGS.txt:**
```
bondiola-hawaiana|foto-bondiola.jpg
bombas-maduro|bombas.jpg
nuestra-picada|picada-foto.png
```

Para “desactivar” una línea sin borrarla, pon `#` al inicio (así no se usa para trackear esa imagen).

---

## 3. Desplegar en Vercel

- Sube toda la carpeta del proyecto (con `index.html`, `menu.json`, `menu-imagenes`, etc.) a un repositorio de GitHub.
- En [vercel.com](https://vercel.com) conecta ese repositorio. Cada vez que hagas cambios y los subas a GitHub, Vercel generará el sitio de nuevo.

Si necesitas cambiar solo textos o fotos, edita `menu.json` y `menu-imagenes/TAGS.txt`, sube los cambios a GitHub y en unos minutos se verá en tu enlace de Vercel.
