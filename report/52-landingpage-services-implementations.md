## 5.2.1. Sprint 1

En esta sección se registra y explica el avance en términos de producto y trabajo colaborativo correspondiente al Sprint 1 del proyecto VitalTrek. Durante este sprint, el equipo concentró sus esfuerzos en la implementación de la Landing Page estática de la plataforma, que constituye el primer punto de contacto con los segmentos objetivo: turistas aventureros y administradores de agencias de tours de aventura.

---

### 5.2.1.1. Sprint Planning 1

A continuación se presenta el resumen de la reunión de Sprint Planning correspondiente al Sprint 1, llevada a cabo de forma virtual mediante Discord. En esta reunión el equipo definió el Sprint Goal, acordó la velocidad del sprint y seleccionó las User Stories que serían abordadas durante la iteración.

El Sprint Goal fue formulado considerando el enfoque de negocio y la perspectiva de los visitantes del sitio, siguiendo el template recomendado por Scrum.org:

> **"Our focus is on** publishing a fully functional and bilingual Landing Page for VitalTrek. **We believe it delivers** a clear understanding of the platform's value proposition — including its features, offline capabilities, and security measures — to prospective tourists and tour agency administrators visiting the site. **This will be confirmed when** visitors can navigate all sections of the landing page, consult benefits tailored to each user segment, access a system demonstration, and submit a contact message — all available in both English and Spanish."

| Campo | Detalle |
|:------|:--------|
| **Sprint #** | Sprint 1 |
| **Date** | 2026-05-9 |
| **Time** | 10:00 PM |
| **Location** | Discord  |
| **Prepared By** | Quispe Perez, Edu |
| **Attendees (to planning meeting)** | Rodriguez, Miler / Verastigue, Giancarlo / Vilchez, Gabriel / Alfaro, Joaquin / Quispe Perez, Edu |
| **Sprint n – 1 Review Summary** | Al tratarse del primer sprint del proyecto, no existe sprint previo que revisar. El equipo inició la iteración con el Product Backlog definido y los artefactos de Requirements Engineering completados. |
| **Sprint n – 1 Retrospective Summary** | Al tratarse del primer sprint del proyecto, no aplica retrospectiva anterior. El equipo acordó establecer canales de comunicación en Discord, distribuir responsabilidades por sección de la landing page y mantener una convención de commits descriptiva desde el inicio del desarrollo. |
| **Sprint 1 Goal** | Our focus is on publishing a fully functional and bilingual Landing Page for VitalTrek. We believe it delivers a clear understanding of the platform's value proposition including its features, offline capabilities, and security measures to prospective tourists and tour agency administrators visiting the site. This will be confirmed when visitors can navigate all sections of the landing page, consult benefits tailored to each user segment, access a system demonstration, and submit a contact message all available in both English and Spanish. |
| **Sprint 1 Velocity** | 24 Story Points |
| **Sum of Story Points** | 24 Story Points |

---

### 5.2.1.2. Aspect Leaders and Collaborators

Durante el Sprint 1, el equipo identificó seis aspectos principales correspondientes al alcance funcional de la Landing Page de VitalTrek. Cada aspecto agrupa un conjunto de User Stories relacionadas y representa una unidad de trabajo coherente dentro de la iteración. La distribución de líderes y colaboradores se estableció en función de las fortalezas de cada integrante y tiene correspondencia directa con la selección de tasks en el Sprint Backlog.

Los aspectos considerados para este sprint son: Hero & Navigation, Benefits & Features Section, Demo & Offline Info Section, Contact & Security Section, Testimonials & Team Section, e i18n & Deployment.

| Team Member (Last Name, First Name) | GitHub Username | Hero & Navigation Leader (L) / Collaborator (C) | Benefits & Features Section Leader (L) / Collaborator (C) | Demo & Offline Info Section Leader (L) / Collaborator (C) | Contact & Security Section Leader (L) / Collaborator (C) | Testimonials & Team Section Leader (L) / Collaborator (C) | i18n & Deployment Leader (L) / Collaborator (C) |
|:-------------------------------------|:----------------|:--------------------------------------------------|:-----------------------------------------------------------|:-----------------------------------------------------------|:----------------------------------------------------------|:----------------------------------------------------------|:------------------------------------------------|
| Quispe Perez, Edu | Eder_09 | C | C | C | C | C | L |
| Rodriguez, Miler | Miler2003 | L | C | C | C | C | C |
| Verastigue, Giancarlo | CaLoVM | C | L | C | C | C | C |
| Alfaro, Joaquin | elprrr | C | C | L | C | C | C |
| Vilchez, Gabriel | GZ-99 | C | C | C | L | L | C |

