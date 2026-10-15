# MultiCalc Studios Web

Sitio público de **MultiCalc Studios**, con información y políticas de privacidad de sus aplicaciones.

## Contenido

- `docs/index.html`: página de MultiCalc Studios.
- `docs/multicontador/index.html`: página pública de MultiContador.
- `docs/multicontador/privacidad/index.html`: Política de Privacidad de MultiContador de efectivo.
- `docs/multicontador/assets/icons/`: copias sin modificar de los iconos utilizados en el sitio.
- `docs/.nojekyll`: publicación directa de los archivos estáticos.

## Publicación

GitHub Pages publica desde la rama `main`, carpeta `/docs`, del repositorio `multicalcstudios/multicalc-studios-web`.

El sitio es HTML con CSS incorporado. No requiere build, dependencias, JavaScript, backend ni autenticación. Los enlaces internos son relativos y funcionan bajo el prefijo del repositorio en GitHub Pages.

Para actualizar la política, editar `docs/multicontador/privacidad/index.html`, revisar el contenido y publicar los cambios en `main`.

## Iconos

Los originales se conservan localmente en `public/multicontador/assets/icons/`, fuera de la publicación. GitHub Pages sirve las copias seleccionadas en `docs/multicontador/assets/icons/`; conservan sus nombres y bytes originales. No se generan ni convierten imágenes durante la publicación.

El icono principal es `android-chrome-512x512.png`, con su variante existente de 192 px para tamaños pequeños. Los favicons usan los PNG existentes de 16 y 32 px, y el acceso directo de Apple usa `apple-touch-icon.png` de 180 px. Open Graph utiliza el icono cuadrado de 512 px. No se publica una imagen panorámica generada.

## Contacto

[multicalcstudios@gmail.com](mailto:multicalcstudios@gmail.com)
