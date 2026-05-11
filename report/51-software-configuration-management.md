## Capítulo V: Product Implementation, Validation & Deployment

### 5.1. Software Configuration Management

#### 5.1.1. Software Development Environment Configuration

Con el objetivo de garantizar un desarrollo fluido, estandarizado y consistente entre todos los miembros del equipo Nexum Devs, se ha definido el siguiente entorno de desarrollo para el ecosistema VitalTrek:

| Actividad                           | Producto           | Propósito / Uso                                                                                                                         | Ruta de referencia / descarga |
|:------------------------------------|:-------------------|:----------------------------------------------------------------------------------------------------------------------------------------|:------------------------------|
| Project Management                  | Trello             | Organización del Product Backlog, planificación de Sprints y monitoreo del avance de tareas del equipo.                                 |                               |
| Requirements Management             | UXPressia          | Elaboración de artefactos de descubrimiento (User Personas, Empathy Maps, Journey Maps e Impact Maps) para la definición de requisitos. |                               |
| UX/UI Design                        | Figma              | Diseño de la guía de estilo, prototipos de baja fidelidad (wireframes) y alta fidelidad (mockups).                                      |                               |
| Big Picture Event Storming          | Miro               | Modelado y representación colaborativa de procesos mediante Event Storming.                                                             |                               |
| User Flows & Wireflows              | LucidChart         | Elaboración de Wireflows y User Flows.                                                                                                  |                               |
| C4 Diagrams                         | Structurizr        | Elaboración de diagramas C4.                                                                                                            |                               |
| Class Diagrams & Database Design    | PlantUML           | Elaboración de diagramas UML y modelado estructural de la base de datos.                                                                |                               |
| Software Development (Backend)      | JetBrains Rider    | Entorno de desarrollo para la implementación de servicios web RESTful con ASP.NET Core y C#.                                            |                               |
| Software Development (Frontend)     | JetBrains WebStorm | Desarrollo de la aplicación web utilizando Vue Framework y tecnologías frontend como HTML5, CSS3 y JavaScript.                          |                               |
| Software Development (Landing Page) | Visual Studio Code | Desarrollo y edición de la Landing Page utilizando tecnologías web estándar.                                                            |                               |
| Version Control                     | GitHub             | Administración de repositorios y control de versiones mediante GitFlow y Conventional Commits.                                          |                               |
| Software Deployment                 | Netlify            | Despliegue y publicación de la Landing Page en un entorno accesible para usuarios.                                                      |                               |
| Documentation                       | Markdown           | Redacción y mantenimiento de la documentación técnica y del reporte del proyecto.                                                       |                               |


#### 5.1.2. Source Code Management

El proyecto utilizará Git como sistema de control de versiones distribuido y GitHub como plataforma de alojamiento de repositorios. Con el propósito de garantizar la trazabilidad, consistencia y control de cambios durante el ciclo de vida del producto digital, se adoptará una estrategia de trabajo basada en GitFlow, permitiendo organizar el desarrollo colaborativo, la integración continua y el mantenimiento de versiones estables del sistema.

Asimismo, cada componente del ecosistema VitalTrek contará con un repositorio independiente, facilitando la modularidad, el control de versiones y la administración de los distintos productos de software desarrollados por el equipo. En el caso de Web Services, el repositorio incluirá tanto el proyecto principal como los archivos correspondientes a pruebas unitarias y pruebas de integración/aceptación.

| Producto | Repositorio | URL |
|:--|:--|:--|
| Landing Page | vitaltrek-landing-page |  |
| Frontend Web Application | vitaltrek-frontend |  |
| Web Services | vitaltrek-backend |  |
| Documentation | NexumDevs |  |

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
├── locales/
│   ├── en.json
│   └── es.json
│
├── news/
│   ├── application/
│   │   └── news.store.js
│   │
│   ├── domain/
│   │   └── model/
│   │       ├── article.entity.js
│   │       └── source.entity.js
│   │
│   ├── infrastructure/
│   │   ├── article.assembler.js
│   │   ├── news-api.js
│   │   └── source.assembler.js
│   │
│   └── presentation/
│       └── components/
│           ├── article-item.vue
│           ├── article-list.vue
│           ├── source-item.vue
│           ├── source-list.vue
│           └── unavailable-content.vue
│
├── shared/
│   ├── infrastructure/
│   │   └── logo-dev-api.js
│   │
│   └── presentation/
│       └── components/
│           ├── footer-content.vue
│           ├── language-switcher.vue
│           └── layout.vue
│
├── app.vue
├── i18n.js
├── main.js
└── style.css
```

Esta estructura arquitectónica será utilizada de manera consistente tanto para aplicaciones frontend como para servicios backend desarrollados por el equipo, garantizando uniformidad en la organización del código, separación clara de responsabilidades y facilidad de escalabilidad del sistema.

#### 5.1.4. Software Deployment Configuration
