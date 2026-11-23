# Project Brief - Landing page de Nilo Sur

Documento base para construir la página. Todo el contenido del artista es **ficticio** (inventado para el ejercicio).

---

## 1. Contexto del encargo

Un amigo artista necesita darse a conocer y mostrar su talento en internet. Esta es la **versión inicial** de su web: una sola página (landing page) que más adelante podrá crecer, pero que debe ser un trabajo de calidad desde el principio.

---

## 2. El artista

| Dato | Valor |
|------|-------|
| Nombre artístico | **Nilo Sur** |
| Nombre real | Martín Lozada Quiroga |
| Disciplina | Guitarrista y compositor |
| Género | Fusión de flamenco, jazz y música latinoamericana |
| Ciudad | Valencia, España |
| Eslogan (portada) | *"Cuerdas que cruzan océanos."* |
| Email de contacto | contacto@nilosur.example |
| Redes | Instagram, YouTube, Spotify (enlaces de ejemplo con dominio `.example`) |

### Sobre el artista

Nilo Sur creció entre la guitarra flamenca de su abuelo andaluz y los discos de jazz y bossa nova que llegaban a casa desde Montevideo, la ciudad natal de su madre. De esa mezcla nació un sonido propio: compases de bulería que se abren a armonías de jazz y ritmos de candombe.

Formado en el Conservatorio Superior de Música de Valencia, hoy compone para guitarra sola y para su trío, **Nilo Sur Trío** (guitarra, contrabajo y percusión). En directo combina la intimidad de una guitarra acústica con la improvisación, y cada concierto es distinto al anterior.

---

## 3. Trayectoria

| Año | Hito |
|-----|------|
| 2016 | Se gradúa en guitarra en el Conservatorio Superior de Música de Valencia. |
| 2018 | Funda **Nilo Sur Trío** con Clara Benet (contrabajo) e Iván Roca (percusión). |
| 2020 | Publica su primer álbum, ***Raíz de agua***, grabado de forma independiente. |
| 2022 | Primer premio en el Certamen Nacional de Guitarra Contemporánea (ficticio). |
| 2024 | Gira de 15 conciertos por España y Uruguay. |
| 2025 | Publica su segundo álbum, ***Mareas del Sur***. |

---

## 4. Próximas presentaciones

| Fecha | Hora | Evento | Lugar | Ciudad |
|-------|------|--------|-------|--------|
| 2026-12-12 | 21:00 | Concierto acústico *Raíz de agua* | Sala La Cúpula | Valencia |
| 2027-01-23 | 20:30 | Presentación de *Mareas del Sur* con el Trío | Teatro del Puerto | Barcelona |
| 2027-02-14 | 21:30 | Noche de guitarra y jazz | Café Central del Sur | Madrid |
| 2027-03-20 | 19:00 | Festival Cuerdas del Mediterráneo | Auditorio Mar Abierto | Alicante |

Cada evento tendrá un enlace "Comprar entradas" (URL de ejemplo).

---

## 5. Imágenes necesarias

| Imagen | Tamaño | Uso | Texto alternativo (`alt`) |
|--------|--------|-----|---------------------------|
| `img/nilo-sur-portada.jpg` | 1024x683 | Fondo de la portada | Decorativa: va como fondo CSS, sin `alt` |
| `img/nilo-sur-retrato.jpg` | 683x1024 | Sección Sobre mí | "Nilo Sur toca la guitarra española sentado junto a un muro de piedra, iluminado por un farol en la noche" |
| `img/mareas-del-sur.jpg` | 734x734 | Trayectoria (álbum 2025) | "Portada del álbum Mareas del Sur: una ola rompe contra las rocas frente al sol del atardecer" |
| `img/raiz-de-agua.jpg` | 683x683 | Trayectoria (álbum 2020) | "Portada del álbum Raíz de agua: primer plano en blanco y negro de las cuerdas de una guitarra acústica" |
| `img/guitarra-detalle.jpg` | 1023x654 | Fondo decorativo (Sobre mí o Trayectoria) | Decorativa: fondo CSS, sin `alt` |
| `img/presentaciones-publico.jpg` | 1024x768 | Fondo de Próximas presentaciones (con capa oscura encima) | Decorativa: fondo CSS, sin `alt` |
| `img/nilo-sur-logo.svg` | 420x120 | Logo en la barra de navegación y footer | "Nilo Sur" (o `alt=""` si va junto al nombre en texto) |
| `img/nilo-sur-perfil.svg` | 600x400 | Caricatura del trío en Sobre mí o Trayectoria (hito 2018); para `og:image` usar un JPG, las redes no aceptan SVG | "Caricatura de Nilo Sur Trío: Clara Benet con el contrabajo, Nilo Sur con la guitarra e Iván Roca con el cajón" |

Las fotos tienen licencia CC BY 2.0. Los créditos están en `img/CREDITOS.md` y también deben aparecer en el pie de página. El logo y el perfil son ilustraciones SVG originales.

---

## 6. Lo que tenemos que entregar

### 6.1 Archivos

```
html-hello/
├── index.html
├── styles.css
├── memory-bank/
│   └── projectbrief.md
└── img/
    ├── nilo-sur-portada.jpg
    ├── nilo-sur-retrato.jpg
    ├── mareas-del-sur.jpg
    ├── raiz-de-agua.jpg
    ├── guitarra-detalle.jpg
    ├── presentaciones-publico.jpg
    ├── nilo-sur-logo.svg
    ├── nilo-sur-perfil.svg
    └── CREDITOS.md
```

### 6.2 Estructura de la página

Una sola página. **Cada sección ocupa aproximadamente el alto de la pantalla** (`min-height: 100vh`).

