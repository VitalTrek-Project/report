# 4.4. Web Applications UX/UI Design

La presente sección documenta la propuesta visual y de interacción correspondiente a la aplicación web de VitalTrek, plataforma orientada al turismo de aventura asistido por dispositivos IoT en zonas de baja conectividad. La propuesta integra los principios de diseño centrado en el usuario, los lineamientos de diseño inclusivo y la arquitectura de información definida en sprints anteriores, garantizando coherencia con el Design System establecido para los productos digitales del proyecto.

El contenido se organiza en cuatro subsecciones complementarias: los **Wireframes**, que constituyen la base estructural y de jerarquía visual de cada pantalla; los **Wireflow Diagrams**, que documentan las transiciones entre wireframes según los User goals de cada User Persona; los **Mock-ups**, que materializan la propuesta visual final aplicando el Design System; y los **User Flow Diagrams**, que integran los mock-ups con los caminos esperados (happy path) y los caminos alternativos (unhappy paths) que el usuario puede recorrer en el sistema.

Los dos User Personas considerados son: **Ana Lucía Quispe**, gerente de operaciones de una agencia mediana de turismo de aventura en Cusco, representante del segmento de agencias y operadores; y **Marco Rodriguez**, viajero europeo experimentado con alto dominio tecnológico, representante del segmento de turistas de aventura nacionales y extranjeros. Cada User goal documentado a continuación responde directamente a las motivaciones y frustraciones identificadas en sus respectivas fichas.

---

## 4.4.1. Web Applications Wireframes

Los Wireframes presentados a continuación constituyen la propuesta estructural de baja fidelidad de la aplicación web de VitalTrek. Cada wireframe fue diseñado aplicando los principios de jerarquía visual, consistencia y proximidad, junto con los criterios de diseño inclusivo (áreas de toque amplias, contraste adecuado en estado de borrador, etiquetas explícitas en elementos interactivos) y la arquitectura de información validada en etapas previas. La herramienta utilizada para su elaboración fue **Figma**, considerando un viewport base de 1920w para la versión light.

Se identifican trece wireframes principales que cubren las funcionalidades clave del sistema, agrupados según los módulos a los que pertenecen:

![Wireframes](../assets/images/wireframes-complete.png)

**Explicación de la propuesta:** Los wireframes se diseñaron bajo un enfoque modular y consistente, manteniendo en todas las pantallas una estructura de tres zonas funcionales: un menú de navegación lateral izquierdo persistente que actúa como anclaje de la arquitectura de información, un área principal de contenido que se reorganiza según el módulo activo, y un footer informativo con datos institucionales. Esta consistencia estructural reduce la carga cognitiva del usuario al moverse entre secciones y refuerza el principio de uniformidad visual.

La jerarquía visual se establece mediante el uso de tipografía escalonada (título principal, subtítulo de sección, etiquetas de campo y texto de cuerpo), espacios en blanco generosos y bloques de contenido claramente delimitados. En las pantallas operativas dirigidas a Ana Lucía (Tour management, Security and monitoring, Agencies, Identity and access), se aplica un patrón de tabla con filtros superiores y acción primaria destacada para soportar las tareas administrativas de alta frecuencia. En las pantallas dirigidas a Marco (Explore routes, Plans and prices), se utilizan grids de tarjetas que facilitan la comparación visual entre opciones, mientras que la pantalla Navigation está optimizada para uso en campo con prominencia del mapa y datos esenciales en panel lateral.

En cuanto a diseño inclusivo, los wireframes contemplan áreas táctiles amplias para botones y elementos clickeables (considerando que Marco puede operar el sistema en condiciones outdoor con guantes o en movimiento), etiquetas textuales explícitas que acompañan a los iconos, soporte para internacionalización (relevante para el perfil europeo de Marco), y un orden de lectura natural que respeta la jerarquía F-pattern característica de las interfaces web occidentales.

---