---

### 5.2.1.3. Sprint Backlog 1

El objetivo principal del Sprint 1 fue implementar la Landing Page completa y bilingüe de VitalTrek, cubriendo todas las secciones informativas dirigidas a los segmentos de turistas aventureros y administradores de agencias de tours. Al cierre del sprint, todas las User Stories comprometidas fueron completadas satisfactoriamente.

A continuación se presenta el screenshot del board de control utilizado durante el sprint, junto con el URL público.

**Board:** https://trello.com/invite/b/6a0567247c8e53cf8fc17be3/ATTI7e5cdb3f9c2996b8b79b09dace8562264A21CD8D/vitaltrek-sprint-1(#)

![VitalTrek Sprint Backlog 1](../assets/images/vitaltrek-sprint-backlog1.png)

---

| Sprint # | Sprint 1 |
|:---------|:---------|

| User Story | | Work-Item / Task | | | | |
|:-----------|:-|:-----------------|:-|:-|:-|:-|
| **Id** | **Title** | **Id** | **Title** | **Description** | **Estimation (Hours)** | **Assigned To** | **Status** |

| Id | Title | Id | Title | Description | Estimation (Hours) | Assigned To | Status |
|:---|:------|:---|:------|:------------|:-------------------|:------------|:-------|
| US-LP01 | Conocer la propuesta de valor | T01 | Diseñar sección Hero | Implementar la sección hero con headline, descripción de la propuesta de valor y CTA principal. | 3 | Rodriguez, Miler | Done |
| | | T02 | Redactar copy de propuesta de valor (EN/ES) | Redactar el contenido textual de la propuesta de valor en inglés y español. | 1 | Alfaro, Joaquin | Done |
| US-LP02 | Navegar entre secciones de la landing | T03 | Implementar Navbar responsive | Desarrollar la barra de navegación con enlaces a todas las secciones y comportamiento responsive. | 3 | Rodriguez, Miler | Done |
| | | T04 | Implementar menú hamburguesa móvil | Implementar el menú colapsable para dispositivos móviles mediante JavaScript. | 2 | Rodriguez, Miler | Done |
| US-LP03 | Conocer beneficios para turistas | T05 | Diseñar sección de beneficios para turistas | Implementar la sección con los beneficios específicos dirigidos al segmento turista, con íconos y descripciones. | 2 | Verastigue, Giancarlo | Done |
| | | T06 | Redactar contenido de beneficios para turistas (EN/ES) | Redactar los textos descriptivos de cada beneficio para el segmento turista en inglés y español. | 1 | Alfaro, Joaquin | Done |
| US-LP04 | Conocer beneficios para administradores de agencia | T07 | Diseñar sección de beneficios para agencias | Implementar la sección con los beneficios específicos dirigidos al segmento agencia, con íconos y descripciones. | 2 | Verastigue, Giancarlo | Done |
| | | T08 | Redactar contenido de beneficios para agencias (EN/ES) | Redactar los textos descriptivos de cada beneficio para el segmento agencia en inglés y español. | 1 | Alfaro, Joaquin | Done |
| US-LP05 | Conocer las funcionalidades principales | T09 | Diseñar sección de funcionalidades | Implementar la sección que presenta las funcionalidades principales del sistema con íconos y descripciones breves. | 2 | Verastigue, Giancarlo | Done |
| | | T10 | Redactar contenido de funcionalidades (EN/ES) | Redactar los textos de cada funcionalidad principal en inglés y español. | 1 | Alfaro, Joaquin | Done |
| US-LP06 | Acceder al registro desde la landing | T11 | Implementar CTA de registro | Añadir botón de acceso rápido al registro en la sección hero y en la navbar. | 1 | Rodriguez, Miler | Done |
| US-LP07 | Acceder a una demostración del sistema | T12 | Diseñar sección de demostración | Implementar la sección que presenta capturas o mockups del sistema con descripción del flujo de uso. | 3 | Alfaro, Joaquin | Done |
| | | T13 | Redactar contenido de demostración (EN/ES) | Redactar los textos descriptivos del flujo de demostración en inglés y español. | 1 | Alfaro, Joaquin | Done |
| US-LP08 | Conocer la compatibilidad offline | T14 | Diseñar sección de compatibilidad offline | Implementar la sección que comunica las capacidades offline de la plataforma. | 1 | Alfaro, Joaquin | Done |
| | | T15 | Redactar contenido offline (EN/ES) | Redactar los textos sobre compatibilidad offline en inglés y español. | 1 | Alfaro, Joaquin | Done |
| US-LP09 | Contactar al equipo de VitalTrek | T16 | Diseñar sección de contacto | Implementar la sección de contacto con formulario de nombre, correo y mensaje. | 2 | Vilchez, Gabriel | Done |
| | | T17 | Implementar validación del formulario de contacto | Añadir validación de campos requeridos y formato de correo electrónico mediante JavaScript. | 2 | Vilchez, Gabriel | Done |
| | | T18 | Redactar contenido de contacto (EN/ES) | Redactar los textos de la sección de contacto en inglés y español. | 1 | Alfaro, Joaquin | Done |
| US-LP10 | Conocer las medidas de seguridad de datos | T19 | Diseñar sección de seguridad de datos | Implementar la sección que comunica las medidas de protección de información personal de los usuarios. | 1 | Vilchez, Gabriel | Done |
| | | T20 | Redactar contenido de seguridad (EN/ES) | Redactar los textos sobre medidas de seguridad de datos en inglés y español. | 1 | Alfaro, Joaquin | Done |
| US-LP11 | Conocer testimonios y casos de uso | T21 | Diseñar sección de testimonios | Implementar la sección de testimonios con tarjetas de casos de uso reales o representativos. | 2 | Vilchez, Gabriel | Done |
| | | T22 | Redactar contenido de testimonios (EN/ES) | Redactar los testimonios y casos de uso en inglés y español. | 1 | Alfaro, Joaquin | Done |
| US-LP12 | Conocer el equipo de la startup | T23 | Diseñar sección del equipo | Implementar la sección con las tarjetas de presentación de los integrantes del equipo VitalTrek. | 2 | Vilchez, Gabriel | Done |
| | | T24 | Redactar contenido del equipo (EN/ES) | Redactar las descripciones de cada integrante del equipo en inglés y español. | 1 | Alfaro, Joaquin | Done |
| | | T25 | Implementar toggle de idioma EN/ES | Desarrollar la funcionalidad de cambio de idioma mediante JavaScript con atributos data-i18n. | 3 | Quispe Perez, Edu | Done |
| | | T26 | Implementar archivo de traducciones | Crear y estructurar el objeto de traducciones en JavaScript para todos los textos de la landing page. | 2 | Quispe Perez, Edu | Done |
| | | T27 | Despliegue en GitHub Pages | Configurar y publicar la landing page en GitHub Pages bajo el repositorio de NexumDevs. | 1 | Quispe Perez, Edu | Done |
| | | T28 | Diseñar Footer | Implementar el footer con links de navegación, redes sociales e información de contacto. | 1 | Quispe Perez, Edu | Done |

