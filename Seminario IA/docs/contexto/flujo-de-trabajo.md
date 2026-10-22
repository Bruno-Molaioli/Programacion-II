# Flujo de Trabajo y Definition of Done (DoD)

## 1. Pasos para Realizar un Cambio de Maquetado
1. **Inspección Previa:** Revisar [convenciones.md](file:///c:/Antigravity/docs/contexto/convenciones.md) y [arquitectura.md](file:///c:/Antigravity/docs/contexto/arquitectura.md) para respetar los tokens CSS y la semántica.
2. **Evaluación de Impacto:**
   - Si es un ajuste puntual en `index.html`: aplicar **Fast-Path** directo asegurando el DoD.
   - Si implica cambios estructurales, nuevos archivos o frameworks: solicitar confirmación explícita previa y registrar en [decisiones.md](file:///c:/Antigravity/docs/contexto/decisiones.md).
3. **Edición de Código:** Mantener HTML5 semántico y CSS modular sin estilos en línea.
4. **Verificación Local:** Comprobar en navegador de escritorio y emulador móvil (F12).

---

## 2. Checklist de "Terminado" (Definition of Done)
Antes de marcar una tarea como completada, debe cumplirse incondicionalmente:

- [ ] **HTML Válido y Semántico:** Empleo de etiquetas semánticas (`<article>`, `<header>`, `<button>`, etc.) y atributos `alt` en imágenes.
- [ ] **4 Estados UI Considerados:**
  - *Loading:* Imágenes con dimensiones explícitas para evitar saltos de pantalla (CLS).
  - *Empty:* Tratamiento de contenido en caso de ausencia de datos.
  - *Error:* Contraste y visibilidad verificados.
  - *Success:* Renderizado consistente y transiciones visuales pulidas.
- [ ] **Código Limpio:** Ausencia de estilos inline (`style="..."`), sin console logs residuales ni código muerto.
- [ ] **Actualización de Contexto:** Registrar la decisión correspondiente en `decisiones.md`.

---

## 3. Validación Responsive
- Probar en resolución móvil angosta (360px a 414px) para descartar scroll horizontal (`overflow-x`).
- Verificar que el tamaño de los botones táctiles alcance un mínimo ergonómico de 44px de altura.
- Confirmar fluidez de animaciones hover en pantallas de escritorio con cursor de ratón.