## 4.4.2. Web Applications Wireflow Diagrams

La presente sección documenta los **Wireflows** diseñados para el sistema VitalTrek, los cuales representan la integración entre los wireframes propuestos y los flujos de interacción que cada User Persona sigue para alcanzar sus respectivos User goals. A diferencia de un Task Flow tradicional, el Wireflow permite visualizar simultáneamente la estructura visual de cada pantalla y la secuencia de transiciones que ocurren como respuesta a las acciones del usuario, evidenciando los cambios de estado mediante la incorporación de un nuevo wireframe por cada paso relevante del flujo.

Para la elaboración de estos diagramas, el equipo trabajó previamente los Task Flows correspondientes a cada User goal, estableciendo consenso sobre las rutas típicas de interacción. Los Wireflows fueron desarrollados considerando los dos User Personas definidos: Ana Lucía Quispe (agencia/operador) y Marco Rodriguez (turista de aventura), redactando los User goals desde la perspectiva de sus motivaciones específicas.

A continuación se presentan los seis Wireflows correspondientes a los User goals más representativos del sistema, tres por cada User Persona.

### 4.4.2.1. Wireflow 01 — Marco registra su cuenta en VitalTrek

**User Persona:** Marco Rodriguez (turista de aventura)

**User goal:** *Como viajero europeo planificando una expedición en Perú, deseo crear una cuenta en VitalTrek desde mi país de origen para preparar mi viaje con anticipación y tener acceso a una plataforma confiable que opere en zonas remotas.*

![Wireflow 01 - Marco registra su cuenta](../assets/images/wireflow-1.png)

**Explicación del flujo:** El flujo se inicia en la pantalla de Login, donde Marco, como nuevo usuario, selecciona la opción "Crear cuenta", lo que dispara una transición hacia el wireframe del formulario de registro en su estado inicial (campos vacíos). Marco procede a diligenciar la información solicitada (nombre, correo, contraseña y confirmación), generando un nuevo estado del wireframe en el que se visualizan los datos ingresados. Al presionar el botón "Registrar", el sistema valida la información y conduce a Marco al wireframe del Hero/landing en su versión autenticada, donde tiene acceso completo a las funcionalidades del rol turista. Este flujo responde a la motivación de Marco de planificar con anticipación una experiencia outdoor auténtica y atiende su frustración por la falta de aplicaciones confiables para el contexto peruano.

### 4.4.2.2. Wireflow 02 — Marco se inscribe en una ruta de aventura

**User Persona:** Marco Rodriguez (turista de aventura)

**User goal:** *Como viajero experimentado con alto poder adquisitivo, deseo explorar el catálogo de rutas y seleccionar aquella que ofrezca una experiencia auténtica acorde a mi nivel técnico, con la confianza de que podré comunicarme con mi familia durante el recorrido.*

![Wireflow 02 - Marco se inscribe en una ruta](../assets/images/wireflow-2.png)

**Explicación del flujo:** El flujo parte del wireframe Hero/landing, desde donde Marco accede al módulo de rutas mediante el menú lateral. Al ingresar, visualiza el wireframe Explore routes con el catálogo completo de rutas disponibles presentadas en formato de tarjetas. Marco aplica filtros de búsqueda (dificultad técnica, duración, ubicación geográfica), generando un nuevo estado del wireframe que refleja únicamente los resultados que cumplen sus criterios. Al hacer clic sobre una tarjeta específica, el flujo transiciona a un nuevo estado del wireframe con el detalle completo de la ruta (descripción cultural e histórica, mapa de la ruta, equipamiento requerido, características de conectividad). Al confirmar la inscripción con el botón "Inscribirme", el flujo retorna al Hero/landing en un estado actualizado. Este Wireflow capitaliza dos motivaciones clave de Marco: enriquecer su experiencia con información cultural del entorno y tener la seguridad de un sistema diseñado para zonas remotas del Perú.

