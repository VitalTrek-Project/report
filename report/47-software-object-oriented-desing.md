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
Supervisa la seguridad de los turistas durante la expedición mediante 
monitoreo en tiempo real. Administra `Location`, `VitalSignReading`, 
`Alert` e `Incident` a través de `SafetyStore`, permitiendo detectar 
anomalías y exportar reportes operativos.

![Class Diagram](../assets/images/VitalTrek_SafetyMonitoring_ClassDiagram.png)

**Bounded Context: Navigation & Exploration**
Gestiona la ejecución de expediciones en campo y la experiencia del 
turista durante el recorrido. Incluye `Expedition` como entidad central, 
junto con `Progress`, `TouristExperience` y `Weather`, coordinados por 
`NavigationStore` para navegación offline y registro multimedia.

![Class Diagram](../assets/images/VitalTrek_NavigationExploration_ClassDiagram.png)

**Bounded Context: Identity & Access**
Gestiona el registro, autenticación y ciclo de vida de las cuentas de 
usuario. Se centra en `User` y `Session`, administradas mediante 
`IdentityStore` para operaciones de login, registro, recuperación de 
contraseña y gestión de sesiones activas.

![Class Diagram](../assets/images/VitalTrek_IdentityAccess_ClassDiagram.png)

**Bounded Context: Tour Management**
Controla la creación y administración del catálogo de tours por parte 
de las agencias. La entidad principal es `Tour`, que se compone de 
`Checkpoint` y se asocia con `Tourist` mediante asignaciones, todo 
gestionado a través de `TourManagementStore`.

![Class Diagram](../assets/images/VitalTrek_TourManagement_ClassDiagram.png)

**Bounded Context: Notification & Profile**
Administra los datos personales del usuario y la entrega de 
notificaciones del sistema. Se basa en `Profile`, `NotificationPreferences` 
y `Notification`, gestionados por `ProfileStore` para personalización 
de la cuenta y configuración de canales de comunicación.

![Class Diagram](../assets/images/VitalTrek_NotificationProfile_ClassDiagram.png)


