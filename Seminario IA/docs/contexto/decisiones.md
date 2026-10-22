# Registro de Decisiones de Arquitectura (ADR)

> [!CAUTION]
> **CONTROL DE GUARDAS (AUTORIZACIÓN EXPLÍCITA OBLIGATORIA):**
> Antes de ejecutar cualquier cambio importante o estructural (cambio de arquitectura, reemplazo o adición de frameworks CSS/JS, eliminación de librerías o borrado de archivos), **DEBES pedir autorización explícita al usuario** explicando el impacto técnico previo a su ejecución.

---

### [ADR-001] · [2026-09-07 13:47] Componente Tarjeta de Presentación en HTML5 y CSS Puro
- **Estado:** Implementado en `index.html`
- **Contexto:** Se solicitó una tarjeta de perfil moderna con tema oscuro, gradiente violeta y botón hover.
- **Decisión:** Implementar usando HTML5 semántico y CSS puro con variables en `:root`, sin frameworks externos.

---

### [ADR-002] · [2026-09-07 13:49] Diagnóstico de Entorno de Desarrollo Windows
- **Estado:** Completado
- **Contexto:** Comprobación del estado de Node.js, Git, npm y políticas de PowerShell.
- **Decisión:** Se validó Git v2.54, Node v24.19, npm v11.17 y `ExecutionPolicy: Unrestricted` en `CurrentUser`.

---

### [ADR-003] · [2026-09-07 13:52] Instalación del Sistema Operativo de Reglas Antigravity
- **Estado:** Activo y Permanente
- **Contexto:** Establecimiento de los 6 pilares maestros de desarrollo y gobernanza de código.
- **Decisión:** Crear `.agents/rules/antigravity_global_rules.md` con trigger `always_on` y enlazarlo en `GEMINI.md`.

---

### [ADR-004] · [2026-09-07 13:55] Definición de Especificaciones de "Classic Bar"
- **Estado:** Especificado (Pendiente de implementación en código)
- **Contexto:** Respuestas a las 14 preguntas pedagógicas para una carta de bar con dos vistas (Productos/Puntuación).
- **Decisión:** Registrar el diseño funcional propuesto para su futura incorporación.

---

### [ADR-005] · [2026-09-07 13:57] Creación de Base de Conocimiento SDD
- **Estado:** Completado
- **Contexto:** Adopción de la metodología Spec-Driven Development de Gentle AI.
- **Decisión:** Crear los 6 documentos de contexto en `docs/contexto/` y vincularlos formalmente en `GEMINI.md`.

---

### [ADR-006] · [2026-09-07 13:58] Auditoría Estricta y Alineación con Código Existente
- **Estado:** Activo
- **Contexto:** Exigencia de documentar estrictamente lo que existe en el repositorio sin invocar elementos no implementados.
- **Decisión:** Sincronizar `docs/contexto/` con el código real de `index.html` (CSS Vanilla, sin frameworks enlazados).

---

### [ADR-007] · [2026-09-07 14:02] Importación de Biblioteca de Skills en .agents/skills/
- **Estado:** Completado
- **Contexto:** Incorporación del ecosistema de habilidades agénticas para potenciar capacidades de maquetado, testing, arquitectura y UX.
- **Decisión:** Clonar el repositorio `https://github.com/sickn33/agentic-awesome-skills` dentro de `.agents/skills/` (2.023 paquetes de skills especializadas).
- **Consecuencias:** Disponibilidad de un catálogo estructurado de skills accesibles localmente para el agente.

---

### [ADR-008] · [2026-09-07 14:05] Poda Inteligente de Skills en .agents/skills/
- **Estado:** Completado
- **Contexto:** Evaluación frente a `docs/contexto/` (arquitectura HTML5/Tailwind, sin frameworks JS pesados, sin backend ni bases de datos) y la metodología SDD de Gentle AI.
- **Decisión:** Podar 1.971 carpetas de skills superfluas (tecnologías prohibidas como React, Vue, Python, Docker, SQL, AWS, mobile nativo) y conservar exactamente 44 skills de alto valor centradas en maquetado Tailwind/CSS, accesibilidad a11y/WCAG, dinamismo de UI y metodología SDD/DoD.
- **Consecuencias:** Directorio `.agents/skills/` ligero, libre de ruido y 100% alineado con el stack del proyecto.

---

### [ADR-009] · [2026-09-07 14:12] Implementación de SPA con 3 Secciones, Modales Interactivos y Reporte SDD
- **Estado:** Completado
- **Contexto:** Definición final de los requisitos de la aplicación web: 3 secciones en archivo único sin recarga (Inicio, Catálogo, Formulario de Contacto/Puntuación), modales para detalles de cócteles, menú hamburguesa en celulares, conmutador de modo claro/oscuro con `.force-text-white` y generación de `REPORTE_VERIFICACION_SDD.md`.
- **Decisión:** Maquetar la solución integral en `index.html` con TailwindCSS v3 CDN y Vanilla JS estructurado, verificando los 4 estados UI y emitiendo el reporte formal de conformidad SDD.
- **Consecuencias:** Cumplimiento total del alcance pedagógico y los 6 pilares maestros de Antigravity OS.

---

### [ADR-010] · [2026-09-07 22:00] Empaquetado y Generación de ZIP con los 4 Entregables
- **Estado:** Completado
- **Contexto:** Consolidación final de los 4 entregables obligatorios del equipo (Sitio funcional, Contexto vivo, Memoria Engram y Reporte de verificación SDD).
- **Decisión:** Generar el archivo comprimido `ClassicBar_Entregable_Final.zip` (0.71 MB) conteniendo `index.html`, `docs/contexto/` (6 archivos), `GEMINI.md`, `ENGRAM_MEMORIA.md`, `REPORTE_VERIFICACION_SDD.md`, `README.md` y `.agents/` depurado.
- **Consecuencias:** Paquete de entrega autónomo, ligero y listo para distribución y evaluación.

---

### [ADR-011] · [2026-09-07 22:15] Creación del Paquete Oficial "Desafio Integrador.zip"
- **Estado:** Completado
- **Contexto:** Solicitud del usuario de generar un paquete ZIP con todo el contenido de `Programacion 2` bajo la denominación oficial "Desafio Integrador".
- **Decisión:** Comprimir los contenidos de `Programacion 2` (incluyendo `index.html`, `Video - Classic Bar.mp4`, `docs/contexto/`, `README.md`, `GEMINI.md`, `REPORTE_VERIFICACION_SDD.md`, `ENGRAM_MEMORIA.md` y `.agents/`) en `Desafio Integrador.zip` (37.58 MB).
- **Consecuencias:** Entrega consolidada con la demostración en video y la solución web integral lista para entrega académica.
