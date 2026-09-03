# Tablero de Dotación PIRC

Tablero ejecutivo de avance de entrega de dotación (Convenio 3007 de 2025 — Unidad para las Víctimas), corte 01/09/2026. Es un único archivo HTML autocontenido: no necesita servidor, base de datos ni build — todos los datos están embebidos directamente en `index.html`.

Este repositorio trae solo lo mínimo:

```
tablero-dotacion-pirc/
├── index.html      ← el tablero completo
├── README.md        ← este archivo
└── .gitignore
```

---

## Opción 1 — Publicar sin usar la terminal (recomendada si no usas git seguido)

1. Entra a [github.com](https://github.com) e inicia sesión (o crea una cuenta si no tienes).
2. Arriba a la derecha, clic en **+ → New repository**.
3. Ponle un nombre, por ejemplo `tablero-dotacion-pirc`. Déjalo en **Public** (para que GitHub Pages funcione gratis). No marques ninguna casilla de inicialización (README, .gitignore, licencia) — las vamos a subir nosotros.
4. Clic en **Create repository**.
5. En la página del repo recién creado, busca el enlace **"uploading an existing file"** (o el botón **Add file → Upload files**).
6. Arrastra los tres archivos de esta carpeta (`index.html`, `README.md`, `.gitignore`) a la zona de carga.
7. Abajo, en "Commit changes", deja el mensaje por defecto y clic en **Commit changes**.
8. Ve a **Settings** (pestaña del repo) → **Pages** (menú izquierdo).
9. En "Build and deployment" → "Source", selecciona **Deploy from a branch**.
10. En "Branch", selecciona `main` y la carpeta `/ (root)`. Clic en **Save**.
11. Espera 1-2 minutos. GitHub te mostrará la URL pública arriba en esa misma página, con el formato:
    `https://<tu-usuario>.github.io/tablero-dotacion-pirc/`

Listo — esa es la URL que puedes compartir.

---

## Opción 2 — Publicar con git desde la terminal (desde cero)

Requisitos: tener [git instalado](https://git-scm.com/downloads) y una cuenta de GitHub.

### 1. Crear el repositorio vacío en GitHub

Entra a github.com → **+ → New repository** → nómbralo `tablero-dotacion-pirc` → **Public** → **Create repository** (sin inicializar con README).

GitHub te mostrará una URL como `https://github.com/<tu-usuario>/tablero-dotacion-pirc.git` — la vas a necesitar en el paso 3.

### 2. Preparar el repositorio local

Abre una terminal, ubícate dentro de esta carpeta (`tablero-dotacion-pirc`) y ejecuta:

```bash
git init
git add index.html README.md .gitignore
git commit -m "Publicar tablero de dotación PIRC"
git branch -M main
```

### 3. Conectar con GitHub y subir

Reemplaza `<tu-usuario>` por tu usuario real de GitHub:

```bash
git remote add origin https://github.com/<tu-usuario>/tablero-dotacion-pirc.git
git push -u origin main
```

Si es la primera vez que usas git desde esa máquina, te pedirá autenticarte (usuario y un *token* de acceso personal, no la contraseña normal — GitHub te guía para crearlo si hace falta).

### 4. Activar GitHub Pages

En el repo, en la web de GitHub: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.

En 1-2 minutos tu tablero queda publicado en:
`https://<tu-usuario>.github.io/tablero-dotacion-pirc/`

---

## Actualizar el tablero más adelante

Cuando tengas un nuevo corte de la base (Anexo1), vuelve a compartírmelo en el chat y te genero un `index.html` actualizado con los mismos formatos, filtros y mapa.

**Sin terminal:** repite el paso 6 de la Opción 1 (subir el nuevo `index.html`, que reemplaza al anterior).

**Con terminal:** desde la misma carpeta, con el nuevo `index.html` ya copiado encima del anterior:

```bash
git add index.html
git commit -m "Actualizar tablero con nuevo corte"
git push
```

GitHub Pages republica automáticamente en 1-2 minutos, sin que tengas que tocar la configuración otra vez.
