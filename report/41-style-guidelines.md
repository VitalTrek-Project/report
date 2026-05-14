## Capítulo IV: Product Design
### 4.1. Style Guidelines
#### 4.1.1. General Style Guidelines

**Branding**

VitalTrek es una plataforma IoT orientada al turismo de aventura extrema en Perú y América Latina. La identidad visual del producto refleja dos valores centrales que coexisten: **seguridad** y **aventura**. El sistema visual comunica confianza tecnológica a través de una paleta oscura y estructurada, mientras que el acento naranja aporta energía, dinamismo y llamada a la acción. El resultado es una marca que transmite seriedad operativa sin perder el espíritu explorador de su audiencia.

El logotipo se presenta siempre acompañado del nombre **VitalTrek** en peso bold, con un espaciado de tracking negativo (-0.3px) para mayor cohesión. El ícono nunca se usa de forma aislada en contextos de navegación. La proporción mínima del logo es 32px de alto para garantizar legibilidad en pantallas pequeñas.

---

**Tone of Communication**

El tono de VitalTrek se posiciona en los siguientes ejes:

| Eje | Posición |
|---|---|
| Divertido / Serio | **Serio con energía** — el producto gestiona situaciones de riesgo real, por lo que el tono es directo y profesional, pero no frío. |
| Formal / Casual | **Semi-casual** — se tutea al usuario, se usan frases cortas y activas. Se evita el lenguaje técnico innecesario. |
| Respetuoso / Irreverente | **Respetuoso** — la seguridad del turista es el eje central; el tono nunca minimiza riesgos ni usa humor inapropiado. |
| Entusiasta / Sereno | **Entusiasta** — los CTAs y encabezados usan lenguaje de acción ("Explore more", "Worry less", "Manage all your tours"). |

El idioma por defecto de la interfaz es **inglés (en_US)**. Se soporta **español latinoamericano (es_419)** como idioma alternativo mediante el sistema i18n implementado en el producto.

---

**Colors**

La paleta de colores de VitalTrek está organizada en cuatro categorías funcionales: superficies, accentos, texto y bordes. Todos los valores están definidos como CSS Custom Properties en el archivo `style.css` del producto, garantizando consistencia y mantenibilidad.

![Color Palette](../assets/images/vitaltrek-paleta1.png)

![Color Palette](../assets/images/vitaltrek-paleta2.png)

---

**Typography**

VitalTrek usa un sistema tipográfico de dos familias con roles claramente diferenciados.

**Fuentes**

| Familia | Peso(s) | Rol |
|---|---|---|
| **Playfair Display** | 700, 800 (regular e italic) | Headings principales (h1, h2, h3), precios |
| **DM Sans** | 300, 400, 500, 600 | Cuerpo de texto, labels, botones, navegación |


**Escala tipográfica**

| Elemento | Familia | Tamaño | Peso | Uso |
|---|---|---|---|---|
| H1 Hero | Playfair Display | `clamp(40px, 5vw, 66px)` | 700 | Titular principal de la landing |
| H2 Secciones | Playfair Display | `clamp(26px, 3vw, 48px)` | 700 | Encabezados de cada sección |
| H3 Cards | DM Sans | `15–24px` | 600–700 | Títulos de plan cards y about cards |
| H4 Features | DM Sans | `14px` | 600 | Títulos de feature cards |
| Body | DM Sans | `15–16px` | 400 | Descripciones de sección |
| Body small | DM Sans | `13–14px` | 400 | Texto de cards y listas |
| Label | DM Sans | `11–12px` | 700 | Section tags, plan tiers |
| Button | DM Sans | `14px` | 600 | Todos los botones |
| Caption | DM Sans | `12px` | 400 | Footer, notas de precio |

**Principios tipográficos**

- **Jerarquía serif/sans**: los headings en Playfair Display establecen un contraste editorial con el cuerpo en DM Sans, creando ritmo visual en cada sección.
- **Line height**: `1.6` para cuerpo de texto, `1.10–1.20` para headings, `1.75` para párrafos descriptivos.
- **Letter spacing**: `0.14em` en section tags (uppercase), `-0.3px` en el nombre del logo.
- **Responsive type**: los headings principales usan `clamp()` para escalar fluidamente entre breakpoints sin media queries adicionales.

---

**Spacing**

El sistema de espaciado de VitalTrek sigue una escala consistente basada en múltiplos de 4px. Los valores más usados son:

