## 1.2. Solution Profile

### 1.2.1. Antecedentes y problemática

En los últimos años, el turismo de aventura en el Perú ha presentado un crecimiento constante debido al interés de turistas nacionales e internacionales por actividades como trekking, montañismo y exploración en zonas naturales. El Ministerio de Comercio Exterior y Turismo ([MINCETUR](https://www.gob.pe/institucion/mincetur/noticias/563063-se-aprueban-veintidos-modalidades-de-turismo-de-aventura)) reconoce al turismo de aventura como un segmento importante dentro de la actividad turística nacional y ha aprobado diversas modalidades para fortalecer su desarrollo y regulación.

Muchas de estas actividades se desarrollan en áreas alejadas de centros urbanos, donde la cobertura de red móvil es limitada o inexistente debido a las condiciones geográficas del territorio peruano. Según reportes del Organismo Supervisor de Inversión Privada en Telecomunicaciones ([OSIPTEL](https://www.osiptel.gob.pe/portal-del-usuario/noticias/checa-tu-senal-asi-puedes-verificar-la-cobertura-movil-en-tu-distrito/)), todavía existen zonas del país con limitaciones de cobertura móvil y variaciones en la calidad del servicio, especialmente en áreas rurales y de difícil acceso.

Actualmente, las agencias de turismo y los guías dependen principalmente de teléfonos móviles y aplicaciones convencionales de comunicación y geolocalización para coordinar recorridos y mantener contacto con los grupos. Sin embargo, estas herramientas presentan limitaciones en zonas sin señal, generando dificultades para el monitoreo continuo de los turistas y la atención oportuna ante situaciones de emergencia. Esta problemática evidencia la necesidad de implementar soluciones tecnológicas adaptadas al contexto geográfico y operativo del turismo de aventura en el país.

| Pregunta | Formulación | Respuesta |
|----------|-------------|-----------|
| **Who?** | ¿Quiénes son los afectados? | Las agencias de turismo de aventura, los guías turísticos y los turistas nacionales e internacionales que realizan expediciones en zonas remotas del Perú, donde la limitada cobertura móvil dificulta el monitoreo y la comunicación durante el recorrido. |
| **What?** | ¿Cuál es el problema? | La falta de un sistema integrado de monitoreo en tiempo real de ubicación y signos vitales limita la capacidad de respuesta ante emergencias y reduce la seguridad de los turistas durante actividades de aventura en zonas sin cobertura de red. |
| **Where?** | ¿Dónde ocurre? | El problema se presenta en rutas de turismo de aventura ubicadas en zonas remotas del Perú, especialmente en circuitos de trekking de los Andes, selva alta y áreas naturales con geografía compleja y cobertura móvil limitada o inexistente. |
| **When?** | ¿Cuándo se hace más evidente? | Durante el desarrollo de las expediciones, principalmente en situaciones de separación de grupos, cambios climáticos bruscos, recorridos de alta dificultad o ante emergencias médicas como fatiga extrema, deshidratación o mal de altura. |
| **Why?** | ¿Por qué ocurre? | Debido a que las herramientas de comunicación y geolocalización utilizadas actualmente dependen de conexión móvil o internet para funcionar correctamente. En zonas remotas del Perú, la cobertura es limitada o inexistente, lo que genera pérdida de comunicación y dificultades para el monitoreo en tiempo real. |
| **How?** | ¿Cómo se manifiesta? | Se manifiesta mediante pérdida de comunicación entre integrantes del grupo, dificultades para ubicar turistas en tiempo real, retrasos en la atención de emergencias y dependencia de aplicaciones móviles que dejan de funcionar correctamente en zonas sin cobertura. |
| **How Much?** | ¿Cuánta es la magnitud? | El crecimiento sostenido del turismo de aventura en el Perú ha incrementado la cantidad de expediciones realizadas en zonas de difícil acceso. Sin embargo, gran parte de estas áreas presenta limitaciones de conectividad, lo que incrementa los riesgos de accidentes, extravíos y retrasos en la respuesta ante emergencias, afectando tanto la seguridad de los turistas como la capacidad operativa de las agencias. |

---

### 1.2.2. Lean UX Process

#### 1.2.2.1. Lean UX Problem Statements

*Domain*

VitalTrek opera en la intersección de la gestión logística turística, la seguridad preventiva y la telemetría IoT. El entorno de acción se ubica en el turismo de aventura y expediciones al aire libre, específicamente en geografías caracterizadas por la ausencia o intermitencia de infraestructura de telecomunicaciones tradicionales.

*Customer Segments*

El modelo de servicio atiende a dos actores fundamentales en el ecosistema turístico:

- *Segmento B2B (Operativo):* Agencias de turismo de aventura, operadores logísticos, directores de ruta y guías de montaña que gestionan expediciones en zonas remotas del Perú.
- *Segmento B2C (Usuario Final):* Turistas, senderistas y exploradores, nacionales e internacionales, que contratan estos servicios y transitan por rutas de baja o nula conectividad.

*Pain Points*

- *Para las agencias:* La supervisión actual depende de reportes manuales o radiocomunicaciones inestables, generando una ceguera operativa. Desconocen la ubicación exacta y el estado fisiológico de sus clientes en tiempo real, lo que provoca tiempos de reacción lentos ante emergencias, elevando los costos de rescate y exponiendo a la empresa a riesgos legales y reputacionales.
- *Para los turistas:* La desconexión total en zonas remotas genera ansiedad e inseguridad. La incapacidad de acceder a mapas interactivos o información del entorno sin conexión disminuye la autonomía y empobrece la experiencia general del recorrido.

*Gap*

Existe una clara desconexión entre la necesidad de seguridad continua y las herramientas disponibles. Las soluciones satelitales actuales son financieramente prohibitivas para equipar a cada turista de forma individual. Las aplicaciones móviles estándar quedan completamente inoperativas al perder la señal celular. No existe actualmente un sistema híbrido y accesible que integre monitoreo biométrico y geolocalización de forma autónoma, sin depender de redes 4G/5G en tiempo real.

*Vision / Strategy*

Nuestra visión es establecer a VitalTrek como el estándar tecnológico para la gestión de riesgo en el turismo de aventura en el Perú. La estrategia se basa en desplegar una arquitectura de hardware y software resiliente: un ecosistema IoT asincrónico mediante wearables de bajo costo y checkpoints Bluetooth estratégicamente ubicados, que capturen signos vitales y datos de ubicación sincronizados en ráfagas. Esto permitirá transformar la gestión de las agencias de un modelo reactivo a uno predictivo, mediante dashboards centralizados y alertas automatizadas, mientras se dota al turista de herramientas robustas de navegación offline.

*Initial Segment*

El despliegue inicial apuntará a agencias de turismo de aventura de tamaño mediano a grande que operan rutas de trekking de alta exigencia, como circuitos de alta montaña o selva densa. Estas agencias manejan volúmenes considerables de turistas, enfrentan los mayores riesgos operativos por la nula conectividad de sus zonas de trabajo y tienen urgencia por elevar sus estándares internacionales de seguridad.

¿Cómo podemos mejorar la capacidad de respuesta y supervisión en rutas de aventura, logrando que las agencias actúen de manera preventiva y los turistas se sientan seguros incluso sin conexión?

#### 1.2.2.2. Lean UX Assumptions

*Assumptions Worksheet*

*Business Assumptions*

- *Creo que mis clientes tienen la necesidad de* mantener una supervisión constante sobre la ubicación y el estado de salud de los grupos de turistas en zonas remotas, reduciendo la incertidumbre y los tiempos de respuesta ante emergencias, sin depender de redes de telecomunicaciones tradicionales.

- *Estas necesidades pueden resolverse con* VitalTrek, una plataforma web integrada con un ecosistema IoT (wearables y checkpoints Bluetooth) que captura y sincroniza de forma asincrónica datos biométricos y de geolocalización, dotando a las agencias de dashboards de control y a los turistas de herramientas de navegación offline.

- *Mis clientes iniciales son:*
    - *Segmento B2B:* Agencias de turismo de aventura y guías de alta montaña que gestionan rutas en zonas de baja o nula conectividad.
    - *Segmento B2C:* Turistas y senderistas que buscan experiencias al aire libre seguras y desean registrar su progreso.

- *El principal valor que un cliente quiere obtener de mi servicio es* seguridad preventiva y visibilidad operativa en tiempo real de toda la expedición, con autonomía total frente a la falta de cobertura celular.

- *También pueden obtener estos beneficios adicionales:*
    - Para las agencias: reducción de costos en misiones de búsqueda y rescate, y mejora en certificaciones de seguridad internacionales.
    - Para los turistas: acceso a mapas interactivos offline, información contextual del recorrido y registro digital de su experiencia.

- *Adquiriré la mayoría de mis clientes a través de* venta directa B2B a agencias consolidadas, alianzas con asociaciones de guías de montaña y federaciones de andinismo, y presencia en ferias de turismo de aventura.

- *Ganaré dinero mediante* un modelo híbrido HaaS/SaaS: venta o alquiler de infraestructura física (wearables y checkpoints Bluetooth) combinado con suscripción mensual o anual por el uso de la plataforma, almacenamiento en la nube y gestión de alertas.

- *Mi principal competencia en el mercado será* sistemas de comunicación por radio (VHF/UHF), dispositivos de mensajería satelital como Garmin inReach, y la gestión logística puramente manual.

- *Superaremos a la competencia debido a* nuestro enfoque escalable y preventivo: a diferencia de los dispositivos satelitales costosos por usuario, VitalTrek permite monitorear automáticamente a decenas de turistas simultáneamente, detectando anomalías fisiológicas antes de que se conviertan en emergencias críticas.

- *El mayor riesgo de mi producto es* que la latencia en la sincronización asincrónica sea demasiado alta para ser útil en una emergencia médica aguda, o que el hardware sufra averías en condiciones climáticas extremas.

- *Lo resolveremos mediante* un diseño de arquitectura de red que priorice la transmisión de alertas críticas en ráfagas cortas de datos, y certificaciones de resistencia industrial para todo el hardware IoT.

- *Otras suposiciones que, si se demuestran falsas, harán que nuestro negocio fracase:*
    - Que las agencias de turismo estén dispuestas a invertir en infraestructura tecnológica preventiva.
    - Que los turistas acepten utilizar wearables de la agencia sin percibir invasión a su privacidad.

*User Assumptions*

- *¿Quién es el usuario?*
    - El operador (B2B): directores de agencias y guías líderes que necesitan herramientas logísticas para garantizar el retorno seguro de sus grupos.
    - El turista (B2C): personas apasionadas por el trekking que valoran la seguridad y exigen herramientas digitales modernas para enriquecer su viaje.

- *¿Dónde encaja nuestro producto en su vida?* En la fase de ejecución operativa del turismo. Para el guía y la agencia, es su centro de comando durante las expediciones. Para el turista, es su herramienta de navegación y seguridad mientras recorre la ruta.

- *¿Qué problemas soluciona nuestro producto?*
    - La ceguera operativa de las agencias sobre la ubicación exacta de sus grupos.
    - La incapacidad de detectar a tiempo problemas de salud como hipotermia, mal de altura o taquicardia.
    - La desorientación del turista por la inutilidad de aplicaciones tradicionales sin señal.

- *¿Cuándo y cómo se utiliza nuestro producto?*
    - En campo (continuo): los turistas llevan el wearable que recopila datos automáticamente y consultan la app para navegación offline.
    - En base (monitoreo): el personal de la agencia visualiza el dashboard web recibiendo actualizaciones asincrónicas conforme los grupos pasan por los checkpoints.

- *¿Qué características son importantes?* Robustez y tolerancia a fallos de red (offline-first), alertas automatizadas configurables por rangos de signos vitales, sincronización Bluetooth de baja energía transparente, y mapas topográficos descargables optimizados para dispositivos móviles.

- *¿Cómo debe verse y comportarse nuestro producto?* Diseño minimalista, profesional y funcional, con interfaces de alto contraste para facilitar la lectura en exteriores, priorizando la claridad de datos de salud, ubicación y cartografía sin elementos visuales superfluos.

*Feature Assumptions*

- Creemos que nuestros clientes necesitan una plataforma que opere sin conexión continua a internet, sincronizando datos de forma asincrónica mediante checkpoints Bluetooth, para garantizar la trazabilidad logística en zonas de nula o baja conectividad.

- Estas necesidades se pueden resolver con una arquitectura offline-first que capture signos vitales y geolocalización mediante wearables IoT, los almacene localmente y los sincronice en ráfagas cuando el turista pase por un checkpoint BLE.

- El valor principal que un cliente quiere de nuestro servicio es la capacidad de monitorear en tiempo cuasi-real la ubicación y el estado de salud de múltiples grupos simultáneos desde un dashboard centralizado, sin depender de cobertura celular.

- El cliente también puede obtener estos beneficios adicionales: generación automática de reportes de expedición, registro digital de la experiencia del turista compartible en redes sociales, y alertas tempranas configurables por umbrales de signos vitales que permiten intervención preventiva antes de que ocurra una emergencia.

- Vamos a adquirir la mayoría de nuestros clientes a través de pilotos gratuitos de tres meses con agencias de turismo de aventura en Cusco y Áncash, demostraciones en campo y alianzas con DIRCETUR y asociaciones gremiales del sector.

- Haremos dinero a través de un modelo híbrido: suscripción mensual o anual por el uso de la plataforma según el volumen de turistas gestionados, combinado con alquiler o venta de la infraestructura física de wearables y checkpoints Bluetooth.

- Nuestra competencia principal en el mercado serán TrekkSoft, AllTrails y Garmin inReach, además de métodos tradicionales como radiocomunicación VHF/UHF, coordinación por WhatsApp y seguimiento manual por parte de los guías.

- Los venceremos debido a que VitalTrek es la única plataforma que integra gestión operativa para agencias, navegación offline para turistas e IoT biométrico en un solo ecosistema diseñado específicamente para el contexto peruano de baja conectividad.

- Nuestro mayor riesgo de producto es que la latencia entre checkpoints sea demasiado alta para responder oportunamente ante una emergencia médica aguda, o que las agencias rechacen la inversión inicial en hardware por considerarla elevada.

- Resolveremos esto a través de una arquitectura de red que priorice la transmisión de alertas críticas, un modelo de alquiler de hardware que elimine la barrera de inversión inicial, y validaciones tempranas en campo con usuarios reales de los segmentos objetivo.

- Otra suposición es que los turistas estarán dispuestos a utilizar los wearables proporcionados por la agencia durante todo el recorrido. Si esto resulta falso, el sistema de monitoreo biométrico no podrá operar, lo que afectaría la propuesta de valor central de la plataforma.

*Business Outcomes*

- Reducción del 40% en evacuaciones médicas de emergencia durante los primeros seis meses de uso en campo.
- Registro exitoso del paso del 95% de los turistas por los puntos de control con una pérdida de paquetes de datos inferior al 5%.
- Tasa de conversión del 25% de agencias que pasan de piloto gratuito a suscripción anual pagada dentro de los primeros 3 meses.
- Calificación de sensación de seguridad como "Alta" o "Muy Alta" por al menos el 85% de los turistas en encuestas post-tour.

#### 1.2.2.3. Lean UX Hypothesis Statements

### Statement 1: Preventive Biometric Monitoring

*Creemos que* equipar a los turistas con wearables IoT que monitorean sus signos vitales permitirá a los guías anticiparse a problemas de salud severos como el mal de altura o agotamiento extremo antes de que se conviertan en emergencias críticas.

*Sabremos que hemos tenido éxito cuando* los reportes operativos de las agencias muestren una reducción del 40% en evacuaciones médicas de emergencia durante los primeros seis meses de uso en campo.

---

### Statement 2: Asynchronous BLE Synchronization

*Creemos que* implementar checkpoints Bluetooth estratégicos a lo largo de la ruta para sincronizar datos de forma asincrónica garantizará la trazabilidad logística en zonas sin cobertura celular, sin necesidad de costosos equipos satelitales.

*Sabremos que hemos tenido éxito cuando* los dashboards de la agencia registren exitosamente el paso del 95% de los turistas por los puntos de control con una pérdida de paquetes de datos inferior al 5%.

---

### Statement 3: Offline Navigation and Autonomy

*Creemos que* proveer a los turistas con una aplicación móvil que contenga mapas topográficos interactivos e información contextual disponible 100% offline reducirá su ansiedad ante la desconexión y mejorará su percepción de seguridad durante el recorrido.

*Sabremos que hemos tenido éxito cuando* las encuestas de satisfacción post-tour indiquen que al menos el 85% de los usuarios califiquen su sensación de seguridad como "Alta" o "Muy Alta" durante los tramos de cero conectividad.

---

### Statement 4: Centralized Dashboards and Alerts

*Creemos que* centralizar la información de múltiples grupos simultáneos en un único dashboard web con alertas automatizadas por anomalías reducirá la carga operativa de los responsables de la agencia y mejorará su capacidad de respuesta ante incidentes.

*Sabremos que hemos tenido éxito cuando* el tiempo promedio de respuesta de la agencia ante una alerta temprana, desde que se detecta la anomalía hasta que se notifica al guía en campo, se reduzca a menos de 5 minutos.

---

### Statement 5: Digital Experience Record

*Creemos que* generar un resumen digital interactivo al finalizar el recorrido, que incluya la ruta trazada, hitos alcanzados y métricas físicas, incentivará a los turistas a compartir su logro en redes sociales, generando visibilidad orgánica para la agencia operadora.

*Sabremos que hemos tenido éxito cuando* al menos el 20% de los turistas que finalizan un tour compartan su resumen en redes sociales etiquetando a la agencia en los primeros 30 días posteriores al lanzamiento.

---

### Statement 6: Hybrid SaaS/HaaS Model Adoption

*Creemos que* ofrecer la infraestructura (wearables y checkpoints) bajo un modelo de alquiler combinado con una suscripción de software escalable según el volumen de turistas derribará la barrera de entrada económica para las agencias medianas y acelerará su adopción.

*Sabremos que hemos tenido éxito cuando* logremos una tasa de conversión del 25% de agencias que pasan de la fase de piloto gratuito a suscripción anual pagada dentro de un periodo de 3 meses.

#### 1.2.2.4. Lean UX Canvas

| 1. Business Problem | 5. Solutions | 2. Business Outcomes |
|---|---|---|
| Las agencias de turismo de aventura del Perú carecen de herramientas accesibles para monitorear en tiempo real la ubicación y el estado de salud de sus clientes en zonas remotas con baja o nula conectividad celular. Esto genera ceguera operativa, tiempos de respuesta lentos ante emergencias médicas y extravíos, y expone a las agencias a riesgos legales y reputacionales. Los turistas, por su parte, no cuentan con herramientas de navegación funcionales sin señal, lo que incrementa su ansiedad y reduce su autonomía durante el recorrido. | - Plataforma web con dashboard centralizado para monitoreo de múltiples grupos en tiempo cuasi-real y alertas automatizadas ante anomalías. <br><br> - Wearables IoT de bajo costo para captura continua de signos vitales y geolocalización. <br><br> - Checkpoints Bluetooth para sincronización asincrónica de datos sin necesidad de cobertura celular. <br><br> - Aplicación móvil para turistas con mapas topográficos interactivos y navegación 100% offline. <br><br> - Generación automática de resumen digital de la experiencia del recorrido al finalizar el tour. | - Reducción del 40% en evacuaciones médicas de emergencia en los primeros 6 meses de uso. <br><br> - Registro exitoso del 95% de turistas en puntos de control con pérdida de datos inferior al 5%. <br><br> - Tasa de conversión del 25% de agencias de piloto gratuito a suscripción anual en 3 meses. <br><br> - El 85% de turistas califica su sensación de seguridad como "Alta" o "Muy Alta" en encuestas post-tour. |

| 3. Users & Customers | 4. User Outcomes & Benefits |
|---|---|
| *B2B (Operativo):* Agencias de turismo de aventura, directores de ruta y guías de montaña que gestionan expediciones en zonas remotas del Perú. <br><br> *B2C (Usuario Final):* Turistas nacionales e internacionales, senderistas y exploradores que contratan estos servicios y transitan por rutas de baja o nula conectividad. | - Respuesta inmediata ante emergencias de salud como taquicardia, hipotermia o fatiga extrema gracias a alertas preventivas. <br><br> - Navegación segura y autónoma sin dependencia de red móvil mediante mapas offline. <br><br> - Registro digital interactivo de la experiencia del recorrido compartible en redes sociales. <br><br> - Reducción de costos logísticos en misiones de búsqueda y rescate. <br><br> - Escalabilidad en la gestión simultánea de múltiples rutas y grupos desde un solo dashboard. |

| 6. Hypotheses | 7. What's the Most Important Thing We Need to Learn First? | 8. What's the Least Amount of Work We Need to Do to Learn the Next Most Important Thing? |
|---|---|---|
| - El monitoreo biométrico continuo mediante wearables permitirá reducir en un 40% las evacuaciones de emergencia. <br><br> - La sincronización asincrónica BLE garantizará trazabilidad del 95% de turistas sin cobertura celular. <br><br> - La navegación offline reducirá la ansiedad del turista y logrará que el 85% califique su seguridad como alta. <br><br> - Los dashboards centralizados reducirán el tiempo de respuesta ante alertas a menos de 5 minutos. <br><br> - El modelo híbrido HaaS/SaaS logrará una conversión del 25% de pilotos a suscripciones pagadas en 3 meses. | ¿Es la precisión y latencia de los datos capturados por los wearables y sincronizados mediante checkpoints Bluetooth suficiente para activar alertas de rescate confiables en entornos de clima extremo y geografía compleja? | Desarrollar un MVP consistente en un wearable básico conectado a un checkpoint BLE, y realizar una prueba de campo en una ruta de senderismo conocida con 5 usuarios reales, midiendo la latencia de sincronización de datos y la tasa de pérdida de paquetes bajo condiciones climáticas variables. |

