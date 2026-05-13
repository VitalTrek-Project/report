### 4.7. Software Object-Oriented Design
#### 4.7.1. Class Diagrams

**Bounded Context: Shared**
Agrupa los componentes y servicios transversales reutilizados por toda 
la aplicación. Incluye `Layout`, `LanguageSwitcher` y `FooterContent` 
como componentes de presentación comunes, junto con `BaseApi` y 
`BaseEndpoint` como infraestructura base que extienden las APIs 
específicas de cada bounded context
.
![Class Diagram](../assets/images/VitalTrek_Shared_ClassDiagram.png)

**Bounded Context: Safety & Monitoring**
Supervisa el bienestar de los turistas y la captura de datos en zonas remotas.
Se centra en la entidad IoTDevice (wearables), gestionando las lecturas de signos vitales (VitalSignReading) y geolocalización (LocationLog) sincronizadas mediante Checkpoint Bluetooth. También maneja Alert para registrar y notificar anomalías o riesgos en tiempo real.

![Class Diagram](../assets/images/VitalTrek_SafetyMonitoring_ClassDiagram.png)

**Bounded Context: Navigation & Exploration**
Gestiona la orientación del turista y el registro de su viaje, operando incluso en baja conectividad.
Incluye la entidad Route y sus Waypoint (tramos del recorrido), así como PointOfInterest para información contextual. También administra OfflineMap para la disponibilidad sin conexión y ExperienceLog donde el turista documenta su recorrido.

![Class Diagram](../assets/images/VitalTrek_NavigationExploration_ClassDiagram.png)

**Bounded Context: Identity & Access**
Controla la seguridad de acceso, autenticación y autorización en la plataforma.
La entidad principal es User, vinculada a Credential y Role. Permite diferenciar los accesos y permisos específicos entre los turistas, los guías de expedición y los administradores de las agencias de turismo.

![Class Diagram](../assets/images/VitalTrek_IdentityAccess_ClassDiagram.png)

**Bounded Context: Tour Management**
Centraliza la planificación, ejecución y supervisión operativa de las excursiones.
Se basa en la entidad Tour, que conecta a la agencia (Agency) con el personal en campo (Guide) y el grupo de viajeros (TouristGroup). Incluye Itinerary para gestionar los horarios y el progreso general que se visualiza en los dashboards de la agencia.

![Class Diagram](../assets/images/VitalTrek_TourManagement_ClassDiagram.png)

**Bounded Context: Notification & Profile**
Administra la información personal de los usuarios y el sistema de avisos de la plataforma.
Incluye la entidad Profile, que guarda información vital y de EmergencyContact. Además, gestiona Notification para despachar alertas de seguridad, desvíos de ruta o confirmaciones de sincronización asincrónica de datos al recuperar la conectividad.

![Class Diagram](../assets/images/VitalTrek_NotificationProfile_ClassDiagram.png)


