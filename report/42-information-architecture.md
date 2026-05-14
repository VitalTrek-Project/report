### 4.2. Information Architecture

La arquitectura de información de VitalTrek está diseñada para servir a tres perfiles de usuario con necesidades distintas: el **turista aventurero**, el **administrador de agencia** y el **guía de tour**. Las decisiones de organización, etiquetado, navegación y búsqueda se orientan a reducir la carga cognitiva en contextos de uso exigentes — en campo, sin señal, bajo presión — garantizando que cada usuario encuentre lo que necesita sin esfuerzo y en el menor número de pasos posible.

---

#### 4.2.1. Organization Systems

**Organización visual del contenido**

***Jerarquía visual (Visual Hierarchy)***

Se aplica jerarquía visual en todas las secciones de la landing page y en las vistas principales de la aplicación web. El sistema tipográfico de dos familias (Playfair Display para headings, DM Sans para cuerpo) establece niveles de importancia claros: el título de sección comunica el tema central, el subtítulo contextualiza, y el cuerpo detalla. Los elementos de mayor jerarquía visual reciben mayor tamaño tipográfico, mayor contraste cromático y mayor espaciado superior. Este sistema se aplica consistentemente en Hero, Problem, Tourists, Agencies, Ecosystem y Plans.

En la aplicación web, la jerarquía visual se expresa mediante el tamaño y posición de los componentes: el estado activo de una expedición se muestra en la parte superior de la vista con métricas clave (progreso, alertas activas), mientras que el detalle histórico queda en un nivel inferior de la pantalla.

***Organización secuencial (Step-by-step)***

Se aplica organización secuencial en los siguientes contextos:

- **Landing page**: las secciones siguen una progresión narrativa — problema → solución por segmento → tecnología → planes → confianza — que guía al visitante desde la identificación del dolor hasta la conversión.
- **Flujo de registro**: el proceso de creación de cuenta sigue pasos ordenados (datos personales → verificación de correo → configuración de perfil) que el usuario debe completar en secuencia.
- **Creación de tour**: el formulario de creación de tour sigue una secuencia lógica (información general → checkpoints → asignación de turistas → publicación).
- **Inicio de expedición**: el guía sigue un flujo secuencial (verificar grupo → iniciar expedición → registrar checkpoints → finalizar) que refleja el proceso operativo real del recorrido.

***Organización matricial***

Se aplica organización matricial en las vistas de listado y comparación donde el usuario necesita evaluar múltiples elementos con los mismos atributos en paralelo:

- **Sección Plans de la landing page**: los tres planes de cada segmento se presentan en una grilla de tres columnas donde cada fila representa una categoría de features, permitiendo la comparación horizontal entre planes.
- **Dashboard de monitoreo**: el estado de cada turista se presenta en una cuadrícula donde las columnas representan métricas (ubicación, signos vitales, último checkpoint) y las filas representan participantes.
- **Lista de tours de la agencia**: los tours se muestran en formato de tabla o tarjeta donde cada elemento expone los mismos atributos (título, estado, fecha, capacidad) para facilitar la comparación.

**Esquemas de categorización del contenido**

***Por audiencia (grupos de usuarios)***

Es el esquema principal de VitalTrek. Tanto en la landing page como en la aplicación web, el contenido se segmenta según el rol del usuario:

- En la landing page, las secciones "For Adventurous Tourists" y "For the Tours Agencies" presentan beneficios diferenciados para cada segmento. El toggle de planes (Tourists / Agencies) es el ejemplo más explícito de esta categorización.
- En la aplicación web, el menú de navegación y las vistas disponibles varían según el rol autenticado: el administrador de agencia accede a Tour Management y Safety & Monitoring; el turista accede a Navigation & Exploration; el guía tiene acceso operativo a la expedición en curso.

***Por tópicos***

Se aplica dentro de cada módulo de la aplicación web para agrupar funcionalidades relacionadas:

- **Tour Management**: agrupa todo lo relacionado con el ciclo de vida del tour (crear, editar, duplicar, asignar, publicar).
- **Safety & Monitoring**: agrupa ubicaciones, signos vitales, alertas e incidentes bajo el tópico de seguridad operativa.
- **Notification & Profile**: agrupa las preferencias del usuario y el historial de comunicaciones.

