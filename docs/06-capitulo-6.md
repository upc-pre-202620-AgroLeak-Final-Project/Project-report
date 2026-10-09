# Capítulo VI: Product Implementation, Validation & Deployment

## 6.1. Software Configuration Management

La gestión de la configuración del software (SCM) establece las prácticas, herramientas y convenciones que el equipo de AgroLeak emplea para garantizar la integridad, trazabilidad y calidad del código fuente a lo largo del ciclo de vida del desarrollo.

### 6.1.1. Software Development Environment Configuration

Para estandarizar el desarrollo y evitar discrepancias entre los equipos locales, se ha definido el siguiente entorno de desarrollo integrado:

*   **Editores e IDEs:** 
    *   IntelliJ IDEA y Visual Studio Code para el desarrollo del Backend modular (Java 21, Spring Boot 3.5).
    *   Visual Studio Code para el desarrollo del Frontend (Angular 20, TypeScript) y el Landing Page (HTML, CSS, JS).
*   **Gestión de Base de Datos:** DBeaver o pgAdmin para la administración de la base de datos relacional PostgreSQL y la ejecución de consultas.
*   **Contenedores y Virtualización:** Docker Desktop para orquestar el contenedor local de PostgreSQL y emular el entorno de persistencia.
*   **Pruebas de API:** Postman y Swagger/OpenAPI para el diseño, prueba y documentación de las colecciones de endpoints RESTful.
*   **Diseño de Arquitectura:** PlantUML y Structurizr para la generación de diagramas C4 Model.

### 6.1.2. Source Code Management

El control de versiones se gestiona centralizadamente utilizando Git y alojado en GitHub. Se ha adoptado el flujo de trabajo GitFlow para mantener un historial limpio y estructurado:

*   **Ramas Principales:**
    *   `main`: Contiene el código de producción estable. Solo recibe fusiones desde la rama de integración tras validar el despliegue.
    *   `develop`: Rama de integración principal donde convergen todas las nuevas características antes del lanzamiento.
*   **Ramas de Soporte:**
    *   `feature/[descripción]`: Para el desarrollo de nuevas historias de usuario.
    *   `bugfix/[descripción]`: Para la resolución de errores detectados.

### 6.1.3. Source Code Style Guide & Conventions

Para garantizar la legibilidad y mantenibilidad del código, el equipo se adhiere a las siguientes convenciones y guías de estilo:

*   **Convenciones de Commits:** Conventional Commits (ej. `feat(monitoring): agregar regla de anomalía`, `fix(ui): ajustar contraste de alerta`).
*   **Guías de Estilo por Lenguaje:**
    *   **Backend (Java):** Cumplimiento de las convenciones estándar de Java (PascalCase para clases, camelCase para métodos/variables). Estructuración basada en los principios de Domain-Driven Design (DDD), separando `application`, `domain/model`, `infrastructure` y `presentation/rest` en cada módulo.
    *   **Frontend (Angular/TypeScript):** Uso de componentes *standalone*, SCSS para estilos, y RxJS + Signals para la reactividad. Los componentes se organizan reflejando los *bounded contexts* del backend.
    *   **Base de datos:** Control de versiones del esquema y migraciones automatizadas gestionadas estrictamente a través de Flyway.

### 6.1.4. Software Deployment Configuration

La infraestructura de despliegue de AgroLeak está diseñada para separar claramente los entornos:

*   **Landing Page:** Despliegue estático automatizado a través de GitHub Pages desde la rama `main`.
*   **Frontend Web (Angular):** Compilación para producción (`npm run build:prod`) y despliegue en plataformas de nube (ej. Vercel o Netlify), configurando las variables de entorno para apuntar a la API productiva.
*   **Backend / Cloud API:** Alojamiento de los servicios API en proveedores cloud compatibles con PostgreSQL (ej. Railway, Neon, Supabase o Render) mediante conexión JDBC requerida con SSL, gestionando variables críticas (ej. `JWT_SECRET`, `DB_URL`) de forma segura.
*   **Edge Computing (IoT):** Los dispositivos en campo ejecutan almacenamiento local para conservar lecturas temporalmente, sincronizándose de manera idempotente con la nube al recuperar la conectividad.