### 4.4.2.3. Wireflow 03 — Marco sigue su expedición en tiempo real

**User Persona:** Marco Rodriguez (turista de aventura)

**User goal:** *Como turista durante una expedición activa en zona remota, deseo seguir mi recorrido en tiempo real y mantener informados a mis familiares sobre mi ubicación, incluso cuando pierdo señal GPS o conectividad continua durante varios días.*

![Wireflow 03 - Marco sigue su expedición](../assets/images/wireflow-3.png)

**Explicación del flujo:** Este Wireflow representa el caso de uso más diferenciador de VitalTrek y responde directamente a las dos frustraciones principales de Marco: la incertidumbre por pérdida de señal GPS y la imposibilidad de avisar a su familia. El flujo es predominantemente reactivo: los cambios de estado se disparan por eventos del dispositivo IoT, no por interacciones explícitas del usuario. El flujo inicia con el wireframe Navigation en su estado de "expedición iniciada", mostrando el mapa de la ruta y el punto de partida. A medida que el dispositivo IoT reporta nueva información de ubicación a través de la red de baja conectividad del sistema, el wireframe transiciona hacia un nuevo estado donde el mapa se actualiza y el panel lateral refleja los datos del trayecto, incluyendo el estado de comunicación con familiares. Al alcanzar un punto de control predefinido, el wireframe presenta un estado de notificación que confirma el envío automático de actualización familiar. Finalmente, al completar la ruta, el flujo conduce a un estado final con el resumen de la expedición. Este Wireflow encarna el diferencial tecnológico IoT que distingue a VitalTrek de competidores como AllTrails o Wayward.

### 4.4.2.4. Wireflow 04 — Ana Lucía monitorea a sus turistas durante un tour

**User Persona:** Ana Lucía Quispe (agencia/operador)

**User goal:** *Como gerente de operaciones de una agencia mediana en Cusco, deseo supervisar en tiempo real las variables vitales y la ubicación de los turistas de cada tour activo para reducir el tiempo de respuesta ante emergencias y profesionalizar la operación de mi agencia.*

![Wireflow 04 - Ana Lucía monitorea turistas](../assets/images/wireflow-4.png)

**Explicación del flujo:** El flujo se origina en el wireframe Tour management, donde Ana Lucía visualiza la lista de tours activos coordinados por su agencia. Al seleccionar un tour específico mediante la acción "Monitorear tour", el flujo transiciona al wireframe Security and monitoring en su estado de dashboard general, presentando las visualizaciones gráficas de los datos recibidos desde los dispositivos IoT de los turistas. Ana Lucía puede aplicar filtros por turista, por guía responsable o por tipo de variable vital, generando un nuevo estado del wireframe con la información segmentada. Si una variable supera un umbral crítico predefinido, el sistema transiciona automáticamente a un nuevo estado del wireframe donde se destaca visualmente la alerta correspondiente, indicando la naturaleza del evento y las acciones recomendadas según el protocolo de la agencia. Este Wireflow atiende directamente la frustración de Ana Lucía por la pérdida de comunicación con los guías por horas y la dependencia de WhatsApp y radios analógicas, posicionando a VitalTrek como herramienta de diferenciación competitiva para su agencia.

### 4.4.2.5. Wireflow 05 — Ana Lucía crea un nuevo tour

**User Persona:** Ana Lucía Quispe (agencia/operador)

**User goal:** *Como responsable de coordinar la operación turística de mi agencia, deseo crear y publicar un nuevo tour dentro del catálogo para gestionar de manera profesional la oferta de servicios y mantener actualizada la información disponible a los turistas.*

![Wireflow 05 - Ana Lucía crea un tour](../assets/images/wireflow-5.png)