| Valor | Uso principal |
|---|---|
| `4px` | Gap entre elementos inline (lang toggle, nav actions) |
| `7–10px` | Gap interno en listas de features |
| `14px` | Gap entre cards en grids |
| `16px` | Padding de elementos compactos (section tags, badges) |
| `22–24px` | Padding interno de cards |
| `28–36px` | Padding de cards grandes (plan cards, eco cards) |
| `48px` | Padding horizontal de secciones en desktop |
| `64–80px` | Padding vertical inferior de secciones |
| `96px` | Padding vertical estándar de secciones en desktop |

**Border Radius**

| Token | Valor | Uso |
|---|---|---|
| `--radius-button` | `8px` | Botones (btn-primary, btn-join, btn-plan) |
| `--radius-card` | `14px` | Feature cards, stat cards, about cards |
| `--radius-section` | `20px` | Eco cards, plan cards, testi cards, modal |
| `--radius-hero` | `28px` | Hero image wrap |

**Shadows**

| Token | Valor | Uso |
|---|---|---|
| `--shadow-elevation-high` | `0 12px 40px rgba(0,0,0,0.28)` | Hero image, modal |
| `--shadow-card` | `0 4px 20px rgba(0,0,0,0.12)` | Feature cards en sección Tourists |
| `--shadow-elevation-low` | `0 2px 10px rgba(0,0,0,0.08)` | Testimonial cards |

---

#### 4.1.2. Web Style Guidelines

**Layout y Grid System**

VitalTrek usa CSS Grid como sistema de layout principal. Cada sección de la landing page sigue un grid de dos columnas en desktop que colapsa a una columna en mobile.

| Sección | Grid desktop | Grid mobile |
|---|---|---|
| Hero | `1fr 1fr` | `1fr` |
| Problem | `1fr 1fr` | `1fr` |
| Tourists | `1fr 1fr` | `1fr` |
| Agencies | `1fr 1fr` | `1fr` |
| Ecosystem | `repeat(4, 1fr)` | `1fr` |
| Plans | `repeat(3, 1fr)` | `1fr` |
| Testimonials | `repeat(3, 1fr)` | `1fr` |
| About cards | `repeat(3, 1fr)` | `1fr 1fr` |
| Team | `repeat(5, 1fr)` | `repeat(2, 1fr)` |
| Footer | `1.6fr 1fr 1fr 1fr` | `1fr` |

El ancho máximo de contenido se limita a `1060–1100px` en las secciones con `max-width` explícito (Ecosystem, Plans, Testimonials, Team).

---

**Navbar**

La barra de navegación es **fixed** en la parte superior, con altura fija de `var(--height-navbar) = 66px` y `z-index: 1000`. Estructura:

- **Izquierda**: logo + nombre de marca.
- **Centro**: links de navegación con hover state (background sutil + color blanco).
- **Derecha**: language toggle pill, hamburger (mobile), botón Join (CTA).

En mobile (≤ 900px), los links colapsan a un dropdown vertical que se activa con el hamburger, el cual anima a una X al abrirse. El estado del menú se gestiona con `aria-expanded` para accesibilidad.

---

**Buttons**

VitalTrek define cuatro variantes de botón con usos específicos:

| Clase | Apariencia | Uso |
|---|---|---|
| `.btn-primary` | Fondo naranja, texto blanco | CTA principal en Hero |
| `.btn-outline` | Borde blanco translúcido, texto blanco | CTA secundario en Hero |
| `.btn-join` | Fondo naranja, texto blanco, compacto | CTA en navbar |
| `.btn-plan` | Fondo translúcido blanco o naranja | CTA en plan cards |

Todos los botones tienen `transition` de `0.15–0.2s` en hover, con `transform: translateY(-1px)` o `(-2px)` para dar feedback táctil visual. El radio de borde es siempre `var(--radius-button) = 8px`.

El estado `:focus-visible` expone un outline naranja de `2px` con `outline-offset: 3px` en todos los elementos interactivos para accesibilidad de teclado.

---

**Cards**

Las cards siguen tres arquetipos visuales según el contexto de uso:

***Cards sobre fondo claro (Feature cards, Testimonial cards)***
- Fondo blanco `#fff`.
- Borde `1px solid var(--color-border-default)`.
- `box-shadow: var(--shadow-card)`.
- `border-radius: var(--radius-card)` (14px).
- Hover: `transform: translateY(-3px)` + sombra elevada.

***Cards sobre fondo oscuro (About cards, Team cards, Stat cards)***
- Fondo `var(--color-surface-card-dark)` (`#364257`).
- Borde `1px solid var(--color-border-inverse)`.
- Sin sombra.
- Hover: `transform: translateY(-3px)` o `(-4px)`.

