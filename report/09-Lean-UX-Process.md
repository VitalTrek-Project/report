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