| # | Sección | `id` | Contenido |
|---|---------|------|-----------|
| - | Barra de navegación | - | Enlaces a Sobre mí, Trayectoria y Próximas presentaciones |
| 1 | Portada / Bienvenida | `#inicio` | Nombre (`<h1>`), disciplina, eslogan, botón hacia las presentaciones |
| 2 | Sobre mí | `#sobre-mi` | Biografía y retrato |
| 3 | Trayectoria | `#trayectoria` | Línea de tiempo con los hitos |
| 4 | Próximas presentaciones | `#presentaciones` | Tarjetas de evento con fecha, lugar y enlace |
| - | Pie de página | - | Contacto, redes y copyright |

### 6.3 Esqueleto semántico

```
<body>
  <a> Saltar al contenido
  <header>
    <nav aria-label="Navegación principal">
  <main id="contenido">
    <section id="inicio">          h1
    <section id="sobre-mi">        h2 + <figure>
    <section id="trayectoria">     h2 + <ol> con <time>
    <section id="presentaciones">  h2 + <article> por evento con <time datetime>
  <footer>
    <address> contacto y redes
```

### 6.4 Accesibilidad

- `lang="es"` en `<html>`.
- Enlace "Saltar al contenido" como primer elemento del `<body>`.
- `aria-label` en el `<nav>` y `aria-labelledby` en cada `<section>` apuntando a su encabezado.
- Un solo `<h1>`; `<h2>` por sección; `<h3>` dentro; sin saltos de nivel.
- `alt` descriptivo en imágenes de contenido; las decorativas van como fondo CSS o con `alt=""`.
- Textos de enlace que tengan sentido por sí solos ("Comprar entradas para Teatro del Puerto", no "click aquí"). Si el texto visible es corto, completar con `aria-label`.
- Enlaces externos que abren en otra pestaña lo avisan (texto o `aria-label`).
- Iconos de redes: `aria-hidden="true"` en el icono y nombre accesible en el enlace.
- Fechas con `<time datetime="2026-12-12T21:00">`.
- Foco visible con `:focus-visible` en todos los elementos interactivos.
- Contraste mínimo 4.5:1 en texto normal y 3:1 en texto grande (ver paleta en 6.7).
- Animaciones desactivadas con `@media (prefers-reduced-motion: reduce)`.
- La página funciona con zoom al 200% y en móvil sin scroll horizontal.

### 6.5 SEO

- `<title>`: "Nilo Sur | Guitarrista y compositor de flamenco-jazz".
- `<meta name="description">` de unos 150 caracteres.
- `<meta name="viewport">` y `<meta charset="UTF-8">`.
- Open Graph: `og:title`, `og:description`, `og:image`, `og:type="profile"`, `og:locale="es_ES"`.
- `<link rel="canonical">` (URL de ejemplo).
- HTML semántico y encabezados con palabras clave (guitarrista, flamenco, jazz, conciertos).
- Imágenes con nombres de archivo descriptivos y `width`/`height` declarados.

### 6.6 Schema.org (JSON-LD)

Bloque `<script type="application/ld+json">` en el `<head>`. Es un bloque de **datos**, no JavaScript ejecutable, así que respeta la restricción de "solo HTML y CSS".

- **`Person`** (el artista): `name`, `alternateName`, `jobTitle`, `description`, `image`, `url`, `email`, `sameAs` (redes), `address` (`PostalAddress`: Valencia, ES), `genre`.
- **`MusicEvent`** (uno por presentación): `name`, `startDate`, `eventStatus`, `eventAttendanceMode`, `location` (`Place` con `PostalAddress`), `performer` (referencia a la `Person`), `offers` (`Offer` con `url`).
- **`MusicAlbum`** (opcional): *Raíz de agua* y *Mareas del Sur*, con `byArtist`.

Validar en validator.schema.org.

### 6.7 Identidad visual

Estilo: nocturno y cálido, como un escenario iluminado.

| Variable | Color | Uso |
|----------|-------|-----|
| `--color-fondo` | `#14121F` | Fondo principal |
| `--color-fondo-alt` | `#1F1C2E` | Fondo de secciones alternas y tarjetas |
| `--color-texto` | `#F4EFE6` | Texto principal |
| `--color-texto-suave` | `#B9B3C7` | Texto secundario |
| `--color-acento` | `#E8A33D` | Enlaces, botones, detalles |

Contrastes calculados (WCAG): texto/fondo 16.1:1, texto suave/fondo-alt 8.2:1, acento/fondo-alt 7.7:1. Todos superan AA (4.5:1).

Tipografía: una serif expresiva para títulos y una sans-serif legible para el texto (fuentes del sistema o Google Fonts vía `<link>`).

### 6.8 Criterios de evaluación

- [ ] HTML correctamente formateado.
- [ ] Etiquetas organizadas según su jerarquía.
- [ ] Uso estricto de HTML semántico.
- [ ] CSS con presentación atractiva y moderna.
- [ ] Organización correcta de archivos (HTML y CSS).
- [ ] Apto para lectores de pantalla (`aria-label`, `alt`, etc.).
- [ ] Datos estructurados de Schema.org que describen al artista o su obra.
- [ ] Cumple los requerimientos del artista (secciones, navegación, portada).

---

## 7. Restricciones

- Solo trabajar con **HTML y CSS**. No incorporar otras tecnologías como JS o frameworks.
- Cumplir al menos con **WCAG 2.1 nivel AA** de accesibilidad.
- Debe ser **HTML semántico**.
- Una sola página (landing page). Cada sección ocupa aproximadamente el alto de una pantalla.
- Las animaciones son opcionales y solo con CSS.
