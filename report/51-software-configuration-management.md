## Capítulo V: Product Implementation, Validation & Deployment

### 5.1. Software Configuration Management

#### 5.1.1. Software Development Environment Configuration

Con el objetivo de garantizar un desarrollo fluido, estandarizado y consistente entre todos los miembros del equipo Nexum Devs, se ha definido el siguiente entorno de desarrollo para el ecosistema VitalTrek:

| Actividad                           | Producto           | Propósito / Uso                                                                                                                         | Ruta de referencia / descarga                                                                                                                                              |
|:------------------------------------|:-------------------|:----------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Project Management                  | Trello             | Organización del Product Backlog, planificación de Sprints y monitoreo del avance de tareas del equipo.                                 | https://trello.com/invite/b/6a01549806a94e62dfa6d970/ATTIaa1f5e639f52cbe5545e00c59015b13b4225C42A/product-backlog <br>                                                     |
| Requirements Management             | UXPressia          | Elaboración de artefactos de descubrimiento (User Personas, Empathy Maps, Journey Maps e Impact Maps) para la definición de requisitos. | https://uxpressia.com/w/zOJAx                                                                                                                                              |
| UX/UI Design                        | Figma              | Diseño de la guía de estilo, prototipos de baja fidelidad (wireframes) y alta fidelidad (mockups).                                      | https://www.figma.com/design/ggY7QkJXCBcy7VXaPptREz/Figma-basics?node-id=0-286&p=f&t=A39veEYR7UykQwPG-0                                                                    |
| Big Picture Event Storming          | Miro               | Modelado y representación colaborativa de procesos mediante Event Storming.                                                             | https://miro.com/app/board/uXjVHddiCxA=/                                                                                                                                   |
| User Flows & Wireflows              | LucidChart         | Elaboración de Wireflows y User Flows.                                                                                                  | https://lucid.app/lucidchart/43bc9b20-18a3-4d2c-b9a6-85ed008620de/edit?viewport_loc=-2040%2C2618%2C4437%2C2445%2C0_0&invitationId=inv_49759446-823e-49d5-b1b4-d320a18165d8 |
| C4 Diagrams                         | Structurizr        | Elaboración de diagramas C4.                                                                                                            | https://structurizr.com/share/109663/51271721-b088-4007-addf-b09ca1ad0c3f                                                                                                  |
| Class Diagrams & Database Design    | PlantUML           | Elaboración de diagramas UML y modelado estructural de la base de datos.                                                                | https://plantuml.com/es/class-diagram                                                                                                                                      |
| Software Development (Backend)      | JetBrains Rider    | Entorno de desarrollo para la implementación de servicios web RESTful con ASP.NET Core y C#.                                            |                                                                                                                                                                            |
| Software Development (Frontend)     | JetBrains WebStorm | Desarrollo de la aplicación web utilizando Vue Framework y tecnologías frontend como HTML5, CSS3 y JavaScript.                          |                                                                                                                                                                            |
| Software Development (Landing Page) | Visual Studio Code | Desarrollo y edición de la Landing Page utilizando tecnologías web estándar.                                                            |                                                                                                                                                                            |
| Version Control                     | GitHub             | Administración de repositorios y control de versiones mediante GitFlow y Conventional Commits.                                          |                                                                                                                                                                            |
| Software Deployment                 | GitHub Pages       | Despliegue y publicación de la Landing Page en un entorno accesible para usuarios.                                                      | https://vitaltrek-project.github.io/landing-page/                                                                                                                          |
| Software Deployment Web-Application | CloudFare          | Despliegue y publicación de la Web Application en un entorno accesible para usuarios.                                                   | 
| Documentation                       | Markdown           | Redacción y mantenimiento de la documentación técnica y del reporte del proyecto.                                                       |                                                                                                                                                                            |


#### 5.1.2. Source Code Management

El proyecto utilizará Git como sistema de control de versiones distribuido y GitHub como plataforma de alojamiento de repositorios. Con el propósito de garantizar la trazabilidad, consistencia y control de cambios durante el ciclo de vida del producto digital, se adoptará una estrategia de trabajo basada en GitFlow, permitiendo organizar el desarrollo colaborativo, la integración continua y el mantenimiento de versiones estables del sistema.

Asimismo, cada componente del ecosistema VitalTrek contará con un repositorio independiente, facilitando la modularidad, el control de versiones y la administración de los distintos productos de software desarrollados por el equipo. En el caso de Web Services, el repositorio incluirá tanto el proyecto principal como los archivos correspondientes a pruebas unitarias y pruebas de integración/aceptación.

| Producto                 | Repositorio            | URL                                                      |
|:-------------------------|:-----------------------|:---------------------------------------------------------|
| Landing Page             | vitaltrek-landing-page | https://github.com/VitalTrek-Project/landing-page.git    |
| Frontend Web Application | vitaltrek-frontend     | https://github.com/VitalTrek-Project/web-application.git |
| Web Services             | vitaltrek-backend      |                                                          |
| Documentation            | NexumDevs              | https://github.com/VitalTrek-Project/report.git          |