**Explicación del flujo:** El flujo inicia en el wireframe Tour management con la tabla de tours existentes visible. Al presionar el botón "+ Nuevo tour", el wireframe transiciona a un nuevo estado donde se presenta el formulario de creación con todos los campos vacíos (nombre del tour, fechas, capacidad máxima, ruta asociada, guías asignados, precio, descripción). Ana Lucía procede a completar la información requerida, generando un nuevo estado del wireframe con los datos diligenciados. Al confirmar mediante el botón "Guardar", el sistema valida la información y conduce al wireframe final con la tabla de tours actualizada, donde se evidencia el nuevo registro creado al inicio de la lista. Este Wireflow responde a la motivación de Ana Lucía de profesionalizar la operación de su agencia mediante herramientas digitales adaptadas al contexto y presupuesto de una micro o pequeña empresa peruana, contrastando con la oferta limitada y costosa de competidores como TrekkSoft.

### 4.4.2.6. Wireflow 06 — Ana Lucía gestiona los permisos de su equipo de guías

**User Persona:** Ana Lucía Quispe (agencia/operador)

**User goal:** *Como gerente de operaciones, deseo gestionar los roles y permisos de los guías y personal de mi agencia para garantizar un control adecuado sobre quién accede a la información de cada tour, fortaleciendo la profesionalización operativa.*

![Wireflow 06 - Ana Lucía gestiona permisos](../assets/images/wireflow-6.png)

**Explicación del flujo:** El flujo parte del wireframe Identity and access en su estado inicial, presentando la lista completa de usuarios vinculados a la agencia de Ana Lucía (guías, asistentes, personal administrativo) con sus roles actuales. Ana Lucía localiza al usuario objetivo mediante los filtros disponibles y hace clic sobre su registro, lo que dispara una transición al wireframe en un nuevo estado con el detalle del usuario seleccionado, mostrando los roles asignados y permisos asociados. Ana Lucía procede a modificar los roles mediante los selectores disponibles, generando un nuevo estado del wireframe que refleja los cambios pendientes de aplicación. Al confirmar mediante el botón "Guardar", el sistema persiste las modificaciones y conduce al wireframe final con la lista de usuarios actualizada. Este Wireflow refuerza la dimensión de profesionalización operativa que es central en la motivación de Ana Lucía, ofreciéndole control granular sobre su equipo en contraste con la informalidad de las comunicaciones vía WhatsApp.

---

## 4.4.3. Web Applications Mock-ups

Los Mock-ups documentados en esta sección constituyen la materialización visual de alta fidelidad de los wireframes presentados previamente. Su elaboración aplica de manera integral el Design System definido para los productos digitales de VitalTrek, incluyendo la paleta cromática institucional, la familia tipográfica seleccionada, el sistema de espaciados, los componentes UI estandarizados y los lineamientos de iconografía. La herramienta utilizada para su construcción fue **Figma**, manteniendo coherencia visual con los wireframes y permitiendo trazabilidad directa entre ambos niveles de fidelidad.

A continuación se presentan los mock-ups correspondientes a las pantallas principales del sistema, agrupados según los módulos definidos en la sección de wireframes:

![Mock-up](../assets/images/mockups-complete.png)

**Explicación de la propuesta:** Los mock-ups aplican consistentemente el Design System establecido, evidenciado en el uso de la paleta cromática principal (con tonos predominantemente naturales asociados al turismo de aventura andino), la tipografía corporativa con escalas tipográficas claras para títulos, subtítulos y cuerpo, y el sistema de espaciado modular que garantiza ritmo visual entre los elementos. Los componentes UI (botones primarios, secundarios y terciarios, campos de formulario, tarjetas, tablas y modales) siguen el catálogo definido en la librería del Design System, lo que asegura consistencia visual y permite escalabilidad en futuras iteraciones.