***Cards de agencia (Agency feature cards)***
- Fondo `rgba(255,255,255,0.10)` con `backdrop-filter: blur(8px)`.
- Borde `1px solid rgba(255,255,255,0.15)`.
- Hover: aumenta opacidad del fondo a `0.16`.

---

**Section Tags**

Los labels de sección (`<span class="section-tag">`) usan:
- Color `var(--color-accent-primary)` — naranja.
- `font-size: 11px`, `font-weight: 700`, `letter-spacing: 0.14em`.
- `text-transform: uppercase`.
- Se colocan siempre encima del `<h2>` correspondiente con `margin-bottom: 16px`.

---

**Modal — Join Dialog**

El modal de acceso sigue el patrón **dialog accesible** con `role="dialog"`, `aria-modal="true"`, `aria-labelledby` y `aria-describedby`. Se activa desde el botón Join en la navbar.

- Overlay: `background: rgba(0,0,0,0.55)`, `z-index: 2000`.
- Card: fondo `var(--color-surface-lighter)`, `border-radius: var(--radius-section)` (20px), `max-width: 520px`.
- Botón primario: `var(--color-accent-primary)` naranja relleno.
- Botón secundario: `var(--color-surface-nav)` navy outlined.
- Cierre: botón X en esquina superior derecha, click en overlay, tecla `Escape`.
- Focus management: al abrir, el foco se mueve al botón de cierre; al cerrar, regresa al botón Join.
- i18n: todos los textos del modal responden al toggle de idioma EN/ES.

---

**Responsive Breakpoints**

VitalTrek define tres breakpoints en el CSS:

| Breakpoint | Valor | Descripción |
|---|---|---|
| Tablet | `max-width: 1024px` | Reduce grids de 4 columnas a 2, ajusta footer |
| Mobile | `max-width: 900px` | Navbar colapsa, secciones de 2 columnas a 1 |
| Mobile small | `max-width: 600px` | Reducción agresiva de padding, grids de 1 columna |

En mobile (≤ 900px):
- El padding horizontal de secciones pasa de `48px` a `24px`.
- El padding vertical de secciones pasa de `96px` a `80px`.
- Los botones Hero ocupan el 100% del ancho (`width: 100%`).
- El plans toggle ocupa el 100% del ancho.

En mobile small (≤ 600px):
- El padding horizontal se reduce a `18px`.
- El padding vertical a `64px`.
- Stats grid, features grid, agency grid y eco grid colapsan a `1fr`.
- El footer grid colapsa a `1fr` en columna única.

---

**Accessibility (a11y)**

VitalTrek implementa los siguientes estándares de accesibilidad en la web:

- **ARIA landmarks**: `role="navigation"` en navbar, `role="contentinfo"` en footer, `role="dialog"` en modal, `role="tablist"` y `role="tabpanel"` en el toggle de planes.
- **aria-labelledby**: cada `<section>` referencia su `<h2>` correspondiente por ID.
- **aria-live**: región `role="status"` anuncia cambios de idioma a screen readers.
- **aria-selected**: los botones de tab de planes actualizan `aria-selected="true/false"` dinámicamente.
- **aria-expanded**: el botón hamburger reporta el estado del menú mobile.
- **aria-hidden**: todos los SVGs decorativos están marcados como `aria-hidden="true"`.
- **focus-visible**: outline naranja de 2px en todos los elementos interactivos para navegación por teclado.
- **Semántica HTML**: se usan `<nav>`, `<section>`, `<footer>`, `<address>`, `<figure>`, `<blockquote>`, `<figcaption>` según su propósito semántico.
- **Textos alternativos**: todas las imágenes tienen `alt` descriptivo; las decorativas tienen `alt=""`.

---

**Internationalization (i18n)**

La interfaz web soporta dos locales:

| Locale | Código | Idioma por defecto |
|---|---|---|
| English | `en-US` | Sí |
| Latin American Spanish | `es-419` | No |

El sistema i18n se implementa mediante atributos `data-i18n` en el HTML y un objeto `translations` en `main.js`. La función `toggleLanguage()` actualiza `document.documentElement.lang`, todos los elementos `[data-i18n]`, el pill del botón de idioma y anuncia el cambio mediante `aria-live`. El modal de Join también responde al toggle de idioma. El idioma predeterminado al cargar la página es inglés, conforme al statement del proyecto.