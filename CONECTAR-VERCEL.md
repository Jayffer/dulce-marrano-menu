# Qué necesitas para conectar el sitio a Vercel

## Necesitas tener:

1. **Cuenta en GitHub** (gratis)  
   → [github.com](https://github.com) → Sign up si no tienes.

2. **Cuenta en Vercel** (gratis)  
   → [vercel.com](https://vercel.com) → Sign up (puedes usar “Continue with GitHub”).

---

## Pasos para publicar

### 1. Subir el proyecto a GitHub

1. Crea un **repositorio nuevo** en GitHub (por ejemplo `dulce-marrano-menu`).
2. En la carpeta del proyecto (`dulce marrano`) abre **Git** (o la terminal de Cursor).
3. Ejecuta (cambia `TU_USUARIO` y `dulce-marrano-menu` por tu usuario y nombre del repo):

```bash
git init
git add .
git commit -m "Menú Dulce Marrano"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/dulce-marrano-menu.git
git push -u origin main
```

Si nunca has usado Git, en GitHub al crear el repo te salen comandos; puedes usar los que te den ahí (sustituyendo por tu carpeta local).

### 2. Conectar el repo con Vercel

1. Entra en [vercel.com](https://vercel.com) e inicia sesión (con GitHub si quieres).
2. Clic en **“Add New…”** → **“Project”**.
3. **Import** el repositorio de GitHub (si no lo ves, autoriza a Vercel para ver tus repos).
4. Vercel detecta que es un sitio estático. No cambies nada (Framework Preset: Other está bien).
5. Clic en **“Deploy”**.

En unos segundos te dará una URL tipo:  
`https://dulce-marrano-menu-xxx.vercel.app`

### 3. Actualizar el menú en el futuro

1. Edita `menu.json` o `menu-imagenes/TAGS.txt` (y sube fotos si quieres) en tu PC.
2. Vuelve a hacer commit y push a GitHub:

```bash
git add .
git commit -m "Actualicé precios"
git push
```

Vercel detecta el cambio y **vuelve a desplegar solo**. En 1–2 minutos la web se actualiza.

---

## Resumen

| Necesitas | Para qué |
|-----------|----------|
| **GitHub** | Guardar el código y que Vercel lo lea |
| **Vercel** | Que te dé la URL pública y el hosting gratis |
| **Git** (en tu PC) | Subir y actualizar el proyecto en GitHub |

No necesitas tarjeta de crédito para el plan gratuito de Vercel.