En relación con los principios de diseño aplicados, se evidencia el uso de jerarquía visual a través de contraste cromático y peso tipográfico, el principio de proximidad mediante la agrupación de elementos relacionados, y el principio de retroalimentación con estados visuales claros (hover, active, disabled, error) en los elementos interactivos. La iconografía utilizada complementa las etiquetas textuales sin sustituirlas, reforzando la comprensión sin generar ambigüedad — un aspecto particularmente relevante para Marco, quien podría utilizar la aplicación en idioma distinto a su lengua materna.

El diseño inclusivo se materializa mediante el uso de contrastes que cumplen los lineamientos WCAG 2.1 en su nivel AA, áreas táctiles mínimas de 44x44 píxeles para elementos interactivos, etiquetas explícitas en todos los campos de formulario, mensajes de error con descripción clara del problema y sugerencia de corrección, y un orden lógico de tabulación para usuarios que navegan con teclado. Adicionalmente, las pantallas dirigidas a Ana Lucía priorizan la densidad informativa controlada (apropiada para perfiles operativos que gestionan múltiples tours simultáneamente), mientras que las pantallas dirigidas a Marco enfatizan la legibilidad en condiciones outdoor y la prominencia visual de la información crítica de seguridad.

---

## 4.4.4. Web Applications User Flow Diagrams

Los User Flow Diagrams documentados en esta sección representan la evolución de alta fidelidad de los Wireflows presentados previamente. Mientras los Wireflows trabajan con representaciones esquemáticas en baja fidelidad, los User Flows integran los Mock-ups finales junto con el detalle completo de los caminos que un usuario puede recorrer en el sistema: tanto la ruta esperada (**happy path**) como las rutas alternativas (**unhappy paths**) que se presentan cuando ocurren errores, validaciones fallidas o decisiones del usuario que se desvían del flujo principal.

Estos User Flows mantienen consistencia directa con los Wireflows definidos en la sección 4.4.2, garantizando trazabilidad de extremo a extremo en el proceso de diseño. Cada diagrama incluye los puntos de decisión, las condiciones de validación y las transiciones entre pantallas, complementados con anotaciones que documentan el comportamiento del sistema en cada bifurcación. Las rutas alternativas fueron diseñadas considerando los escenarios reales identificados durante las entrevistas con representantes de los segmentos objetivo.

### 4.4.4.1. User Flow 01 — Marco registra su cuenta en VitalTrek

**User Persona:** Marco Rodriguez (turista de aventura)

**User goal:** *Como viajero europeo planificando una expedición en Perú, deseo crear una cuenta en VitalTrek desde mi país de origen para preparar mi viaje con anticipación y tener acceso a una plataforma confiable que opere en zonas remotas.*

![User Flow 01 - Marco registra su cuenta](../assets/images/userflow-1.png)

**Explicación del flujo:** El happy path inicia en la pantalla de Login y conduce a Marco al formulario de creación de cuenta, donde completa sus datos personales (nombre, correo, contraseña, país de origen). Al enviar el formulario con información válida, el sistema crea la cuenta y redirige al Hero/landing como turista autenticado, con contenido localizado según su país. Los unhappy paths contemplados son: (a) correo ya registrado, donde el sistema retorna al formulario mostrando un mensaje de error y sugiriendo iniciar sesión o recuperar contraseña; (b) contraseña que no cumple los requisitos mínimos de seguridad, generando un mensaje inline bajo el campo afectado con los criterios pendientes; (c) campos obligatorios vacíos, donde el sistema impide el envío y resalta los campos pendientes; (d) términos y condiciones no aceptados, bloqueando el botón de envío hasta que el checkbox sea marcado; (e) error de conexión durante el registro, mostrando un mensaje de reintento sin perder los datos diligenciados.

### 4.4.4.2. User Flow 02 — Marco se inscribe en una ruta de aventura

**User Persona:** Marco Rodriguez (turista de aventura)

**User goal:** *Como viajero experimentado con alto poder adquisitivo, deseo explorar el catálogo de rutas y seleccionar aquella que ofrezca una experiencia auténtica acorde a mi nivel técnico, con la confianza de que podré comunicarme con mi familia durante el recorrido.*

