![Logo de la UPC](../assets/imagenes-caratula//logo-upc.png)

# Universidad Peruana de Ciencias Aplicadas

# Ingeniería de Software

### Periodo: 2026-20 Pregrado

### Curso: Desarrollo de Soluciones IoT

### Código del Curso: 1ASI0572

### NRC: 8725

### Docente: León Baca, Marco Antonio

## Informe del Trabajo Final

### Startup: AgroLeak

### Producto: 

### Integrantes:

| Código | Apellidos y Nombres |
| :--- | :--- |
| U202516291 | Meza Tataje, David |
| U201611430 | Flores Manrique, Sebastian |
| U202117475 | Dueñas Canales, Leonardo Manuel |
| U201913639 | Palacios Jauregui, Kalid |
| U202222846 | Ramos Calagua, Sebastian Alexander|


### Agosto 2026-20

---

# Registro de Versiones del Informe

| Versión | Fecha | Autor | Descripción Modificada |
| :---: | :---: | :--- | :--- |
| 0.1 | 12/09/26 | Meza Tataje, David | Creación de la estructura base y primera versión del informe. |
|0.2 | 13/09/26 | Meza Tataje, David | Capítulo 1 y 2 añadido |
|0.3 | 14/09/26 | Dueñas Canales, Leonardo | Capítulo 3 añadido | 
|0.4 | 15/09/26 | Flores Manrique, Sebastian | Capítulo 4 añadido |
|0.5 | 16/09/26 | Palacios Jauregui, Kalid | Landing Page |
|0.6 | 30/09/26 |  Meza Tataje, David| Correción del capitulo 2 y 5 |
|0.7 | 30/09/26 |  Dueñas Canales, Leonardo| Correción del capitulo 3|
|0.8 | 30/09/26 |  Flores Manrique, Sebastian | Correción del capitulo 4|
|0.9 | 30/09/26 |  Ramos Calagua, Sebastian Alexander |Avance del capitulo 6|
|1.0 | 30/09/26 |  Palacios Jauregui, Kalid |Avance del capitulo 6|

---

# Project Report Collaboration Insights

- Link del repositorio del informe: [Repositorio del informe](https://github.com/upc-pre-202620-AgroLeak-Final-Project/Project-report)
- Link del repositorio del Landing Page: [Repositorio del Landing Page](https://github.com/upc-pre-202620-AgroLeak-Final-Project/Landing-page-AgroLeak)
- Link del repositorio del Backend / Web Services: [Repositorio del backend](https://github.com/upc-pre-202620-AgroLeak-Final-Project/AgroLeak-backend.git)
- Link del repositorio del Edge API / Embedded: []

A lo largo del proyecto, el equipo ha estado comprometido en la creación del informe en diferentes fases. Las tareas principales abarcan:
- Investigación de mercado y del dominio del negocio para la solución IoT.
- Redacción colaborativa de los capítulos en formato Markdown.
- Modelado de arquitectura de software (C4 Model), Domain-Driven Design y diseño de prototipo físico IoT.

---

# Contenido

## Tabla de contenidos

* [Student Outcome](#student-outcome)
* [Capítulo I: Introducción](#capítulo-i-introducción)
    * [1.1. Startup Profile](#11-startup-profile)
        * [1.1.1. Descripción de la Startup](#111-descripción-de-la-startup)
        * [1.1.2. Perfiles de integrantes del equipo](#112-perfiles-de-integrantes-del-equipo)
    * [1.2. Solution Profile](#12-solution-profile)
        * [1.2.1 Antecedentes y problemática](#121-antecedentes-y-problemática)
        * [1.2.2 Lean UX Process](#122-lean-ux-process)
            * [1.2.2.1. Lean UX Problem Statements](#1221-lean-ux-problem-statements)
            * [1.2.2.2. Lean UX Assumptions](#1222-lean-ux-assumptions)
            * [1.2.2.3. Lean UX Hypothesis Statements](#1223-lean-ux-hypothesis-statements)
            * [1.2.2.4. Lean UX Canvas](#1224-lean-ux-canvas)
    * [1.3. Segmentos objetivo](#13-segmentos-objetivo)
* [Capítulo II: Requirements Elicitation & Analysis](#capítulo-ii-requirements-elicitation--analysis)
    * [2.1. Competidores](#21-competidores)
        * [2.1.1. Análisis competitivo](#211-análisis-competitivo)
        * [2.1.2. Estrategias y tácticas frente a competidores](#212-estrategias-y-tácticas-frente-a-competidores)
    * [2.2. Entrevistas](#22-entrevistas)
        * [2.2.1. Diseño de entrevistas](#221-diseño-de-entrevistas)
        * [2.2.2. Registro de entrevistas](#222-registro-de-entrevistas)
        * [2.2.3. Análisis de entrevistas](#223-análisis-de-entrevistas)
    * [2.3. Needfinding](#23-needfinding)
        * [2.3.1. User Personas](#231-user-personas)
        * [2.3.2. User Task Matrix](#232-user-task-matrix)
        * [2.3.3. User Journey Mapping](#233-user-journey-mapping)
        * [2.3.4. Empathy Mapping](#234-empathy-mapping)
    * [2.4. Big Picture EventStorming](#24-big-picture-eventstorming)
    * [2.5. Ubiquitous Language](#25-ubiquitous-language)
* [Capítulo III: Requirements Specification](#capítulo-iii-requirements-specification)
    * [3.1. User Stories](#31-user-stories)
    * [3.2. Impact Mapping](#32-impact-mapping)
    * [3.3. Product Backlog](#33-product-backlog)
* [Capítulo IV: Solution Software Design](#capítulo-iv-solution-software-design)
    * [4.1. Strategic-Level Domain-Driven Design](#41-strategic-level-domain-driven-design)
        * [4.1.1. Design-Level EventStorming](#411-design-level-eventstorming)
        * [4.1.2. Context Mapping](#412-context-mapping)
        * [4.1.3. Software Architecture](#413-software-architecture)
    * [4.2. Tactical-Level Domain-Driven Design](#42-tactical-level-domain-driven-design)
* [Capítulo V: Solution UI/UX Design](#capítulo-v-solution-uiux-design)
    * [5.1. Style Guidelines](#51-style-guidelines)
    * [5.2. Information Architecture](#52-information-architecture)
    * [5.3. Landing Page UI Design](#53-landing-page-ui-design)
    * [5.4. Applications UX/UI Design](#54-applications-uxui-design)
    * [5.5. Applications Prototyping](#55-applications-prototyping)
    * [5.6. IoT Device Design](#56-iot-device-design)
* [Capítulo VI: Product Implementation, Validation & Deployment](#capítulo-vi-product-implementation-validation--deployment)
    * [6.1. Software Configuration Management](#61-software-configuration-management)
    * [6.2. Landing Page, Services & Applications Implementation](#62-landing-page-services--applications-implementation)
    * [6.3. Validation Interviews](#63-validation-interviews)
    * [6.4. Video About-the-Product](#64-video-about-the-product)
* [Conclusiones](#conclusiones)
* [Bibliografía](#bibliografía)
* [Anexos](#anexos)

---

# Student Outcome

**ABET - EAC - Student Outcome 5**
**Criterio:** La capacidad de funcionar efectivamente en un equipo cuyos miembros juntos proporcionan liderazgo, crean un entorno de colaboración e inclusivo, establecen objetivos, planifican tareas y cumplen objetivos.

En el siguiente cuadro se describe las acciones realizadas y enunciados de conclusiones por parte del grupo, que permiten sustentar el haber alcanzado el logro del ABET – EAC - Student Outcome 5.

| Criterio específico | Acciones realizadas | Conclusiones |
| :--- | :--- | :--- |
| **Trabaja en equipo para proporcionar liderazgo en forma conjunta** | **Meza Tataje, David**<br>*AV1*<br>Asumí el liderazgo en la definición de la arquitectura de software, guiando al equipo en la elaboración de los diagramas C4 Model y el diseño de nivel estratégico y táctico (DDD).<br><br>*TB1*<br>Asumí el liderazgo en la definición de la gestión de la configuración del software, estableciendo la estructuración de los entornos de desarrollo y las directrices para el control del código fuente de todo el equipo.<br><br>**Flores Manrique, Sebastian**<br>*AV1*<br>Lideré el diseño de la experiencia de usuario, definiendo las guías de estilo, la arquitectura de información y dirigiendo la implementación técnica de la primera versión funcional del Landing Page.<br><br>*TB1*<br>Lideré la consolidación del diseño de interfaces y experiencia de usuario de la solución, dirigiendo además la implementación técnica y el despliegue a producción de la primera versión de nuestras aplicaciones web frontend y del Landing Page.<br><br>**Dueñas Canales, Leonardo Manuel**<br>*AV1*<br>Encabecé la fase de investigación y elicitación, conduciendo el análisis competitivo, el proceso Lean UX y la estructuración del EventStorming junto con el equipo.<br><br>*TB1*<br>Dirigí la gestión ágil de la implementación del producto, encabezando la planificación del primer Sprint, la asignación de líderes de aspectos y colaboradores, y la estructuración de la pila de tareas (Backlog) a desarrollar.<br><br>**Palacios Jauregui, Kalid**<br>*AV1*<br>Dirigí la especificación de requisitos, estableciendo los estándares para la redacción de User Stories y liderando la priorización del Product Backlog para el MVP.<br><br>*TB1*<br>Encabecé la recopilación y estructuración técnica de las evidencias de desarrollo, pruebas, ejecución y documentación de servicios, garantizando la preparación integral para la revisión del Sprint.<br><br>**Ramos Calagua, Sebastian Alexander**<br>*AV1*<br>Asumí el liderazgo en la investigación preliminar de requerimientos físicos para IoT, evaluando la viabilidad de integración con nuestro ecosistema de software.<br><br>*TB1*<br>Dirigí la configuración y documentación del despliegue de software y estructuré las evidencias de dicho despliegue para asegurar la estabilidad de los pases a producción en los servicios implementados. | **AV1**<br>Durante la elaboración del informe AV1, demostramos un liderazgo compartido efectivo al distribuir la dirección de la investigación y diseño inicial según nuestras fortalezas técnicas. Esta delegación nos permitió profundizar en áreas complejas como el diseño IoT, la arquitectura de software y la implementación inicial del Landing Page, asegurando resultados de alta calidad.<br><br>**TB1**<br>Para esta entrega, el liderazgo compartido se adaptó a las altas exigencias de implementación técnica. La incorporación de un nuevo integrante nos permitió fortalecer áreas clave. Distribuimos la dirección para abarcar simultáneamente el diseño avanzado de interfaces, la gestión rigurosa de la configuración del código y la ejecución metodológica del primer Sprint, logrando desplegar con éxito nuestras aplicaciones web y servicios en la nube. |
| **Crea un entorno colaborativo e inclusivo, establece metas, planifica tareas y cumple objetivos.** | **Meza Tataje, David**<br>*AV1*<br>Planifiqué el flujo de control de versiones en GitHub para el informe y el código, estableciendo convenciones claras que facilitaron la integración del trabajo de todos los miembros sin conflictos.<br><br>*TB1*<br>Planifiqué y coordiné la actualización del registro de versiones del informe y los hallazgos de colaboración del equipo (Project Report Collaboration Insights), asegurando que los aportes se integren de forma cohesiva y cumplan las metas de la entrega.<br><br>**Flores Manrique, Sebastian**<br>*AV1*<br>Aseguré un entorno inclusivo al integrar principios de accesibilidad (a11y) en el Landing Page y coordiné el espacio de trabajo colaborativo en herramientas de diseño, permitiendo la revisión conjunta de los mock-ups.<br><br>*TB1*<br>Establecí las convenciones y guías de estilo para el código fuente, promoviendo un código limpio y estandarizado, y organicé sesiones de refactorización para lograr las versiones corregidas y mejoradas de los artefactos presentados previamente.<br><br>**Dueñas Canales, Leonardo Manuel**<br>*AV1*<br>Establecí las metas a corto plazo para la redacción del informe, organizando las sesiones de trabajo síncronas y consolidando los aportes individuales para asegurar la coherencia inicial del proyecto.<br><br>*TB1*<br>Facilité un entorno inclusivo al consolidar las retrospectivas del equipo para redactar las métricas de colaboración durante el Sprint, y establecí el cronograma para cumplir puntualmente con la fase de implementación, validación y despliegue del producto.<br><br>**Palacios Jauregui, Kalid**<br>*AV1*<br>Planifiqué y monitoreé las tareas del equipo utilizando herramientas de gestión ágil, asegurando que los objetivos de investigación, diseño y desarrollo web inicial se cumplieran dentro de los plazos establecidos.<br><br>*TB1*<br>Supervisé la actualización de la sección Student Outcome y establecí métricas de revisión cruzada para confirmar que las correcciones aplicadas a los artefactos de entregas anteriores cumplieran con los estándares de calidad esperados.<br><br>**Ramos Calagua, Sebastian Alexander**<br>*AV1*<br>Colaboré en la estructuración de la documentación inicial y establecí canales de comunicación técnica asíncrona para facilitar las decisiones arquitectónicas.<br><br>*TB1*<br>Trabajé activamente apoyando al equipo en la integración de la primera versión de las aplicaciones web frontend, garantizando que el entorno colaborativo se mantuviera enfocado y alineado con las metas de despliegue planificadas para este ciclo. | **AV1**<br>Logramos consolidar un entorno de trabajo altamente colaborativo, apoyándonos en herramientas en la nube y repositorios compartidos para mantener la visibilidad del progreso. La planificación estructurada de tareas y el establecimiento de hitos internos nos permitieron cumplir con todos los objetivos planteados para la fase inicial del proyecto.<br><br>**TB1**<br>En esta etapa, fortalecimos nuestro entorno colaborativo implementando convenciones formales de código y de gestión de configuración. Logramos cumplir todas las metas establecidas: desde la actualización y mejora sustancial de los artefactos previos, hasta la ejecución íntegra del primer Sprint con sus respectivas evidencias de pruebas y despliegue. Esta planificación conjunta unificó nuestro flujo de trabajo de manera transparente. |