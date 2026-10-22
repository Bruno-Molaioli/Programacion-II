# Classic Bar - Proyecto Final

Aplicación web SPA (Single Page Application) moderna para la carta de coctelería y sistema de feedback interactivo de **Classic Bar** (Río Cuarto, Córdoba).

Desarrollada bajo la metodología **Spec-Driven Development (SDD)** de [Gentle AI](https://github.com/Gentleman-Programming/gentle-ai) y gobernada por el **Sistema Operativo de Reglas Antigravity**.

---

## 📦 Contenido del Paquete de Entrega
1. **`index.html`**: Aplicación web completa y funcional en un único archivo (HTML5 semántico + TailwindCSS v3 CDN + Vanilla JS).
   - 3 Secciones SPA: **Inicio (Hero)**, **Catálogo de Cócteles** y **Formulario de Contacto / Puntuación**.
   - Ventana modal interactiva de detalles de cada cóctel (receta, cristalería, graduación y notas).
   - Menú hamburguesa táctil para celulares (< 768px) y grilla de 2 columnas.
   - Alternador de **Modo Nocturno / Modo Claro** con persistencia en `localStorage`.
   - Formulario interactivo con botón verde de éxito (`#10B981`), tilde animado y cartel de confirmación.
2. **`docs/contexto/`**: Los 6 documentos de contexto vivo exigidos por la metodología SDD:
   - `arquitectura.md`, `convenciones.md`, `decisiones.md`, `glosario.md`, `flujo-de-trabajo.md`, `errores-conocidos.md`.
3. **`GEMINI.md`**: Vinculación de reglas globales y contexto vivo.
4. **`ENGRAM_MEMORIA.md`**: Historial consolidado de memoria continua y línea temporal de ADRs (ADR-001 a ADR-009).
5. **`REPORTE_VERIFICACION_SDD.md`**: Reporte formal de verificación empírica de los 4 estados UI (Loading, Empty, Error, Success) y Definition of Done (DoD).
6. **`.agents/`**:
   - `rules/antigravity_global_rules.md`: Los 6 pilares maestros de Antigravity OS.
   - `skills/`: Biblioteca podada de 44 habilidades especializadas en frontend, Tailwind, accesibilidad y SDD.

---

## 🚀 Cómo Ejecutar la Aplicación
No requiere instalación de dependencias, compilación ni servidores backend:
1. Abre directamente el archivo **`index.html`** en cualquier navegador moderno (Google Chrome, Microsoft Edge, Mozilla Firefox o Safari).
2. Para probar la vista móvil, presiona `F12` en el navegador y activa el emulador de dispositivos (375px a 414px).