![User Flow 02 - Marco se inscribe en una ruta](../assets/images/userflow-2.png)

**Explicación del flujo:** El happy path conduce a Marco desde el Hero/landing hasta la pantalla Explore routes, donde aplica filtros, selecciona una ruta y confirma su inscripción, retornando con una notificación de éxito y los detalles del tour en su perfil. Los unhappy paths considerados son: (a) ningún resultado coincide con los filtros aplicados, mostrando un estado vacío con sugerencia de ajustar criterios o ver rutas similares; (b) ruta sin cupos disponibles, donde el botón de inscripción se deshabilita y se ofrece la opción de unirse a una lista de espera o ver fechas alternativas; (c) usuario sin plan activo intentando inscribirse en una ruta premium, lo que dispara una redirección sugerida hacia la pantalla Plans and prices; (d) nivel de dificultad técnica de la ruta superior al perfil declarado por Marco, generando una advertencia que requiere confirmación explícita antes de continuar; (e) error de conexión durante la confirmación, mostrando un mensaje de reintento sin perder los datos seleccionados.

### 4.4.4.3. User Flow 03 — Marco sigue su expedición en tiempo real

**User Persona:** Marco Rodriguez (turista de aventura)

**User goal:** *Como turista durante una expedición activa en zona remota, deseo seguir mi recorrido en tiempo real y mantener informados a mis familiares sobre mi ubicación, incluso cuando pierdo señal GPS o conectividad continua durante varios días.*

![User Flow 03 - Marco sigue su expedición](../assets/images/userflow-3.png)

**Explicación del flujo:** El happy path corresponde a una expedición que avanza normalmente: el dispositivo IoT reporta posición continua a través de la red de baja conectividad, el mapa se actualiza, los familiares de Marco reciben notificaciones automáticas en cada checkpoint, y se completa la ruta con resumen final. Los unhappy paths cubiertos — que constituyen el diferencial central de VitalTrek frente a competidores — son: (a) pérdida temporal de señal GPS, donde el sistema muestra la última posición conocida con marca temporal y activa la búsqueda automática mediante el dispositivo IoT, manteniendo a Marco informado del estado de comunicación; (b) desvío del turista respecto a la ruta planificada, lo que dispara una alerta visual con instrucciones de retorno y notifica simultáneamente al guía responsable; (c) detección de valores anómalos en variables vitales (frecuencia cardiaca elevada, temperatura corporal alterada), generando una notificación a Marco y al equipo de la agencia; (d) imposibilidad temporal de enviar actualización familiar, donde el sistema encola el mensaje y lo despacha automáticamente al recuperar conectividad, mostrando claramente el estado de la comunicación a Marco; (e) cancelación voluntaria de la expedición, que conduce a una pantalla de confirmación y registra el evento para la agencia.

### 4.4.4.4. User Flow 04 — Ana Lucía monitorea a sus turistas durante un tour

**User Persona:** Ana Lucía Quispe (agencia/operador)

**User goal:** *Como gerente de operaciones de una agencia mediana en Cusco, deseo supervisar en tiempo real las variables vitales y la ubicación de los turistas de cada tour activo para reducir el tiempo de respuesta ante emergencias y profesionalizar la operación de mi agencia.*

![User Flow 04 - Ana Lucía monitorea turistas](../assets/images/userflow-4.png)