---

## 6.2. Landing Page, Services & Applications Implementation

### 6.2.1. Sprint 1

#### 6.2.1.1. Sprint Planning 1

El Sprint 1 tiene como objetivo principal establecer la base estructural del proyecto AgroLeak. Esto incluye la configuración inicial de los repositorios, la implementación y despliegue del Landing Page para captación de prospectos (Hito BG02), la configuración de la base de datos PostgreSQL mediante migraciones y el desarrollo de los primeros endpoints de la API (Identity and Access Management).

*   **Fecha de inicio:** [31-08-2026]
*   **Fecha de fin:** [14-09-2026]
*   **Sprint Goal:** Desplegar el Landing Page público de AgroLeak y establecer la infraestructura base del backend para recibir telemetría y gestionar usuarios.

#### 6.2.1.2. Aspect Leaders and Collaborators

*   **David Meza:** Líder de Arquitectura y SCM.
*   **Sebastian Flores:** Líder de Diseño UX/UI y Frontend (Landing Page / Angular).
*   **Leonardo Dueñas:** Líder de Desarrollo Backend (Spring Boot / Arquitectura DDD).
*   **Kalid Palacios:** Líder de Requisitos (Scrum Master).
*   **Sebastian Ramos:** Líder de Validación, Base de datos (PostgreSQL/Flyway) y Testing.

#### 6.2.1.3. Sprint Backlog 1

| ID | User Story / Task | Asignado a | Estado |
| :--- | :--- | :--- | :--- |
| EP01-US01 | Browse the Public Website | Sebastian Flores | Terminado |
| EP01-US02 | Request a Product Demonstration | Sebastian Flores | Terminado |
| EP02-US03 | Sign In to the Platform | Leonardo Dueñas | Terminado |
| TS01 | Receive Device Telemetry through the Edge API | Sebastian Ramos | Terminado |
| Tarea | Configuración de Repositorios y CI/CD | David Meza | Terminado |

#### 6.2.1.4. Development Evidence for Sprint Review

<img src="https://i.postimg.cc/vTkrhYcd/image.png" alt="angular" width="100%">> 

#### 6.2.1.5. Testing Suite Evidence for Sprint Review

Se implementaron pruebas automatizadas para asegurar la estabilidad de las entregas del Sprint 1, utilizando **JUnit** y **Mockito** para el backend, además de **MockMvc** y **H2** para las pruebas de integración en memoria.

#### 6.2.1.6. Execution Evidence for Sprint Review

<img src="https://i.postimg.cc/44Vxx41k/image.png" alt="landing page" width="100%">> 

#### 6.2.1.7. Services Documentation Evidence for Sprint Review

La documentación de los servicios expuestos se generó de manera automatizada utilizando **Swagger / OpenAPI** interactivo (`/swagger-ui/index.html`), garantizando que el equipo de frontend tenga contratos claros para el consumo de la API, incluyendo la autenticación JWT.

<img src="https://i.postimg.cc/7P3qysqF/Whats-App-Image-2026-10-08-at-7-52-07-PM.jpg" alt="swagger" width="100%">> 

#### 6.2.1.8. Software Deployment Evidence for Sprint Review

El Landing Page y los servicios básicos fueron desplegados con éxito en sus respectivos entornos cloud.

*   **URL del Landing Page (GitHub Pages):** `https://upc-pre-202620-agroleak-final-project.github.io/Landing-page-AgroLeak/`
*   **URL de la API (Cloud):** `[Insertar URL de la API]`

#### 6.2.1.9. Team Collaboration Insights during Sprint

