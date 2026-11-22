# Documento de Especificaciones Técnicas y Handoff de Diseño: Agent-Hub

**Proyecto:** Agent-Hub — Autonomous Operations Console  
**Versión:** 1.0.0 (Production Hand-off)  
**Entorno de destino:** Desktop Web (Resolución base: 1440px / 1920px responsive)  
**Diseño de referencia:** {{DATA:DESIGN_SYSTEM:DESIGN_SYSTEM_1}} & {{DATA:SCREEN:SCREEN_9}}  

---

## 1. Resumen Arquitectónico del Sistema

Agent-Hub es una consola web de operaciones y supervisión para clústeres de agentes autónomos de IA y telemetría de inferencia. La interfaz está construida como un panel modular con navegación unificada (Shell) y conmutación reactiva entre **Modo Oscuro** (predeterminado) y **Modo Claro**.

### Pantallas del Ecosistema (Suite Completa)
1. **Dashboard** (`/` o `/dashboard`): Métricas de clúster, actividad semanal cómputo vs. SLA, telemetría GPU/LLM y feed de actividad en tiempo real.
2. **Gestión de usuarios** (`/usuarios`): Directorio IAM, roles, asignación de cuota de cómputo y auditoría de políticas de seguridad.
3. **Gestión de agentes** (`/agentes`): Monitor de inferencia, catálogo colapsable de skills con micro-transiciones y etiquetas de estado de alto contraste.
4. **Skills** (`/skills`): Catálogo modular de capacidades WASM/Firecracker, filtros por categoría y telemetría de invocación.
5. **Contrataciones de agentes** (`/contrataciones`): Seguimiento de MRR, licencias activas, renovaciones y desglose de consumo por tenant empresarial.
6. **Log de errores** (`/logs`): Telemetría de fallos, códigos de error técnicos, filtros por severidad y acciones de triage.

---

## 2. Design Tokens y Sistema de Temas (Dark / Light)

El sistema utiliza CSS Custom Properties estructuradas bajo un esquema de tokens semánticos con soporte para cambio instantáneo de tema mediante la clase `.light-mode` o el atributo `data-theme="light"` en el elemento raíz `<html>` o `<body>`.

### 2.1 Paleta Cromática y Tokens Semánticos

| Token Semántico | Modo Oscuro (Base) | Modo Claro | Uso UI |
|---|---|---|---|
| `--color-surface` | `#0b1326` | `#f8fafc` | Fondo de lienzo de la aplicación |
| `--color-surface-container` | `#131b2e` | `#ffffff` | Tarjetas, modales, contenedores |
| `--color-surface-container-high` | `#1a243b` | `#f1f5f9` | Elementos hover, tablas, filas alternas |
| `--color-border-subtle` | `rgba(255, 255, 255, 0.08)` | `#e2e8f0` | Divisores, bordes de tarjeta |
| `--color-border-active` | `rgba(99, 102, 241, 0.4)` | `#cbd5e1` | Bordes en foco o seleccionados |
| `--color-text-primary` | `#f8fafc` | `#0f172a` | Encabezados H1-H4, textos destacados |
| `--color-text-secondary` | `#94a3b8` | `#475569` | Descripciones, labels técnicos, placeholders |
| `--color-text-muted` | `#64748b` | `#94a3b8` | Timestamps, metadatos terciarios |
| `--color-brand-primary` | `#6366f1` | `#4f46e5` | Botones de acción, enlaces activos, acentos |
| `--color-brand-primary-hover` | `#4f46e5` | `#4338ca` | Estado hover de acciones primarias |

### 2.2 Tokens Semánticos de Estado (Badges y Semáforos)
*Optimizados para cumplir ratio de contraste WCAG AA / AAA:*

- **Estado ACTIVO / NOMINAL (Verde)**
  - *Dark:* Fondo `rgba(16, 185, 129, 0.15)`, Texto `#34d399`, Borde `rgba(16, 185, 129, 0.3)`
  - *Light:* Fondo `#ecfdf5`, Texto `#166534` (`emerald-800`), Borde `#a7f3d0`
- **Estado FALLANDO / CRÍTICO (Rojo)**
  - *Dark:* Fondo `rgba(239, 68, 68, 0.15)`, Texto `#f87171`, Borde `rgba(239, 68, 68, 0.3)`
  - *Light:* Fondo `#fef2f2`, Texto `#991b1b` (`rose-800`), Borde `#fecaca`
- **Estado EN EJECUCIÓN / INFORMATIVO (Azul / Cian)**
  - *Dark:* Fondo `rgba(59, 130, 246, 0.15)`, Texto `#60a5fa`, Borde `rgba(59, 130, 246, 0.3)`
  - *Light:* Fondo `#eff6ff`, Texto `#1e40af`, Borde `#bfdbfe`
- **Estado INACTIVO / STAGING (Gris Pizarra)**
  - *Dark:* Fondo `rgba(148, 163, 184, 0.12)`, Texto `#cbd5e1`, Borde `rgba(148, 163, 184, 0.2)`
  - *Light:* Fondo `#f1f5f9`, Texto `#334155` (`slate-700`), Borde `#cbd5e1`

---

## 3. Tipografía y Escala de Espaciado

