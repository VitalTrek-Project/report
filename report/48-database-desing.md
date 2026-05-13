### 4.8. Database Design
#### 4.8.1. Database Diagrams

El diseño de base de datos de VitalTrek está estructurado en 5 bounded
contexts con 15 tablas, siguiendo los principios de Domain-Driven Design
para garantizar modularidad, escalabilidad y mantenibilidad. Cada contexto
—Identity & Access, Tour Management, Navigation & Exploration, Safety &
Monitoring y Notification & Profile— gestiona de forma autónoma una parte
específica del sistema, pero todos están integrados mediante claves foráneas
UUID que reflejan el flujo operativo del negocio: desde el registro del
usuario y la configuración del tour, hasta la ejecución de la expedición,
el monitoreo de seguridad en tiempo real y la entrega de notificaciones.
Esta arquitectura desacoplada pero conectada garantiza trazabilidad completa
del recorrido, monitoreo biométrico continuo, sincronización offline y una
gestión eficiente de toda la operación de turismo de aventura.

![Imagen de la base de datos](../assets/images/VitalTrek_DatabaseDiagram.png)