### 5.2.1.4. Development Evidence for Sprint Review

Durante el Sprint 1, el equipo implementó la Landing Page estática y bilingüe de VitalTrek utilizando HTML, CSS y JavaScript vanilla. Los avances cubrieron la estructura semántica completa del sitio, los estilos visuales con variables CSS, la funcionalidad de cambio de idioma EN/ES mediante atributos `data-i18n`, el menú responsive para dispositivos móviles y el despliegue en GitHub Pages. A continuación se presenta la tabla de commits relacionados con la implementación durante este sprint.

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
|:-----------|:-------|:----------|:---------------|:--------------------|:--------------------|
| VitalTrek-Project/landing-page | feature/hero-navbar | a3f2c1e | feat(landing): add hero section with main CTA | Implements hero section with headline, subtitle and call-to-action button linking to registration. | 2026-04-15 |
| VitalTrek-Project/landing-page | feature/hero-navbar | b7d4e2a | feat(landing): add responsive navbar with mobile menu | Implements navigation bar with links to all sections and hamburger menu for mobile devices using toggleMobileMenu(). | 2026-04-15 |
| VitalTrek-Project/landing-page | feature/hero-navbar | c1a9f3d | style(landing): add CSS custom properties and base styles | Defines CSS variables for color palette (--navy-hero, --orange, --plan-card-bg) and global typography styles. | 2026-04-16 |
| VitalTrek-Project/landing-page | feature/benefits | d5e8b2f | feat(landing): add benefits section for tourists segment | Implements benefits cards section targeted at the tourist user segment with icons and descriptions. | 2026-04-17 |
| VitalTrek-Project/landing-page | feature/benefits | e2c7a4b | feat(landing): add benefits section for agency segment | Implements benefits cards section targeted at the agency administrator segment with icons and descriptions. | 2026-04-17 |
| VitalTrek-Project/landing-page | feature/benefits | f4d1c9e | feat(landing): add features section | Implements main platform features section with icon cards and brief descriptions of core functionalities. | 2026-04-18 |
| VitalTrek-Project/landing-page | feature/demo-offline | g8b3f2a | feat(landing): add demo and offline compatibility sections | Implements system demonstration section with mockup screenshots and offline compatibility info section. | 2026-04-19 |
| VitalTrek-Project/landing-page | feature/contact-security | h2e5d7c | feat(landing): add contact form with validation | Implements contact form with name, email and message fields and JavaScript validation for required fields and email format. | 2026-04-20 |
| VitalTrek-Project/landing-page | feature/contact-security | i9f4a1b | feat(landing): add data security section | Implements section communicating personal data protection measures to platform visitors. | 2026-04-20 |
| VitalTrek-Project/landing-page | feature/testimonials-team | j3c8e6d | feat(landing): add testimonials and team sections | Implements testimonials cards section with use cases and team presentation cards for all VitalTrek members. | 2026-04-21 |
| VitalTrek-Project/landing-page | feature/i18n | k7a2b5f | feat(landing): implement EN/ES language toggle | Implements bilingual support using data-i18n attributes and toggleLanguage() function with translations object for all text content. | 2026-04-22 |
| VitalTrek-Project/landing-page | feature/i18n | l1d9c3e | feat(landing): add translations object for all sections | Defines complete EN/ES translations object in JavaScript covering all text content across hero, benefits, features, demo, contact, testimonials and team sections. | 2026-04-22 |
| VitalTrek-Project/landing-page | feature/footer | m5f7b4a | feat(landing): add footer with navigation links and social media | Implements footer with navigation links, social media icons and contact information. | 2026-04-23 |
| VitalTrek-Project/landing-page | develop | n8e1d2c | style(landing): responsive adjustments for mobile and tablet | Applies media queries for breakpoints at 768px and 480px ensuring correct layout on mobile and tablet devices. | 2026-04-24 |
| VitalTrek-Project/landing-page | develop | o4b6f9a | fix(landing): fix mobile menu close behavior on link click | Fixes mobile menu not closing when a navigation link is clicked on small screens. | 2026-04-25 |
| VitalTrek-Project/landing-page | develop | p2c3e7d | fix(landing): fix language toggle not updating CTA buttons | Fixes toggleLanguage() not updating text content of CTA buttons in hero and navbar sections. | 2026-04-25 |
| VitalTrek-Project/landing-page | main | q6a8b1f | chore(deploy): configure GitHub Pages deployment | Configures GitHub Pages deployment from main branch and verifies correct rendering of all sections. | 2026-04-26 |
| VitalTrek-Project/landing-page | main | r3d5c4e | docs(landing): add README with project description and deploy URL | Adds README.md with project description, tech stack, local setup instructions and GitHub Pages URL. | 2026-04-26 |

