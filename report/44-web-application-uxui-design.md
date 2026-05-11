#### 4.4.3. Web Applications User Flow Diagrams

En esta sección se presentan los User Flows de VitalTrek, los cuales describen la ruta lógica que siguen los distintos usuarios para cumplir sus objetivos dentro de la plataforma.
<br>
A diferencia de los wireflows estructurales, estos diagramas incorporan los mock-ups de las pantallas, permitiendo visualizar la interacción del usuario con la interfaz durante cada etapa del recorrido. Se incluyen tanto el flujo principal (Happy Path) como las rutas alternativas o de error (Unhappy Paths), considerando situaciones como pérdida de conectividad, datos inválidos o incidencias durante el tour.

##### Turista de aventura
**User Goal:** Consultar y descargar la ruta del tour antes de iniciar el recorrido para acceder a ella sin conexión durante la actividad.

**Descripción del flujo:** El flujo inicia cuando la turista accede a la plataforma e inicia sesión. Luego visualiza la lista de tours disponibles, selecciona uno y accede al detalle del recorrido. Desde esta pantalla puede revisar el mapa, los checkpoints y descargar la ruta para utilizarla sin conexión.
<br>

El happy path ocurre cuando las credenciales son válidas y la descarga se completa correctamente.
<br>
Los unhappy paths contemplan situaciones como credenciales inválidas, falla de descarga o indisponibilidad temporal de la ruta.
<br><br>![Web Applications User Flow Diagrams 1](../assets/images/Web-Applications-User-Flow-Diagrams-1.png)

##### Agencia de turismo
**User Goal:** Monitorear el estado y la ubicación del grupo durante el desarrollo del tour para identificar posibles incidencias a tiempo.
**Descripción del flujo:** El flujo inicia cuando el operador de la agencia ingresa al sistema y accede al dashboard principal. Desde allí selecciona un tour activo y visualiza el mapa con la ubicación del grupo y el estado general del recorrido.
<br>

El happy path ocurre cuando los datos del recorrido se reciben correctamente y el monitoreo continúa sin incidencias.
<br>
Los unhappy paths incluyen pérdida de conectividad, ausencia de nuevos datos o detección de una anomalía que genera una alerta para seguimiento.
<br><br>![Web Applications User Flow Diagrams 2](../assets/images/Web-Applications-User-Flow-Diagrams-2.png)