Durante el Sprint 1, el equipo mantuvo una comunicación constante a través de reuniones diarias (Daily Standups) y el uso de tableros ágiles (ej. GitHub Projects). La división de tareas según las fortalezas técnicas permitió avanzar en paralelo: mientras se estructuraba el diseño visual y la web responsiva en Angular, el equipo de backend consolidaba las migraciones Flyway y la autenticación JWT en Spring Boot. La integración del trabajo se logró sin conflictos mayores gracias a las políticas estrictas de revisión de Pull Requests.

---

## 6.3. Validation Interviews

El Needfinding organiza los hallazgos disponibles sobre la supervisión del riego y la sanidad vegetal. Su base empírica son los resúmenes de las entrevistas registradas en la sección 2.2.2: **Michael Quispe (Segmento 1)**, y **Alexis Alarcón e Ing. Vega (Segmento 2)**. La muestra disponible es **n = 3**; si bien aporta perspectivas complementarias desde el trabajo de campo y la administración, no permite afirmar que los hallazgos representen estadísticamente a todos los integrantes de los dos segmentos objetivo.

**Alcance y criterio de evidencia.** Se revisaron los capítulos del informe, los assets existentes y la rama `ENTREVISTAS`, que contiene los registros documentales. Las preguntas de 2.2.1 y las hipótesis del capítulo I no se tratan como respuestas de participantes.

Se distinguen tres niveles: **E** = evidencia explícita en el resumen; **I** = interpretación del equipo, pendiente de contrastación; **N/D** = información no documentada. Las prioridades de diseño y las emociones inferidas se identifican como I. No se asignan puntuaciones cuantitativas cuando la entrevista no las proporciona.

### 6.3.1. Diseño de Entrevistas

AgroLeak es una plataforma integral de monitoreo agrícola diseñada para proporcionar detección temprana de fugas de agua y confirmación visual de plagas mediante Inteligencia Artificial en el borde (Edge Computing), enfocándose en la intervención oportuna a través de alertas y actuación física remota. 

Para validar la viabilidad de esta solución, se diseñó un cuestionario estructurado orientado a descubrir los puntos de dolor actuales (pain points) en la operación en campo y medir la receptividad de los usuarios frente a la tecnología propuesta.

**Preguntas para la Entrevista:**

1.  **Contexto Operativo:** ¿Cómo realizan actualmente los recorridos diarios para monitorear el estado del caudal y las líneas de los sistemas de riego?
2.  **Percepción del Riesgo:** ¿Cuánto tiempo suele pasar desde que ocurre una fuga de agua (o desacople de manguera) hasta que alguien se da cuenta, y qué impacto genera esto?
3.  **Gestión de Plagas:** Hoy en día, ¿qué método utilizan para la inspección y confirmación temprana de plagas en las hojas de los cultivos?
4.  **Recepción Tecnológica (Fugas):** ¿De qué manera te facilitaría el trabajo contar con un sistema que te alerte en el celular en el momento exacto en que ocurre una anomalía de caudal, permitiéndote cerrar la válvula de forma remota?
5.  **Recepción Tecnológica (IA):** ¿Consideras útil que una cámara instalada en campo tome fotos y una inteligencia artificial te envíe una alerta con la imagen si detecta un insecto objetivo, antes de que tengas que ir a revisar físicamente?
6.  **Control y Seguridad:** ¿Qué nivel de confianza te genera que el sistema requiera siempre tu validación humana antes de tomar decisiones críticas (como un cierre de válvula o un reporte de plaga confirmada)?
7.  **Valor Percibido:** En resumen, viendo los problemas operativos actuales, ¿consideras que un kit tecnológico como AgroLeak es viable de implementar y necesario para mejorar la eficiencia del fundo?

### 6.3.2. Registro de Entrevistas

**Segmento 1: Pequeños y medianos agricultores tecnificados**