***Cronológico***

Se aplica en vistas donde el tiempo es el criterio de relevancia más importante:

- **Historial de expediciones**: ordenado de más reciente a más antiguo.
- **Historial de notificaciones**: ordenado cronológicamente inverso, con las no leídas destacadas al inicio.
- **Registros de ubicación y telemetría**: los datos biométricos y de localización se presentan en orden cronológico para permitir la identificación de patrones a lo largo del recorrido.
- **Incidentes reportados**: ordenados por fecha de reporte, con posibilidad de reordenar por severidad.

---

#### 4.2.2. Labeling Systems

Las etiquetas de VitalTrek siguen el principio de mínimo número de palabras sin sacrificar claridad. Se prioriza el uso de términos del dominio de la aventura y el turismo para que los usuarios reconozcan las funciones sin necesidad de aprendizaje adicional.

**Etiquetas de navegación principal**

| Etiqueta EN | Etiqueta ES | Destino |
|---|---|---|
| Tourists | Turistas | Sección beneficios turistas |
| Agencies | Agencias | Sección beneficios agencias |
| Ecosystem | Ecosistema | Sección IoT |
| Plans | Planes | Sección precios |
| About us | Nosotros | Sección equipo |
| Join | Únete | Modal de acceso |

**Etiquetas de módulos de la aplicación**

| Etiqueta EN | Etiqueta ES | Módulo |
|---|---|---|
| My Tours | Mis Tours | Lista de tours del turista |
| Tour Catalog | Catálogo | Lista de tours de la agencia |
| Active Expedition | Expedición activa | Vista de expedición en curso |
| Live Monitoring | Monitoreo en vivo | Dashboard de seguridad |
| Alerts | Alertas | Lista de alertas activas |
| Incidents | Incidentes | Registro de incidentes |
| Profile | Perfil | Datos personales |
| Notifications | Notificaciones | Historial de notificaciones |

**Etiquetas de acciones principales**

| Etiqueta | Contexto |
|---|---|
| Create tour | Nuevo tour |
| Edit | Modificar tour existente |
| Duplicate | Copiar configuración de tour |
| Assign tourist | Agregar participante |
| Start expedition | Iniciar recorrido |
| Register checkpoint | Paso manual por checkpoint |
| Report incident | Nuevo incidente |
| Acknowledge | Confirmar recepción de alerta |
| Export report | Descargar reporte |
| Download route | Guardar ruta offline |
| Sign in | Acceso con cuenta existente |
| Create account | Registro nuevo usuario |

**Etiquetas de estados de entidades**

| Entidad | Estados |
|---|---|
| Tour | Draft · Available · Closed · Cancelled |
| Expedition | Scheduled · Active · Finished · Partially completed |
| Assignment | Pending · Confirmed · Cancelled |
| Alert | Active · Acknowledged · Dismissed |
| Incident | Reported · Acknowledged · Resolved |
| Account | Pending verification · Active · Inactive |

---

#### 4.2.3. SEO Tags and Meta Tags

**Landing Page (index.html)**

```html
<title>VitalTrek — Explore more. Worry less.</title>

<meta name="description"
  content="VitalTrek is an IoT platform for extreme adventure tourism in Peru.
  Monitor location, vital signs, and route progress in real time,
  even without a signal.">

<meta name="keywords"
  content="VitalTrek, adventure tourism Peru, IoT trekking, wearable monitoring,
  tour agency platform, GPS tracking trekking, smartwatch hiking,
  turismo aventura Peru, plataforma agencias tours, NexumDevs">

<meta name="author" content="NexumDevs — UPC 2026">

<meta property="og:title"        content="VitalTrek — Explore more. Worry less.">
<meta property="og:description"  content="IoT platform for extreme adventure tourism in Peru.
  Real-time monitoring of location, vital signs and route progress.">
<meta property="og:type"         content="website">
<meta property="og:locale"       content="en_US">
<meta property="og:locale:alternate" content="es_419">
```

**Web Application — Login / Register**

```html
<title>Sign in — VitalTrek</title>

<meta name="description"
  content="Sign in to your VitalTrek account to manage tours,
  monitor expeditions and access your adventure history.">

<meta name="keywords"
  content="VitalTrek login, VitalTrek sign in, adventure tour management,
  IoT expedition platform">

<meta name="author"  content="NexumDevs — UPC 2026">
<meta name="robots" content="noindex, nofollow">
```

