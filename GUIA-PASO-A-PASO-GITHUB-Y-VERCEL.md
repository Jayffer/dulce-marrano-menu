# Guía para tontos: subir el menú a Internet con GitHub y Vercel

Todo es **gratis**. No piden tarjeta. Solo seguir los pasos en orden.

---

## ¿Qué es cada cosa en una frase?

- **GitHub** = Un sitio donde guardas el “código” del menú en la nube (como un Drive pero para proyectos).
- **Vercel** = Un sitio que toma lo que tienes en GitHub y lo convierte en una **página web con su propia dirección** (link que puedes compartir).
- **Git** = Un programa en tu PC que sirve para “subir” tu carpeta del menú a GitHub.

---

# PARTE 1: Crear cuenta en GitHub

1. Abre el navegador y ve a: **https://github.com**
2. Arriba a la derecha verás **“Sign up”** (Registrarse). Haz clic ahí.
3. Te pedirán:
   - **Email:** el que uses normalmente.
   - **Contraseña:** inventa una (mínimo algo así: 8 caracteres, con letras y números).
   - **Usuario:** el nombre con el que te identificarás (ej: `juanperez` o `dulcemarrano`). Anótalo, lo usarás luego.
4. Pueden pedirte verificar que no eres robot (elige imágenes, etc.).
5. Cuando termines, ya estás dentro de GitHub. **No cierres esa pestaña.**

---

# PARTE 2: Instalar Git en tu PC (solo una vez)

Git es lo que permite “subir” tu carpeta a GitHub desde Cursor.

1. Ve a: **https://git-scm.com/download/win**
2. Se descargará un instalador. Ábrelo.
3. En las ventanas que salgan, no cambies nada: solo haz clic en **“Next”** (Siguiente) hasta que diga **“Finish”**.
4. Cierra Cursor si lo tenías abierto y vuelve a abrirlo (para que reconozca Git).

---

# PARTE 3: Crear el “repositorio” en GitHub

Un “repositorio” es como una carpeta vacía en GitHub donde vas a subir tu proyecto.

1. En GitHub (en el navegador), arriba a la izquierda verás un símbolo **+**. Haz clic ahí.
2. En el menú que se abre, elige **“New repository”**.
3. En la página que sale:
   - **Repository name:** escribe exactamente: **dulce-marrano-menu** (o el nombre que quieras, sin espacios).
   - **Description:** puedes dejarlo vacío o poner “Menú del restaurante”.
   - **Public** debe estar marcado (un círculo).
   - **NO marques** la casilla “Add a README file”.
   - **NO elijas** “Add .gitignore” ni “Choose a license”.
   - Deja todo lo demás como está.
4. Abajo haz clic en el botón verde **“Create repository”**.
5. Te llevará a una página que dice “Quick setup” y tiene una dirección que termina en `.git`. **No hagas nada más en esa página.** Solo deja esa pestaña abierta; ya tienes el “repositorio” creado.

---

# PARTE 4: Subir tu carpeta del menú a GitHub desde Cursor

Aquí conectas la carpeta de tu PC con el repositorio que acabas de crear y “subes” todo.

