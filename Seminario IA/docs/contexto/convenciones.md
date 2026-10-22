# Convenciones de Desarrollo y Diseño - Classic Bar

## 1. Semántica HTML5
- Uso estricto de elementos estructurados según su rol W3C:
  - `<header>`: Barra de navegación superior fija (*sticky*).
  - `<nav>`: Contenedor de enlaces de navegación principal y móvil.
  - `<main>`: Contenedor global de las 3 secciones SPA (`#sec-inicio`, `#sec-catalogo`, `#sec-formulario`).
  - `<section>`: Delimitador de cada una de las 3 vistas principales.
  - `<article>`: Para cada tarjeta de cóctel dentro de la grilla.
  - `<figure>` e `<img>`: Para fotografías con `loading="lazy"`, dimensiones y `alt` descriptivo.
  - `<dialog>` o contenedor modal con `role="dialog"`, `aria-modal="true"` y `aria-labelledby`.
  - `<button type="button">`: Para todos los disparadores interactivos (hamburguesa, modal, filtros, botón de tema, envío).

## 2. Paleta de Colores y Tokens CSS

### Modo Nocturno (Predeterminado - Elegante & Cálido)
- **Fondo Principal (`bordo-dark`):** `#3A0D16` (Bordó oscuro profundo)
- **Superficie de Tarjetas (`marron-dark`):** `#241417` (Marrón café tostado)
- **Texto Primario (`crema-light`):** `#F3E6D0` (Crema marfil cálido)
- **Texto Secundario (`beige-soft`):** `#D8C3A5` (Beige arena)
- **Color de Acento & Precios (`dorado-gold`):** `#C9A24D` (Dorado vintage)
- **Bordes:** `rgba(201, 162, 77, 0.2)` (Dorado translúcido)
- **Confirmación / Éxito:** `#10B981` (Verde esmeralda para estado "Enviado")

### Modo Claro (Limpio & Sofisticado)
- **Fondo Principal:** `#FAF6F0` (Crema marfil suave)
- **Superficie de Tarjetas:** `#FFFFFF` (Blanco con sombra sutil)
- **Texto Principal:** `#241417` (Marrón café intenso)
- **Texto Secundario:** `#5C3A41` (Bordó atenuado)
- **Color de Acento:** `#9E7B27` (Oro viejo de alto contraste)

### Utilidad de Contraste Protegido: `.force-text-white`
- La clase `.force-text-white` asegura que textos situados sobre fondos oscuros, banners o botones con gradientes permanezcan en blanco puro (`#FFFFFF`) independientemente del tema activo (Modo Claro u Oscuro), garantizando ratio de contraste > 7:1 (WCAG AAA).

## 3. Tipografía Oficial
- **Familia:** `Poppins`, sans-serif (Google Fonts: 400, 500, 600, 700).
- **Fallback:** `system-ui, -apple-system, sans-serif`.

## 4. Diseño Responsive y Ergonomía Táctil
- **Móviles (< 768px):**
  - Menú hamburguesa táctil con drawer desplegable animado.
  - Grilla de cócteles en **2 columnas horizontales** (`grid-cols-2 gap-3`) para fácil navegación con pulgar.
  - Áreas táctiles con altura mínima de 44px.
- **Escritorio (>= 768px):**
  - Barra de navegación horizontal centrada con indicador de sección activa.
  - Grilla de 6 tarjetas distribuidas en **3 columnas x 2 filas** (`md:grid-cols-3 gap-6`).