---

### 5.2.1.5. Execution Evidence for Sprint Review

Durante el Sprint 1, el equipo completó la implementación de la Landing Page estática y bilingüe de VitalTrek. Se implementaron todas las secciones comprometidas en el Sprint Backlog: Hero con propuesta de valor y CTA, navegación responsive con toggle de idioma EN/ES, beneficios diferenciados por segmento (turistas y agencias), funcionalidades principales de la plataforma, demostración del sistema, compatibilidad offline, formulario de contacto con validación, medidas de seguridad de datos, testimonios y casos de uso, y sección del equipo. La landing page fue desplegada en GitHub Pages al cierre del sprint.

A continuación se presentan capturas de las principales vistas implementadas:

*(Insertar screenshot de la sección Hero)*

*(Insertar screenshot de la sección de Beneficios)*

*(Insertar screenshot de la sección de Funcionalidades)*

*(Insertar screenshot de la sección de Contacto)*

*(Insertar screenshot del toggle de idioma EN/ES)*

**Video de demostración:** *(Insertar enlace al video que ilustra la navegación completa de la landing page)*

---

### 5.2.1.6. Services Documentation Evidence for Sprint Review

Durante el Sprint 1, el alcance del equipo se limitó exclusivamente a la implementación de la Landing Page estática de VitalTrek, desarrollada con HTML, CSS y JavaScript vanilla. En esta iteración no se implementaron Web Services ni endpoints de API REST, por lo que no aplica documentación de servicios con OpenAPI para este sprint.

La implementación de endpoints y su documentación corresponderá a sprints posteriores, una vez que el equipo avance hacia el desarrollo de la Web Application y el Web Service de la plataforma.