1. Abre **Cursor** y abre la carpeta del proyecto: **dulce marrano** (la que tiene `index.html`, `menu.json`, etc.).
2. Abre la **Terminal** dentro de Cursor:
   - Arriba en el menú: **Terminal** → **New Terminal**
   - O atajo: **Ctrl + Ñ** (o **Ctrl + `** según el teclado).
   - Abajo aparecerá una ventanita con una línea donde puedes escribir.
3. Comprueba que estás en la carpeta correcta: debe salir algo como `dulce marrano` en la ruta. Si no, escribe y pulsa Enter:
   ```
   cd "c:\Users\ASUS\Desktop\dulce marrano"
   ```
4. Ahora vas a pegar **tres comandos**, uno detrás de otro. Después de cada uno pulsa **Enter** y espera a que termine antes del siguiente.

   **IMPORTANTE:** En la terminal solo debes pegar **la línea del comando**. No copies los símbolos \`\`\` ni la palabra `bash`; eso es solo formato del documento y la terminal no lo entiende.

   **Comando 1** (enlazar tu carpeta con el repo de GitHub).  
   Si tu usuario de GitHub es **Jayffer**, pega exactamente esto (solo esta línea):
   ```
   git remote add origin https://github.com/Jayffer/dulce-marrano-menu.git
   ```
   Si tu usuario es otro, cambia `Jayffer` por tu usuario. Luego Enter.

   **Comando 2** — pega solo esta línea:
   ```
   git branch -M main
   ```
   Enter.

   **Comando 3** — pega solo esta línea:
   ```
   git push -u origin main
   ```
   Enter.

5. La **primera vez** que hagas el Comando 3 puede abrirse una ventana del navegador o pedirte **usuario y contraseña**:
   - **Usuario:** tu usuario de GitHub.
   - **Contraseña:** GitHub ya no acepta la contraseña normal. Tienes que usar un **Token**:
     - En GitHub (navegador): clic en tu foto (arriba derecha) → **Settings**.
     - En el menú de la izquierda, abajo: **Developer settings** → **Personal access tokens** → **Tokens (classic)**.
     - **Generate new token (classic)**. Ponle un nombre (ej: “Cursor”) y marca la casilla **repo**.
     - **Generate token**. Copia el token (solo se muestra una vez) y **úsalo como contraseña** donde te pida la contraseña de GitHub.
6. Cuando el Comando 3 termine sin error, vuelve a la pestaña de GitHub y **actualiza la página** (F5). Deberías ver todos los archivos del menú (index.html, menu.json, etc.). **Ya está subido.**

---

# PARTE 5: Crear cuenta en Vercel y publicar la web

Vercel toma lo que está en GitHub y te da un enlace para ver el menú en Internet.

1. Ve a: **https://vercel.com**
2. Arriba a la derecha: **“Sign Up”** (o “Log In” si ya tienes cuenta).
3. Elige **“Continue with GitHub”**. Te pedirá autorizar a Vercel para ver tus repositorios. Acepta (Authorize).
4. Cuando entres en Vercel, verás algo como “Add New…” o “Create”. Haz clic en **“Add New…”** y luego en **“Project”**.
5. En la lista de repositorios, busca **dulce-marrano-menu** (o el nombre que pusiste). Al lado tendrá un botón **“Import”**. Haz clic en **Import**.
6. En la siguiente pantalla **no cambies nada**. Solo revisa que diga algo como “Framework Preset: Other”. Abajo haz clic en el botón **“Deploy”**.
7. Espera unos segundos (o un minuto). Verás que “Building” y luego “Ready”.
8. Verás un mensaje tipo **“Congratulations!”** y un **enlace** (URL) que empieza por `https://dulce-marrano-menu-...vercel.app`. Ese es el enlace de tu menú. Haz clic ahí y se abrirá tu menú en el navegador. **Ese link es el que compartes con la gente.**

---

# PARTE 6: Cuando quieras cambiar el menú (precios, platos, fotos)

1. En tu PC, edita los archivos como siempre:
   - **menu.json** → precios, nombres, descripciones.
   - **menu-imagenes/TAGS.txt** y las fotos en **menu-imagenes** → imágenes de platos.
2. En Cursor, con la carpeta del proyecto abierta, abre la **Terminal** (Terminal → New Terminal).
3. Ejecuta estos **tres comandos** en orden (cada uno, Enter):
   ```bash
   git add .
   git commit -m "Actualicé el menú"
   git push
   ```
   Si te pide usuario/contraseña, usa otra vez tu usuario de GitHub y el **token** como contraseña.
4. En **2–3 minutos** entra otra vez en el enlace de Vercel (el que te dio en la Parte 5). La web se habrá actualizado sola con los cambios.

---

# Resumen rápido

| Paso | Dónde | Qué haces |
|------|--------|-----------|
| 1 | github.com | Crear cuenta (Sign up). |
| 2 | git-scm.com | Descargar e instalar Git en el PC. |
| 3 | github.com | Crear repositorio nuevo (dulce-marrano-menu), sin README. |
| 4 | Cursor (Terminal) | Los 3 comandos: `git remote add...`, `git branch -M main`, `git push -u origin main`. |
| 5 | vercel.com | Crear cuenta con GitHub, Import el repo, Deploy. |
| 6 (futuro) | Cursor + editar archivos | Editar menu.json o fotos, luego `git add .` → `git commit -m "..."` → `git push`. |

Si algo no te sale (por ejemplo “error” en la terminal), copia el mensaje de error y pide ayuda indicando en qué parte ibas (Parte 1, 2, 3, 4, 5 o 6).
