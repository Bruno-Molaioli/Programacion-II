# Errores Conocidos y Gotchas Técnicos

## 1. Gotchas de CSS / HTML Detectados en el Código

- **Compatibilidad con `backdrop-filter`:**
  - *Gotcha:* En navegadores basados en WebKit (Safari anterior a macOS Sonoma o iOS), `backdrop-filter: blur(...)` no funciona sin prefijo.
  - *Solución en código:* Se declara siempre con duplicado `-webkit-backdrop-filter: blur(16px);` antes de la propiedad estándar.

- **Texto con Gradiente (`background-clip: text`):**
  - *Gotcha:* La clase `.profile-role` utiliza degradado de texto. Si se omite `-webkit-text-fill-color: transparent`, el texto se pinta del color por defecto y tapa el degradado.
  - *Solución en código:* Mantener ambos: `-webkit-background-clip: text;` y `-webkit-text-fill-color: transparent;`.

- **Desbordamiento por Pseudo-Elementos Animados:**
  - *Gotcha:* En `.btn-primary::before`, la animación mueve el brillo de `left: -100%` a `left: 100%`. Si el botón carece de `overflow: hidden`, el elemento desborda la tarjeta.
  - *Solución en código:* El botón define estrictamente `overflow: hidden;`.

- **Preservación de Foco Accesible:**
  - *Gotcha:* Al remover contornos por defecto, los usuarios de teclado pierden visibilidad del elemento enfocado.
  - *Solución en código:* Se aplica regla explícita `:focus-visible { outline: 2px solid #c084fc; outline-offset: 3px; }`.

---

## 2. Compatibilidad de Navegadores y Ajustes de Windows

- **Codificación de Archivos:** Guardar siempre archivos en `UTF-8 sin BOM` para evitar caracteres corruptos al renderizar o ejecutar scripts en PowerShell.
- **Ejecución de Scripts en PowerShell:** Requiere política `Unrestricted` o `RemoteSigned` en `CurrentUser` para correr scripts `.ps1` de verificación y herramientas CLI.
- **Normalización de Separadores de Ruta:** En Windows usar diagonales hacia adelante `/` en enlaces Markdown `file:///c:/...` para compatibilidad en navegadores y editores.
