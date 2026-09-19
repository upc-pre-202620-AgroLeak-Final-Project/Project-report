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
| U202117475 | Dueñas Canales, Leonardo Manuel |
| codigo3 | Integrante 3 |
| codigo4 | Integrante 4 |
| codigo5 | Integrante 5 |

### Agosto 2026-20

---

# Registro de Versiones del Informe

| Versión | Fecha | Autor | Descripción Modificada |
| :---: | :---: | :--- | :--- |
| 0.1 | 12/09/26 | Meza Tataje, David | Creación de la estructura base y primera versión del informe. |

---

# Project Report Collaboration Insights

- Link del repositorio del informe: [https://github.com/upc-pre-202620-AgroLeak-Final-Project/Project-report]
- Link del repositorio del Landing Page: [https://github.com/upc-pre-202620-AgroLeak-Final-Project/Landing-page-AgroLeak]
- Link del repositorio del Backend / Web Services: []
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