**Entrevista 1**
*   **Nombres y Apellidos:** Michael Quispe
*   **Edad:** 24 años
*   **Lugar de Residencia:** Cañete, Lima
*   **Ocupación:** Asistente Técnico de Riego
*   **URL:** [entrevista-michael.mp4](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202222846_upc_edu_pe/IQCAaAcW1oK_Tqof8YVhn2hPAeoTG09J7UKSdoKXZTXxL40?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=cwsQ3o)
*   **Resumen de Validación:** El usuario validó la necesidad urgente de automatizar la detección de fugas, indicando que actualmente dependen de recorridos físicos que retrasan la respuesta, lo que genera desperdicio de agua y daño al cultivo. Confirmó que la propuesta de recibir alertas móviles, evidencias fotográficas y opciones de cierre remoto reduciría significativamente el tiempo de reacción, validando la viabilidad y necesidad del proyecto AgroLeak en campo.

**Segmento 2: Jefes de Operaciones Agrícolas y Administradores de Fundo**

**Entrevista 2**
*   **Nombres y Apellidos:** Alexis Alarcón Vargas
*   **Edad:** 32 años
*   **Lugar de Residencia:** Cañete, Lima
*   **Ocupación:** Jefe de Operaciones Agrícolas
*   **URL:** [entrevista-sector-2.mp4](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202516291_upc_edu_pe/IQBUZID357uxQYUte2Gb4geMARDM9A0AdXGqjCBTxWvffuV?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=Lhg1P9)
*   **Resumen de Validación:** Destacó que la falta de información en tiempo real retrasa la detección de errores y roturas. Considera absolutamente necesarios los *interlocks* para validar la persistencia de una anomalía y solicitar autorizaciones con credenciales antes de abrir válvulas tras una inspección. Valoró positivamente que la IA envíe alertas fotográficas con porcentajes de certeza, lo que podría reducir el uso de fitosanitarios. 

### 6.3.3. Evaluaciones según heurísticas

Dado que el proyecto se encuentra en una fase de validación de concepto y viabilidad técnica, las heurísticas de usabilidad (Jakob Nielsen) se proyectaron sobre los requerimientos y el comportamiento esperado del sistema IoT. Las principales directrices validadas con los usuarios para el diseño fueron:

1.  **Visibilidad del estado del sistema:** El sistema deberá informar siempre de forma proactiva al usuario a través del móvil (alertas en tiempo real) y de forma física (indicadores LED en la caja IoT en campo), eliminando la incertidumbre sobre el flujo del riego.
2.  **Relación entre el sistema y el mundo real:** Validado al utilizar lenguaje agronómico cotidiano en las entrevistas (válvulas, presión, anomalía de caudal, evapotranspiración) en lugar de jerga de software, lo que asegura que la interfaz final será intuitiva.
3.  **Control y libertad del usuario (Prevención de errores):** Validado como un requisito crítico por ambos perfiles. Las entrevistas confirmaron que los técnicos necesitan modos operativos seguros (ej. requerir confirmación manual obligatoria para el cierre remoto de válvulas) para evitar bloqueos automáticos accidentales.
4.  **Reconocer en lugar de recordar:** En el circuito de monitoreo de plagas, la plataforma debe enviar la evidencia visual (fotografía capturada) junto con el porcentaje de confianza de la IA directamente en la alerta. Así, el agricultor valida la información viendo la imagen de la hoja afectada, sin depender de descripciones textuales.

---

## 6.4. Video About-the-Product

En esta sección se presenta el material audiovisual desarrollado para comunicar de forma clara y directa la propuesta de valor de AgroLeak a los segmentos objetivo (agricultores tecnificados y jefes de fundo). El video resume el problema de la ineficiencia hídrica y fitosanitaria, y demuestra cómo el kit IoT de ciclo cerrado y el dashboard web/móvil resuelven estas deficiencias.

*   **Plataforma de alojamiento:** YouTube
*   **Enlace al video About-the-Product:** `[Insertar enlace de YouTube aquí]`

> [Insertar miniatura o captura representativa del video de YouTube]
