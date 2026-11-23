# Nilo Sur - Landing page de artista

Landing page de una sola página para **Nilo Sur**, guitarrista y compositor ficticio de flamenco-jazz. Proyecto del módulo de HTML, CSS y SEO, hecho **solo con HTML y CSS** (sin JavaScript ni frameworks).

## Dos versiones

| Versión | Archivos | Estado |
|---------|----------|--------|
| Generada con IA | `index-IA.html` + `style-IA.css` | Terminada |
| Escrita a mano | `index.html` + `styles.css` | En progreso |

## Estructura

```
index-IA.html / style-IA.css   Versión IA
index.html / styles.css        Versión manual
img/                           Imágenes, logo y caricatura (créditos en img/CREDITOS.md)
memory-bank/projectbrief.md    Contenido del artista y requisitos del proyecto
lighthouse/                    Informes de Lighthouse (escritorio y móvil)
```

## Requisitos cubiertos

- **Secciones:** portada, Sobre mí, Trayectoria y Próximas presentaciones, cada una del alto de la pantalla, con barra de navegación.
- **HTML semántico:** `header`, `nav`, `main`, `section`, `article`, `footer`, `time`, `address`.
- **Accesibilidad (WCAG 2.1 AA):** textos `alt`, `aria-label`, enlace para saltar al contenido, foco visible, contraste verificado, `prefers-reduced-motion` y atajos de teclado (`Alt` + `1`, `2`, `3`).
- **SEO:** `title`, `meta description`, Open Graph y datos estructurados de Schema.org en JSON-LD (`Person`, `MusicEvent`, `MusicAlbum`).

## Validación de la versión IA

- W3C HTML: 0 errores. W3C CSS: 0 errores.
- Schema.org Validator: 0 errores, 0 avisos.
- Lighthouse: Accesibilidad 100 y SEO 100 en escritorio y móvil.

## Ver la página

```bash
pip3 install flask && python3 server.py
```

Abre `http://localhost:3000/index-IA.html` (versión IA) o `http://localhost:3000` (versión manual).

## Créditos

Fotografías con licencia CC BY 2.0; autores y enlaces en [img/CREDITOS.md](img/CREDITOS.md). El artista, la banda y los eventos son ficticios.