**Web Application — Tour Catalog (Agency)**

```html
<title>Tour Catalog — VitalTrek</title>

<meta name="description"
  content="Manage your agency's tour catalog. Create, edit, publish and assign
  tourists to each tour from the VitalTrek dashboard.">

<meta name="keywords"
  content="tour management, agency dashboard, tour catalog, assign tourists,
  VitalTrek agency, adventure tours Peru">

<meta name="author"  content="NexumDevs — UPC 2026">
<meta name="robots" content="noindex, nofollow">
```

**Web Application — Live Monitoring**

```html
<title>Live Monitoring — VitalTrek</title>

<meta name="description"
  content="Real-time monitoring dashboard. Track tourist locations,
  vital signs and receive automatic alerts during active expeditions.">

<meta name="keywords"
  content="live monitoring, IoT expedition tracking, tourist safety,
  vital signs dashboard, VitalTrek monitoring">

<meta name="author"  content="NexumDevs — UPC 2026">
<meta name="robots" content="noindex, nofollow">
```

**Web Application — Active Expedition (Tourist)**

```html
<title>Active Expedition — VitalTrek</title>

<meta name="description"
  content="Navigate your current expedition with offline maps, checkpoint tracking
  and real-time health monitoring provided by VitalTrek.">

<meta name="keywords"
  content="offline navigation, expedition tracking, checkpoint progress,
  trekking app, VitalTrek tourist">

<meta name="author"  content="NexumDevs — UPC 2026">
<meta name="robots" content="noindex, nofollow">
```

---

#### 4.2.4. Searching Systems

**Landing Page**

La landing page no implementa búsqueda textual dado que su contenido es estático y está estructurado en secciones claramente diferenciadas. La navegación por anclas cumple la función de localización de contenido de forma más eficiente que una búsqueda para este tipo de producto.

**Web Application**

***Búsqueda de tours***

- **Dónde**: módulo Tour Management, vista de catálogo de la agencia y vista de exploración del turista.
- **Tipo**: búsqueda textual por término libre sobre título y descripción del tour.
- **Filtros disponibles**: dificultad (Easy / Moderate / Hard / Expert), estado (Available / Draft / Closed), duración estimada (rango en horas).
- **Resultado**: lista filtrada de tour cards con título, dificultad, estado y duración. Se actualiza en tiempo real conforme el usuario escribe. Cada card es clickeable para acceder al detalle.
- **Estado vacío**: mensaje "No tours match your search. Try adjusting the filters." con botón "Clear filters" para restablecer la vista completa.

***Búsqueda de turistas asignados***

- **Dónde**: módulo Tour Management, vista de detalle de tour.
- **Tipo**: búsqueda textual por nombre completo o correo electrónico.
- **Filtros disponibles**: estado de asignación (Pending / Confirmed / Cancelled).
- **Resultado**: lista filtrada de turistas con nombre, correo y estado de confirmación. Cada fila expone acciones directas (Unassign).
- **Estado vacío**: mensaje "No tourists found." diferenciando si no hay turistas asignados o si no coinciden con el criterio de búsqueda.

***Búsqueda de incidentes***

- **Dónde**: módulo Safety & Monitoring, vista de incidentes de la expedición.
- **Tipo**: filtrado por categorías predefinidas, sin búsqueda textual libre.
- **Filtros disponibles**: estado (Reported / Acknowledged / Resolved), severidad (Minor / Moderate / Major / Emergency), reportado por (Tourist / Tour Guide).
- **Resultado**: lista filtrada de tarjetas de incidente con descripción, severidad, estado, reportador y timestamp. Los incidentes de mayor severidad se muestran con un indicador de color (rojo para Emergency, naranja para Major).
- **Estado vacío**: mensaje "No incidents recorded for this expedition."

***Búsqueda de notificaciones***

