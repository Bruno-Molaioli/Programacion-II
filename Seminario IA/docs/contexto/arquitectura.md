# Arquitectura del Sistema - Classic Bar

## 1. Visión General del Producto
**Classic Bar** es una aplicación web interactiva desarrollada en un único archivo (`index.html`) estructurada como **SPA (Single Page Application)** sin recarga de página, bajo la metodología **SDD (Spec-Driven Development)** de [Gentle AI](https://github.com/Gentleman-Programming/gentle-ai). Ofrece una experiencia digital elegante, accesible y fluida para explorar la carta de cócteles, consultar recetas en ventanas modales y enviar calificaciones y notas de preparación.

## 2. Stack Técnico Oficial
- **Estructura:** HTML5 semántico nativo (cumplimiento estricto W3C y WCAG AA).
- **Estilos:** TailwindCSS v3 cargado mediante CDN oficial con extensión de paleta personalizada y diseño responsive mobile-first.
- **Tipografía:** Google Fonts (`Poppins`: 400, 500, 600, 700).
- **Lógica e Interactividad:** JavaScript Vanilla moderno (ES6+), modular, sin librerías externas ni transpiladores.
- **Arquitectura de Vistas:** SPA en archivo único `index.html` con enrutamiento ligero por DOM (`data-section`).

## 3. Mapa de Módulos de la Interfaz

```
[ index.html ]
 ├── 1. Navbar Sticky & Navegación
 │    ├── Isotipo Insignia ("CB") y Título ("Classic Bar")
 │    ├── Enlaces de Navegación Desktop ("Inicio", "Catálogo", "Puntuación & Contacto")
 │    ├── Conmutador de Modo Dual (Nocturno / Claro con icono Sol/Luna)
 │    └── Botón Hamburguesa Táctil & Drawer Desplegable para Móviles
 ├── 2. Sección 1: Inicio (Hero & Bienvenida)
 │    ├── Banner visual inmersivo con estética nocturna bordó/dorado
 │    ├── Propuesta de valor, horario y ambientación del bar
 │    └── Botones de Acción Primaria ("Explorar Carta") y Secundaria ("Calificar")
 ├── 3. Sección 2: Catálogo de Tarjetas (La Carta)
 │    ├── Selector de Píldoras de Filtro (Todos, Clásicos, 2x1, Sin Alcohol, Vinos)
 │    ├── Grilla Responsiva de Cócteles (6 tarjetas: 3 cols en escritorio / 2 cols en móviles)
 │    └── Tarjetas enriquecidas con imagen, zoom hover, precio dorado, tags y botón "Ver detalles"
 ├── 4. Componente Modal Interactivo (Drink Modal Dialog)
 │    ├── Ventana emergente con fondo oscurecido (backdrop-blur)
 │    ├── Ficha técnica ampliada del cóctel: cristalería, graduación, receta paso a paso
 │    ├── Botón de cierre accesible (X), cierre por tecla ESC y clic exterior
 │    └── Botón directo "Calificar este trago"
 └── 5. Sección 3: Formulario de Contacto & Puntuación
      ├── Selector / Buscador dinámico de trago
      ├── Selector interactivo de puntaje en escala del 1 al 10
      ├── Campo de sugerencias de preparación ("mucha coca", "mucho limón")
      ├── Botón con microinteracción a verde esmeralda ("¡Enviado!") + tilde animado
      └── Banner de confirmación visual verde de éxito
```

## 4. Tecnologías Prohibidas (Límites Técnicos del Proyecto)
- ⛔ **NO Frameworks JS:** Prohibido React, Vue, Angular, Svelte, Next.js, etc.
- ⛔ **NO Backend:** Prohibido Node/Express, Python, PHP o cualquier servidor externo.
- ⛔ **NO Bases de Datos:** Prohibido SQL, MongoDB, Firebase o Supabase.
- ⛔ **NO Estilos Inline:** Prohibido el uso de `style="..."` dentro de las etiquetas HTML; todo se gestiona con clases semánticas de TailwindCSS y estilos centralizados en `<style>`.
