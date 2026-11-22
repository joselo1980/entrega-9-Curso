# Rodó & Asociados

Sitio web del estudio jurídico y notarial Rodó & Asociados, de Parque Rodó, Montevideo. Es el proyecto del curso de Desarrollo Web de Coderhouse.

## Sitio publicado

https://joselo1980.github.io/entrega-8-Curso/

## Pre-entrega 8: Animaciones y full-responsive

- **Animación nativa:** `@keyframes aparecer` en `scss/base/_base.scss`, aplicada con el mixin `aparecer()` al título principal y a las fotos. Las tarjetas, botones y links tienen `transition` en `:hover`.
- **Librería de animación:** AOS por CDN en los 5 HTML (`data-aos="fade-up"` en las tarjetas).
- **SCSS avanzado:** mixins con parámetros (`columna($espacio)` y `aparecer($duracion, $demora)` en `_mixins.scss`), `@extend` del placeholder `%titulo-base` en `_tipografia.scss` y operadores en `_variables.scss` (`$espacio-chico * 2`).
- **Responsive en los 5 HTML** con tres medidas: base mobile sin media query, `@media (min-width: 768px)` para tablet y `@media (min-width: 1024px)` para escritorio (mixins `tablet` y `escritorio`). Probado de 1400px a 375px sin scroll horizontal.

## Pre-entrega 7: Arquitectura SCSS

Todo el CSS propio está escrito en SCSS y se compila a un único archivo `css/style.css`. Bootstrap se sigue cargando por CDN en los 5 HTML.

### Estructura

```
scss/
├── main.scss              (único punto de entrada, usa @use)
├── utilities/
│   ├── _variables.scss    (colores, tipografías, espacios, breakpoint)
│   └── _mixins.scss       (media queries, columna flex y animación)
├── base/
│   ├── _base.scss         (reset y estilos generales)
│   └── _tipografia.scss   (títulos y textos)
├── layout/
│   ├── _header.scss       (navbar de Bootstrap: barra, logo y marca)
│   ├── _nav.scss          (links del menú y sus estados)
│   ├── _grillas.scss      (grillas de inicio, servicios y nosotros)
│   └── _footer.scss       (pie de página y redes)
└── components/
    ├── _buttons.scss
    ├── _cards.scss
    ├── _carousel.scss     (carousel de Bootstrap)
    └── _modal.scss        (modal de Bootstrap)
css/
└── style.css              (archivo compilado, no se edita a mano)
```

### Cómo compilar

Desde la carpeta del proyecto:

```
npx sass scss/main.scss css/style.css
```

## Páginas

- Inicio (index.html)
- Nosotros (pages/sobre-mi.html)
- Preguntas frecuentes (pages/proyectos.html)
- Servicios (pages/servicios.html)
- Contacto (pages/contacto.html)

## Cómo verlo

Entrar al link del sitio publicado, o descargar el repositorio y abrir el archivo index.html en el navegador.