- **Dónde**: módulo Notification & Profile, vista de historial de notificaciones.
- **Tipo**: filtrado por categorías.
- **Filtros disponibles**: tipo (Safety alert / Tour assignment / Expedition update / System), estado (Unread / Read).
- **Resultado**: lista filtrada de notificaciones ordenadas cronológicamente con título, cuerpo, tipo y timestamp. Las no leídas se muestran con un indicador visual (fondo destacado o punto de color).
- **Estado vacío**: mensaje "No notifications yet." para historial vacío, o "No notifications match the selected filters." cuando los filtros no retornan resultados.

***Principios del sistema de búsqueda***

- **No destructiva**: los filtros aplicados no modifican los datos; siempre se puede regresar a la vista completa mediante "Clear filters".
- **Feedback explícito**: el sistema distingue entre "no hay datos registrados" y "no hay coincidencias con los filtros actuales" para evitar que el usuario crea que el sistema tiene un error.
- **Persistencia de filtros**: los filtros activos se mantienen mientras el usuario permanece en la vista; se reinician al salir del módulo.
- **Sin búsqueda global**: no se implementa búsqueda transversal entre módulos. Cada módulo tiene su propio contexto de búsqueda para evitar resultados ambiguos entre entidades de dominios distintos (un "tour" y una "expedition" son entidades diferentes aunque relacionadas).

---

#### 4.2.5. Navigation Systems

**Landing Page**

La landing page implementa un sistema de navegación **global fija** mediante una barra superior que permanece visible durante todo el desplazamiento. Los links funcionan como anclas de sección con scroll suave, permitiendo al visitante orientarse y moverse entre secciones sin perder el contexto de la página.

El botón **Join** actúa como CTA de conversión principal y está diferenciado visualmente del resto de links (botón naranja relleno vs. links de texto). Al presionarlo, abre un modal con dos acciones primarias (Sign in / Create account) y una opción terciaria (Continue as guest), estructurando el flujo de entrada en tres niveles de compromiso.

En mobile (≤ 900px), la navegación colapsa a un menú hamburger que despliega los links verticalmente. El estado abierto/cerrado se comunica visualmente con la animación hamburger → X y mediante el atributo `aria-expanded` para screen readers. Al hacer clic en cualquier link del menú, este se cierra automáticamente y el scroll lleva al usuario a la sección destino.

El recorrido esperado del visitante sigue la progresión natural de la página: Hero → Problem → Tourists o Agencies → Ecosystem → Plans → Testimonials → About → footer con acceso a Terms y Privacy Policy.

**Web Application**

La aplicación web usa un sistema de navegación **lateral persistente** en desktop con acceso directo a los módulos principales desde cualquier pantalla. El módulo activo se resalta visualmente para orientar al usuario sobre su posición dentro de la aplicación.

Se aplica el patrón **hub and spoke**: cada módulo es un hub desde el que se accede a las vistas de detalle. La navegación hacia el detalle siempre expone un mecanismo de retorno (botón "Back" o breadcrumb) para que el usuario pueda regresar al hub sin usar el botón de retroceso del navegador.

La aplicación implementa **navegación contextual** en vistas operativas: cuando hay una expedición activa, el sistema expone acciones relevantes para ese contexto (registrar checkpoint, reportar incidente, ver progreso del grupo) sin necesidad de navegar entre módulos.

El flujo de navegación por rol es el siguiente:

**Administrador de agencia**: Dashboard → Tour Catalog → Tour Detail → Assign Tourists → Live Monitoring → Alerts → Incidents → Export Report.

**Guía de tour**: Active Expedition → Checkpoint List → Register Checkpoint → Report Incident → Group Status → Finish Expedition.

**Turista**: My Tours → Tour Detail → Download Route → Active Expedition → Route Map → Checkpoint Progress → Record Experience → Health Status.

**Mobile Application**

La aplicación móvil usa una **barra de navegación inferior** con cuatro destinos organizados por frecuencia de uso durante la expedición:

| Posición | Destino | Uso |
|---|---|---|
| 1 | Route Map | Principal durante el recorrido |
| 2 | Checkpoints | Frecuente durante el avance |
| 3 | Health | Consulta periódica |
| 4 | Profile | Uso ocasional |

El estado de conectividad (online / offline) se comunica mediante un indicador persistente en la interfaz. Las rutas descargadas previamente son accesibles sin conexión, y el sistema sincroniza automáticamente los datos generados offline cuando se recupera la señal.

---