---

##### Estrategia de Ramas (GitFlow)

El flujo de trabajo del proyecto seguirá el modelo GitFlow propuesto por Vincent Driessen, estableciendo ramas específicas para desarrollo, integración, liberación y mantenimiento correctivo.

Las ramas definidas para el proyecto son las siguientes:

- **main**: contiene únicamente versiones estables, aprobadas y listas para producción. Cada liberación será etiquetada utilizando Semantic Versioning.
- **develop**: rama principal de integración continua donde se consolidan las funcionalidades desarrolladas antes de su liberación.
- **feature/***: ramas temporales creadas a partir de `develop` para el desarrollo de nuevas funcionalidades o User Stories.
- **release/***: ramas utilizadas para la preparación, validación y estabilización de nuevas versiones antes de ser desplegadas en producción.

Las funcionalidades serán desarrolladas en ramas `feature/*` y posteriormente integradas a `develop` mediante Pull Requests (PR). Una vez completada la validación de funcionalidades, se preparará una rama `release/*` para estabilizar la versión antes de su integración en `main`. En caso de detectarse errores críticos en producción, se utilizarán ramas `hotfix/*` creadas a partir de `main`.

---

##### Convención para el Nombre de Ramas

Con el objetivo de mantener consistencia y facilitar la identificación de cambios dentro del repositorio, se definieron las siguientes convenciones para el nombramiento de ramas:

| Tipo de rama | Convención | Ejemplo |
|:--|:--|:--|
| Feature Branch | `feature/<nombre-funcionalidad>` | `feature/user-authentication` |
| Release Branch | `release/v<major>.<minor>.<patch>` | `release/v1.0.0` |

---

##### Semantic Versioning

El versionado de liberaciones seguirá el estándar Semantic Versioning 2.0.0 bajo el siguiente formato:

```text
vMAJOR.MINOR.PATCH
```

Donde:

- **MAJOR**: cambios incompatibles o modificaciones significativas.
- **MINOR**: incorporación de nuevas funcionalidades compatibles.
- **PATCH**: corrección de errores o ajustes menores.

Ejemplo de versión:

```text
v1.0.0
```

---

##### Convención de Commits (Conventional Commits)

Todos los mensajes de commit seguirán el estándar Conventional Commits con el objetivo de mantener un historial de cambios claro, consistente y fácilmente rastreable.

La estructura definida para los mensajes de commit es la siguiente:

```text
<tipo>(componente): descripción corta en minúsculas y en infinitivo
```

---

##### Tipos de Commits Permitidos

| Tipo | Uso recomendado | Ejemplo |
|:--|:--|:--|
| **feat** | Incorporación de nuevas funcionalidades | `feat(auth): agregar autenticación mediante JWT` |
| **fix** | Corrección de errores o fallos del sistema | `fix(api): corregir validación de valores nulos` |
| **docs** | Actualizaciones o modificaciones de documentación | `docs(readme): actualizar instrucciones de instalación` |
| **style** | Cambios de formato que no afectan la lógica del código | `style(navbar): ajustar espaciado entre componentes` |
| **refactor** | Reestructuración interna del código sin modificar su comportamiento | `refactor(recipe): simplificar lógica de filtrado` |
| **test** | Creación o modificación de pruebas unitarias o de integración | `test(user): agregar pruebas unitarias de registro` |
| **chore** | Tareas de mantenimiento o configuración del proyecto | `chore(deps): actualizar dependencias npm` |
| **build** | Cambios relacionados con compilación, CI/CD o despliegue | `build(deploy): configurar pipeline de despliegue` |
| **perf** | Mejoras orientadas al rendimiento del sistema | `perf(search): optimizar tiempo de respuesta del filtrado` |

#### 5.1.3. Source Code Style Guide & Conventions

##### Organización del Código

El proyecto seguirá una arquitectura basada en Domain-Driven Design (DDD) y organización modular por funcionalidades (Feature-Based Structure), permitiendo mantener un código desacoplado, reutilizable, escalable y fácil de mantener tanto en frontend como en backend.

Cada funcionalidad del sistema se organiza como un módulo independiente que contiene sus propias capas de responsabilidad, evitando dependencias innecesarias entre contextos del sistema.

Las capas utilizadas en cada módulo son las siguientes:

- `application`: contiene la lógica de aplicación, manejo de estado y coordinación de casos de uso.
- `domain`: contiene entidades, modelos y reglas de negocio del dominio.
- `infrastructure`: contiene acceso a APIs, ensambladores, persistencia y servicios externos.
- `presentation`: contiene componentes visuales e interacción con el usuario.

Asimismo, el sistema incorpora un módulo `shared` destinado a funcionalidades y componentes reutilizables entre diferentes módulos de la aplicación.

La estructura general adoptada en el proyecto es la siguiente:

```text
/src
├── assets/
│
├── locales/
│   ├── en.json
│   └── es.json
│
├── monitoring/
│   ├── application/
│   │   └── monitoring.store.js
│   │
│   ├── domain/
│   │   └── model/
│   │       ├── alert.entity.js
│   │       ├── incident.entity.js
│   │       ├── location.entity.js
│   │       ├── sign.entity.js
│   │       └── tourist.entity.js
│   │
│   ├── infrastructure/
│   │   ├── alert.assembler.js
│   │   ├── incident.assembler.js
│   │   ├── location.assembler.js
│   │   ├── monitoring-api.js
│   │   ├── sign.assembler.js
│   │   └── tourist.assembler.js
│   │
│   └── presentation/
│       ├── components/
│       │   ├── alert-item.vue
│       │   ├── alert-list.vue
│       │   ├── incident-item.vue
│       │   ├── incident-list.vue
│       │   ├── location-item.vue
│       │   ├── location-list.vue
│       │   ├── sign-item.vue
│       │   ├── sign-list.vue
│       │   ├── tourist-item.vue
│       │   └── tourist-list.vue
│       │
│       └── views/
│           └── monitoring-view.vue
│
├── tour-management/
│   ├── application/
│   │   └── tour-management.store.js
│   │
│   ├── domain/
│   │   └── model/
│   │       ├── checkpoint.entity.js
│   │       ├── tour.entity.js
│   │       └── tourist.entity.js
│   │
│   ├── infrastructure/
│   │   ├── checkpoint.assembler.js
│   │   ├── tour.assembler.js
│   │   └── tour-management-api.js
│   │
│   └── presentation/
│       ├── components/
│       │   ├── checkpoint-item.vue
│       │   ├── checkpoint-list.vue
│       │   ├── tour-item.vue
│       │   ├── tour-list.vue
│       │   └── tourist-item.vue
│       │
│       └── views/
│           └── tour-management-view.vue
│
├── shared/
│   ├── infrastructure/
│   │   ├── base-api.js
│   │   └── base-endpoint.js
│   │
│   └── presentation/
│       └── components/
│           ├── footer-content.vue
│           ├── language-switcher.vue
│           └── layout.vue
│
├── navigation/
│   └── index.js
│
├── app.vue
├── i18n.js
├── main.js
└── style.css
```

Esta estructura arquitectónica será utilizada de manera consistente tanto para aplicaciones frontend como para servicios backend desarrollados por el equipo, garantizando uniformidad en la organización del código, separación clara de responsabilidades y facilidad de escalabilidad del sistema.

#### 5.1.4. Software Deployment Configuration


Esta sección describe la configuración de despliegue adoptada para los productos digitales del ecosistema VitalTrek, especificando el proceso necesario para publicar correctamente cada solución a partir de sus respectivos repositorios de código fuente.

Durante este primer sprint, el único producto desplegado corresponde a la Landing Page del proyecto. Debido a su naturaleza estática, el despliegue se realiza utilizando GitHub Pages como plataforma de publicación continua integrada con GitHub.

---

##### Landing Page Deployment

La Landing Page fue desarrollada utilizando HTML5, CSS3 y JavaScript, sin requerir herramientas de compilación, gestores de paquetes ni procesos de build adicionales. El despliegue se realiza directamente desde el repositorio remoto alojado en GitHub.

| Configuración            | Valor                                             |
|:-------------------------|:--------------------------------------------------|
| Producto                 | Landing Page                                      |
| Plataforma de despliegue | GitHub Pages                                      |
| Repositorio fuente       | `vitaltrek-landing-page`                          |
| Rama de despliegue       | `main`                                            |
| Directorio publicado     | `/root`                                           |
| Tipo de despliegue       | Automático                                        |
| URL pública              | https://vitaltrek-project.github.io/landing-page/ |

---

##### Procedimiento de Despliegue

El proceso de despliegue configurado para la Landing Page sigue los siguientes pasos:

1. Crear el repositorio remoto en GitHub bajo la organización del equipo.
2. Subir el código fuente de la Landing Page mediante commits y push hacia la rama `main`.
3. Acceder a la sección **Settings > Pages** dentro del repositorio.
4. Configurar GitHub Pages seleccionando:
    - Source: `Deploy from a branch`
    - Branch: `main`
    - Folder: `/root`
5. Guardar la configuración de publicación.
6. Esperar la generación automática del sitio público por parte de GitHub Pages.
7. Verificar el correcto despliegue accediendo a la URL pública generada.

---

##### Automatización del Despliegue

El despliegue está configurado bajo un esquema de publicación automática. Cada actualización enviada mediante `git push` hacia la rama `main` genera automáticamente una nueva versión desplegada de la Landing Page.

Este enfoque permite mantener sincronizada la versión publicada con el estado actual del repositorio fuente, facilitando la integración continua y la entrega rápida de cambios.

---

##### Consideraciones Técnicas

- El despliegue está orientado exclusivamente a contenido estático.
- No se requiere infraestructura de servidores dedicada.
- No se utilizan contenedores ni pipelines CI/CD personalizados durante este sprint.
- El entorno de publicación es completamente administrado por GitHub Pages.
- La solución desplegada es accesible públicamente mediante una URL permanente.