# Landing personal · Cristian Ricardo González Ibarra

Sitio estático (HTML + CSS, sin dependencias ni build) listo para publicar en **GitHub Pages**.

```
.
├── index.html        ← toda la página (estilos y script incluidos)
├── assets/foto.jpg   ← foto de perfil
├── .nojekyll         ← le dice a GitHub Pages que sirva los archivos tal cual
└── README.md
```

## Publicarlo en GitHub Pages

### Opción A — URL principal (recomendada): `https://CristianGonzalez23.github.io`

1. En GitHub crea un repositorio **público** llamado exactamente `CristianGonzalez23.github.io`.
2. Desde esta carpeta:

   ```bash
   git init
   git add .
   git commit -m "Landing personal"
   git branch -M main
   git remote add origin https://github.com/CristianGonzalez23/CristianGonzalez23.github.io.git
   git push -u origin main
   ```

3. Ve a **Settings → Pages**, en *Source* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)` y guarda.
4. En 1–2 minutos la página estará en `https://CristianGonzalez23.github.io`.

### Opción B — Como proyecto: `https://CristianGonzalez23.github.io/portafolio`

Igual que la opción A, pero el repositorio puede llamarse como quieras (por ejemplo `portafolio`) y la URL incluye ese nombre.

## Verlo en local

Abre `index.html` en el navegador, o levanta un servidor:

```bash
python3 -m http.server 8000   # luego abre http://localhost:8000
```

## Personalizar

- **Textos:** todo está en `index.html`, organizado por secciones (`#sobre-mi`, `#experiencia`, `#formacion`, `#habilidades`, `#contacto`).
- **Colores:** variables `--brand` y `--brand-2` al inicio del `<style>` (hay una paleta clara y otra oscura automática).
- **Foto:** reemplaza `assets/foto.jpg` (idealmente cuadrada, mínimo 400×400 px).
- **CV descargable (opcional):** copia tu PDF a `assets/cv.pdf` y agrega en la sección de botones:
  `<a class="btn" href="assets/cv.pdf" download>Descargar CV</a>`
- **Dominio propio (opcional):** en *Settings → Pages → Custom domain* escribe tu dominio y configura el DNS según indique GitHub.