**Explicación del flujo:** El happy path conduce a Ana Lucía desde Tour management hasta el dashboard de Security and monitoring, donde supervisa las variables sin incidentes durante toda la expedición y revisa el reporte de cierre al finalizar. Los unhappy paths definidos — que responden a los escenarios reales que actualmente Ana Lucía gestiona vía WhatsApp y radios analógicas — son: (a) alerta crítica por variable vital fuera de umbral, que activa una notificación destacada con protocolo de respuesta sugerido y permite contacto inmediato con el guía en campo; (b) pérdida de comunicación con un dispositivo IoT específico, que marca al turista afectado en estado "sin conexión" con tiempo transcurrido y dispara el protocolo de búsqueda; (c) múltiples alertas simultáneas en tours diferentes, donde el sistema prioriza por nivel de criticidad y guía a Ana Lucía en el orden de atención; (d) guía responsable no disponible para responder a una alerta, donde el sistema escala automáticamente a un guía de respaldo o a la propia Ana Lucía; (e) error en la carga del dashboard, mostrando un fallback con los últimos datos cacheados y un botón de reintento manual, garantizando continuidad operativa.

### 4.4.4.5. User Flow 05 — Ana Lucía crea un nuevo tour

**User Persona:** Ana Lucía Quispe (agencia/operador)

**User goal:** *Como responsable de coordinar la operación turística de mi agencia, deseo crear y publicar un nuevo tour dentro del catálogo para gestionar de manera profesional la oferta de servicios y mantener actualizada la información disponible a los turistas.*

![User Flow 05 - Ana Lucía crea un tour](../assets/images/userflow-5.png)

**Explicación del flujo:** El happy path conduce a Ana Lucía desde la tabla de tours hasta el formulario de creación, completando todos los campos requeridos (nombre, fechas, ruta, capacidad, guías asignados, precio) y guardando exitosamente el nuevo registro, que queda disponible inmediatamente en el catálogo. Los unhappy paths considerados son: (a) campos obligatorios incompletos al intentar guardar, donde el sistema resalta los pendientes con mensajes inline específicos; (b) fechas inconsistentes (fecha de inicio posterior a la de fin, o fechas en el pasado), mostrando un mensaje de validación contextual en los campos afectados; (c) capacidad máxima fuera del rango permitido por la política de la agencia, bloqueando el envío hasta corrección; (d) conflicto con otro tour ya programado en las mismas fechas con los mismos guías asignados, donde el sistema detecta la sobreposición y sugiere fechas o guías alternativos; (e) guía asignado sin las certificaciones requeridas para la dificultad técnica de la ruta, lo que dispara una validación que impide guardar hasta que se asigne un guía calificado; (f) error al guardar por pérdida de conexión, manteniendo los datos del formulario para reintento sin pérdida de información.

### 4.4.4.6. User Flow 06 — Ana Lucía gestiona los permisos de su equipo de guías

**User Persona:** Ana Lucía Quispe (agencia/operador)

**User goal:** *Como gerente de operaciones, deseo gestionar los roles y permisos de los guías y personal de mi agencia para garantizar un control adecuado sobre quién accede a la información de cada tour, fortaleciendo la profesionalización operativa.*

![User Flow 06 - Ana Lucía gestiona permisos](../assets/images/userflow-6.png)

**Explicación del flujo:** El happy path conduce a Ana Lucía desde la lista de usuarios de su agencia hasta el detalle del miembro del equipo seleccionado, donde modifica sus roles y guarda los cambios con éxito, viendo reflejado el cambio inmediatamente en la tabla. Los unhappy paths definidos son: (a) intento de remover el rol de Ana Lucía como única gerente con permisos completos, donde el sistema bloquea la acción y solicita asignar previamente otro responsable; (b) asignación de roles incompatibles entre sí (por ejemplo, guía de campo simultáneamente como administrador de identidad), generando una validación que impide guardar hasta resolver el conflicto; (c) usuario actualmente activo en una sesión con los roles previos, donde el sistema advierte que los cambios surtirán efecto al siguiente inicio de sesión y ofrece notificar al usuario afectado; (d) intento de asignar un permiso de monitoreo IoT a un usuario sin entrenamiento certificado en uso del sistema, donde el sistema sugiere agendar capacitación previa; (e) error de persistencia al guardar, mostrando un mensaje de reintento sin perder las modificaciones realizadas en pantalla.