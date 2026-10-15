# MultiCalc Studios Web

Sitio oficial de **MultiCalc Studios**: catálogo de aplicaciones, información de producto, soporte y políticas de privacidad.

## Contenido

- `docs/index.html`: página de MultiCalc Studios.
- `docs/apps/index.html`: catálogo de aplicaciones.
- `docs/multicontador/index.html`: página pública de MultiContador.
- `docs/acerca-de/index.html`: enfoque del estudio.
- `docs/soporte/index.html`: contacto y guía para reportar problemas.
- `docs/multicontador/privacidad/index.html`: Política de Privacidad de MultiContador de efectivo.
- `docs/404.html`: página de error con enlaces de recuperación; conserva el HTTP 404 de Pages.
- `docs/assets/css/site.css`: estilos compartidos de navegación, layout, cards, botones, footer y documento legal.
- `docs/multicontador/assets/icons/`: copias sin modificar de los iconos utilizados en el sitio.
- `docs/.nojekyll`: publicación directa de los archivos estáticos.

## Publicación

GitHub Pages publica desde la rama `main`, carpeta `/docs`, del repositorio `multicalcstudios/multicalc-studios-web`.

El sitio es HTML con una hoja CSS compartida. No requiere build, dependencias, JavaScript, backend ni autenticación. Los enlaces del sitio incluyen explícitamente el prefijo `/multicalc-studios-web/`; funcionan también en las rutas anidadas y en la página 404. Las URL canonical y Open Graph incluyen el dominio HTTPS real de Pages.

La navegación es HTML público en cada página; no se inyecta desde JavaScript. El menú móvil usa `details/summary`, accesible con teclado y sin scripts. Al actualizar enlaces globales, mantener el mismo header y footer en las seis páginas y en `404.html`; cada página principal indica su enlace activo con `aria-current="page"`.

Para actualizar la política, editar `docs/multicontador/privacidad/index.html`, revisar el contenido y publicar los cambios en `main`.

## Añadir aplicaciones

1. Crear `docs/<slug>/index.html` reutilizando el header, footer y metadatos de una página existente. Ajustar title, description, canonical y Open Graph.
2. Añadir un `article.app-card` dentro de `.app-grid` en el catálogo y, si corresponde, en el inicio. La rejilla se adapta al número de aplicaciones sin cambiar CSS.
3. Usar funciones, imágenes, estado de disponibilidad y enlaces reales. No publicar fichas vacías ni aplicaciones anunciadas sin confirmar.
4. Crear la política específica de esa aplicación cuando corresponda, sin reutilizar como propia la de MultiContador.
5. Añadir los archivos públicos exactos a la lista permitida de `.gitignore`; revisar el diff, enlaces, accesibilidad y tamaños de pantalla antes del push.

La navegación presenta las áreas principales del sitio; añadir una app al catálogo no requiere añadirla al menú global.

## Iconos

Los originales se conservan localmente en `public/multicontador/assets/icons/`, fuera de la publicación. GitHub Pages sirve las copias seleccionadas en `docs/multicontador/assets/icons/`; conservan sus nombres y bytes originales. No se generan ni convierten imágenes durante la publicación.

El icono principal es `android-chrome-512x512.png`, con su variante existente de 192 px para tamaños pequeños. Los favicons usan los PNG existentes de 16 y 32 px, y el acceso directo de Apple usa `apple-touch-icon.png` de 180 px. Open Graph utiliza el icono cuadrado de 512 px. No se publica una imagen panorámica generada.

Actualmente el único recurso de identidad gráfico disponible es el icono de MultiContador. También se reutiliza como favicon e imagen social del sitio; el nombre del estudio se presenta como texto, sin inventar un logo corporativo.

## Capturas de MultiContador

`public/multicontador/assets/screenshots/README.txt` reserva la carpeta para añadir manualmente capturas reales y autorizadas. No contiene imágenes de ejemplo. Solo se versiona ese README; los futuros archivos quedan excluidos hasta revisarlos expresamente.

La sección `section.screenshots` en la página de MultiContador está oculta con `hidden`. Para activarla:

1. Revisar que las capturas reales no incluyan información privada.
2. Copiar los archivos revisados a `docs/multicontador/assets/screenshots/` y permitir solo esos nombres exactos en `.gitignore`.
3. Añadir elementos `figure` con `img`, dimensiones reales, `alt` descriptivo, `loading="lazy"` y `figcaption` dentro de `.screenshot-grid`.
4. Usar rutas con el prefijo `/multicalc-studios-web/` y retirar `hidden` cuando las imágenes estén disponibles y comprobadas.

Mientras no exista una URL pública confirmada de Google Play, el producto muestra la etiqueta «Próximamente en Google Play», sin enlace ni botón de descarga ficticio.

## Comprobación antes de publicar

Revisar todas las páginas en 320, 360, 390, 412, 768, 1024 y 1440 px; comprobar teclado, menú móvil, navegación directa, recarga, incógnito, recursos y política legal. Comprobar también que una URL inexistente conserva HTTP 404 y presenta la página de recuperación.

Mantener la política pública e indexable. No añadir analítica, cookies, servicios externos ni scripts al sitio. El copyright del footer es estático (`2026`); actualizarlo cuando corresponda.

Antes del push, verificar `gh api user --jq .login` (`multicalcstudios`), `git remote -v`, estado, diff y archivos incluidos. Publicar únicamente en `multicalcstudios/multicalc-studios-web`, sin force push.

## Contacto

[multicalcstudios@gmail.com](mailto:multicalcstudios@gmail.com)