- **Fuente Principal:** `Space Grotesk`, sans-serif (para titulares, cifras métricas y navegación)
- **Fuente Secundaria / Monospace:** `JetBrains Mono` o `ui-monospace` (para IDs de agente, hashes, timestamps UTC y códigos de error)
- **Escala de Texto:**
  - H1 (Títulos de página): `24px` / `1.2` (Font Weight: 700)
  - H2 / Subtítulos de sección: `18px` / `1.3` (Font Weight: 600)
  - Métricas / KPI Numbers: `28px` - `32px` / `1.1` (Font Weight: 700)
  - Body Text: `14px` / `1.5` (Font Weight: 400 - 500)
  - Metadatos / Labels: `11px` - `12px` / `1.4` (Font Weight: 500 - 600, `uppercase`, tracking `0.05em`)
- **Sistema de Espaciado (Grid de 4px/8px):**
  - Padding contenedores estándar: `24px` (`p-6`)
  - Gaps de tarjetas métricas: `16px` o `20px` (`gap-4` / `gap-5`)
  - Separación entre secciones: `32px` (`mb-8`)

---

## 4. Estructura del Shell Persistente y Layout Global

### 4.1 Barra Lateral (Persistent Left Sidebar)
- **Ancho fijo:** `260px`
- **Posicionamiento:** `fixed` a la izquierda, altura `100vh`
- **Navegación Canónica (Orden Estricto):**
  1. `Dashboard` (`icon: layout-grid`)
  2. `Gestión de usuarios` (`icon: users`)
  3. `Gestión de agentes` (`icon: cpu-chip`)
  4. `Skills` (`icon: puzzle-piece` o `lightbulb`)
  5. `Contrataciones de agentes` (`icon: credit-card` o `handshake`)
  6. `Log de errores` (`icon: shield-alert` o `terminal`)
- **Pie de Sidebar:** Indicador de versión técnica (`v4.1.0-prod`) y semáforo de estado del clúster (`ONLINE`, verde pulso).

### 4.2 Cabecera Global (Top Navigation Bar)
- **Altura fija:** `64px`
- **Componentes:**
  - Input de búsqueda global contextual con shortcut (`Ctrl + K` / `Cmd + K`): `Buscar telemetría, agentes o identidades...`
  - Toggle de tema reactivo (`☀️ / 🌙`) con persistencia en `localStorage`.
  - Campana de notificaciones con badge de alertas no resueltas.
  - Perfil de usuario autenticado: `ADMIN ROOT (SecOps Admin)` con avatar circular.

---

## 5. Especificación de Componentes e Interacciones Clave

### 5.1 Gestión de Agentes: Despliegue de Skills Colapsable
- **Comportamiento:**
  - Por defecto, la lista de skills asociadas al agente se encuentra **colapsada**.
  - El botón disparador (`Skills (N) ▼`) conmuta el estado `aria-expanded="true|false"`.
  - La transición debe animar `max-height` (de `0` a `500px`), `opacity` (de `0` a `1`) y rotar el chevron `180deg` en `250ms cubic-bezier(0.4, 0, 0.2, 1)`.
- **Estructura del elemento:**
  - Chip con icono de habilidad, nombre de la skill, versión y botón de acción directa o configuración (`⚙`).

### 5.2 Botón de Tema (Theme Switcher Logic)
Para sincronizar el tema de forma global en producción sin saltos de flash (FOUC):
```javascript
// Theme Manager Script
const THEME_STORAGE_KEY = 'agenthub_theme';

function getPreferredTheme() {
  const storedTheme = localStorage.getItem(THEME_STORAGE_KEY);
  if (storedTheme) return storedTheme;
  return window.matchMedia('(prefers-color-scheme: light)').matches ? 'light' : 'dark';
}

function applyTheme(theme) {
  const root = document.documentElement;
  if (theme === 'light') {
    root.classList.add('light-mode');
    root.setAttribute('data-theme', 'light');
  } else {
    root.classList.remove('light-mode');
    root.setAttribute('data-theme', 'dark');
  }
  localStorage.setItem(THEME_STORAGE_KEY, theme);
  updateToggleIcon(theme);
}

function toggleTheme() {
  const currentTheme = document.documentElement.classList.contains('light-mode') ? 'light' : 'dark';
  applyTheme(currentTheme === 'light' ? 'dark' : 'light');
}
```

---

## 6. Recomendaciones de Integración Frontend (React / Vue / Tailwind)

1. **Framework CSS:** Tailwind CSS v3.x configurado con modo `class` (`darkMode: 'class'`).
2. **Iconografía:** Lucide React o Heroicons (v2 micro/outline).
3. **Gestión de Estados Globales:** 
   - Store para filtros de tablas (búsqueda, severidad, tipo de agente).
   - Estado de tema guardado en `localStorage` o cookie de sesión para SSR sin parpadeos.
4. **Accesibilidad (a11y):**
   - Ratios de contraste revisados superiores a `4.5:1` en texto normal y `3:1` en componentes UI.
   - Atributos `aria-expanded` y `aria-controls` en acordeones de skills y menús contextuales.
   - Navegación completa por teclado accesible en tablas y botones de acción.
