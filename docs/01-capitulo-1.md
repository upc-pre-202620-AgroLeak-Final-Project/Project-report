<div style="page-break-before: always;"></div>

# Capítulo I: Introducción

En este capítulo se presenta la información general de AgroLeak como startup de base tecnológica, incluyendo su descripción, misión, visión y los perfiles de los integrantes del equipo. Asimismo, se expone el perfil de la solución propuesta, que abarca el análisis de antecedentes y la problemática identificada mediante la técnica de las 5 W's y 2 H's, el desarrollo completo del proceso Lean UX y la caracterización detallada de los segmentos objetivo.

---

## 1.1. Startup Profile

### 1.1.1. Descripción de la Startup

AgroLeak es una startup peruana de tecnología agrícola (AgTech) fundada por un equipo de estudiantes de Ingeniería de Software de la Universidad Peruana de Ciencias Aplicadas (UPC). Nace como respuesta a dos problemáticas críticas en el sector agrario: las elevadas pérdidas de agua por ineficiencias y fugas en los sistemas de riego tecnificado, y la detección tardía de plagas que afectan la productividad de los cultivos.

La startup integra componentes físicos de Internet de las Cosas (sensores de caudal por pulsos a la entrada y salida de cada sector, microcontroladores ESP32 y una cámara ESP32-S3 con inteligencia artificial), servicios en la nube con procesamiento en el borde (Edge Computing) y modelos de visión por computador. Esta combinación permite ofrecer una plataforma accesible de monitoreo en tiempo real que detecta anomalías hídricas, actúa sobre la válvula de corte del sector con salvaguardas de seguridad y genera alertas tempranas ante la presencia de plagas foliares.

| Misión | Visión |
| :--- | :--- |
| Empoderar a los agricultores y gestores de riego con soluciones IoT e Inteligencia Artificial accesibles, permitiéndoles monitorear de forma continua sus redes de distribución hídrica y detectar plagas a tiempo para reducir pérdidas y promover una gestión agrícola eficiente, sostenible y rentable. | Ser la plataforma IoT de monitoreo hídrico y analítica agrícola líder en América Latina, impulsando la transformación digital y la sostenibilidad en el sector agropecuario mediante tecnología innovadora de bajo costo. |

---

### 1.1.2. Perfiles de integrantes del equipo

| Fotografía | Integrantes del equipo | Código de estudiante | Carrera | Conocimientos / Habilidades |
| :---: | :--- | :---: | :---: | :--- |
| <img src="../assets/Foto-Kalid.jpg" width="100" alt="Kalid Palacios"> | Palacios Jauregui, Kalid | U201913639 | Ingeniería de Software | Estudiante de Ingeniería de Software con conocimientos en C++, HTML, CSS y JavaScript, así como en herramientas de desarrollo de software. Aporta al equipo en el desarrollo web y continúa fortaleciendo sus habilidades de programación.|
|<img src="../assets/Foto-Leonardo.png" width="100" alt="Leonardo Dueñas">| Dueñas Canales, Leonardo Manuel | U202117475 | Ingeniería de Software | Estudiante de 7° ciclo. Cuenta con experiencia en desarrollo backend con Java y Spring Boot, así como en diseño de arquitecturas de software utilizando C4 Model y Structurizr. Posee conocimientos en bases de datos relacionales (PostgreSQL, MySQL), Docker y despliegue en la nube. Familiarizado con marcos de trabajo ágiles y control de versiones con Git/GitHub. |
| <img src="../assets/Foto-Sebastian.jpeg" width="100" alt="Sebastian Flores"> | Flores Manrique, Sebastian Enrique | U201611430 | Ingeniería de Software | Estudiante de séptimo ciclo de Ingeniería de Software. Tiene conocimientos en C++ y Python y experiencia en desarrollo frontend y backend. Se caracteriza por ser responsable y por apoyar al equipo en lo que haga falta.|
| <img src="../assets/Foto-David.jpg" width="100" alt="David Meza"> | **Meza Tataje, David** | U202516291 | Ingeniería de Software | Estudiante de Ingeniería de Software de 21 años, con conocimientos intermedios en C++, Java y C#, además de experiencia en el desarrollo de aplicaciones web con HTML, CSS, JavaScript y SQL. Se considera una persona colaboradora y responsable, siempre dispuesto a aprender y trabajar en equipo para lograr los objetivos del proyecto. |
| <img src="https://i.postimg.cc/8ktyLZj4/Sebastian-Ramos-foto-perfil.jpg" width="100" alt="Sebastian Ramos"> | **Ramos Calagua, Sebastian Alexander** | U202222846 | Ingeniería de Software | Estudiante de Ingeniería de Software de 23 años. Se desempeña como Analista Programador, con experiencia en desarrollo backend con C# y .NET, automatización con Python y aplicaciones con Flutter. Maneja bases de datos en SQL Server, diseño de arquitectura con C4 Model (PlantUML, Structurizr) y control de versiones con Git/GitHub. Se orienta a la creación de APIs eficientes y al trabajo colaborativo. |


## 1.2. Solution Profile

### 1.2.1. Antecedentes y problemática

El sector agrícola peruano es uno de los motores económicos más importantes del país. Según datos del Ministerio de Desarrollo Agrario y Riego (MIDAGRI), la agricultura representa cerca del 75 % de la demanda consuntiva de agua a nivel nacional. Sin embargo, la eficiencia en la conducción y distribución del recurso hídrico en parcelas tecnificadas es baja: se estima que entre el 20 % y el 40 % del agua se pierde debido a fugas no detectadas, roturas de mangueras, desacoples o desajustes de presión. A esta ineficiencia hídrica se suma el impacto de las plagas y enfermedades foliares que, al ser identificadas de manera tardía mediante recorridos visuales esporádicos, causan reducciones de hasta un 30 % en el rendimiento de los cultivos.

Investigaciones e informes internacionales de la FAO y la CEPAL señalan que la falta de herramientas tecnológicas accesibles en el campo incrementa los costos operativos y el tiempo dedicado a inspecciones manuales. Por otro lado, la infraestructura de conectividad en zonas rurales ha mejorado sustancialmente: según OSIPTEL (2024), el acceso a internet en hogares rurales del Perú alcanzó cerca del 83 %, creando el contexto ideal para el despliegue de soluciones basadas en Internet de las Cosas (IoT) y aplicaciones web responsive.

Aplicando la técnica de las 5 W's y 2 H's (Who, What, Where, When, Why, How, How Much), se identificaron los siguientes aspectos clave del problema:

> **Who (¿Quién?):** Los principales afectados son los pequeños y medianos agricultores tecnificados que administran parcelas de cultivo, así como los jefes de operaciones y administradores de fundo encargados del control de riego y sanidad vegetal.

> **What (¿Qué?):** La ineficiencia en la detección oportuna de anomalías hidráulicas (fugas y obstrucciones) y la falta de supervisión continua de plagas en el cultivo, lo que genera desperdicio masivo de agua, sobrecostos energéticos en bombeo y pérdida de cosechas.

> **Where (¿Dónde?):** En las redes de conducción de riego tecnificado (tuberías y mangueras de goteo/aspersión) y en las zonas foliares de los cultivos ubicados en valles agrícolas del Perú.

> **When (¿Cuándo?):** Ocurre de manera continua durante los turnos de bombeo y a lo largo de las etapas de desarrollo vegetativo de la planta, agravándose cuando los incidentes suceden en horarios nocturnos o sectores alejados.

> **Why (¿Por qué?):** Debido a la dependencia exclusiva de inspecciones físicas visuales y a la ausencia de un sistema IoT económico que combine monitoreo de flujo diferencial y cámaras inteligentes con procesamiento en el borde (Edge Computing).

> **How (¿Cómo?):** Se aborda mediante el desarrollo de AgroLeak, un kit IoT compuesto por sensores de caudal por pulsos a la entrada y salida de cada sector, una válvula de corte con modos de operación seguros, una cámara ESP32-S3 con un modelo de visión por computador y una plataforma web y móvil conectada a un RESTful API.

> **How Much (¿Cuánto?):** En los fundos, el bombeo representa entre el 15 % y el 25 % del costo operativo, y cada fuga no detectada aumenta ese gasto, además del agua y los fertilizantes perdidos; en las parcelas pequeñas, las pérdidas de agua pueden llegar al 40 %. AgroLeak propone un kit de hardware de bajo costo con una suscripción SaaS mensual o por hectárea.

**Puntos clave que debe resolver la solución**

1. Detectar en minutos, y no en horas, una diferencia persistente entre el caudal que entra y el que sale de un sector de riego.
2. Permitir actuar sobre la válvula del sector con salvaguardas: confirmar que la anomalía persiste, elegir entre actuación manual o automática y exigir autorización para la reapertura.
3. Alertar sobre plagas con evidencia fotográfica para realizar aplicaciones focalizadas.
4. Registrar las incidencias y las acciones realizadas para sustentar auditorías y certificaciones.

**Objetivo general**

Desarrollar una solución IoT de bajo costo que detecte fugas en sectores de riego tecnificado y plagas foliares, y que permita actuar sobre la válvula del sector de forma segura y trazable.

**Objetivos específicos**

1. Implementar el monitoreo del caudal de entrada y salida de cada sector mediante sensores de pulso y microcontroladores ESP32.
2. Detectar anomalías persistentes de caudal y notificarlas en tiempo real en la aplicación web y móvil.
3. Permitir el cierre de la válvula del sector en tres modos de operación: solo monitoreo, manual y automático protegido.
4. Registrar observaciones de plagas capturadas por una cámara ESP32-S3, con su nivel de confianza.
5. Mantener una bitácora de incidencias y de acciones sobre las válvulas.

**Restricciones y alcance**

- El MVP se limita a sectores de riego por goteo; el riego por aspersión y las redes troncales quedan fuera del alcance.
- La validación técnica se realiza con un prototipo físico a escala (maqueta hidráulica con mini bomba), no en un fundo en operación.
- Los sensores de bajo costo tienen una precisión limitada, por lo que la detección se basa en una diferencia mínima de caudal sostenida en el tiempo y no en lecturas aisladas.
- La detección de plagas se limita a un conjunto de plagas objetivo y no reemplaza la evaluación del agrónomo.
- El desarrollo se realiza en un ciclo académico de tres sprints con un equipo de cinco integrantes.

---

### 1.2.2. Lean UX Process

#### 1.2.2.1. Lean UX Problem Statements

The current state of **irrigation and crop health management in small and medium tech-enabled farms in Peru** has focused mainly on **tech-enabled farmers and farm operations managers who detect leaks, pipe breaches and pests through manual field walks and paper or spreadsheet records, which delays their response by hours or days and wastes water, pumping energy and inputs**.

What existing products/services fail to address is **an affordable solution that continuously compares the water entering and leaving each irrigation sector, detects leaks and pests in real time, and lets users act on the sector valve safely, without the cost and complexity of industrial telemetry or the limits of satellite-only analytics**.

Our product/service will address this gap by **providing AgroLeak, a low-cost IoT kit with inflow and outflow pulse flow sensing, a shutoff valve with safe operation modes, an AI camera for pest detection, and a responsive web and mobile platform with real-time alerts and an audit log**.

Our initial focus will be **small and medium tech-enabled farmers and farm operations managers in the coastal valleys of Peru who use drip irrigation**.

We'll know we are successful when we see **a 50% reduction in the average time to detect irrigation leaks, an early pest detection accuracy above 85%, and over 70% of generated alerts acknowledged by users through the platform**.

---

#### 1.2.2.2. Lean UX Assumptions

##### Business Assumptions
1. Creemos que existe una demanda creciente en el sector agrícola por soluciones tecnológicas accesibles enfocadas en la eficiencia hídrica y la protección fitosanitaria.
2. Creemos que un modelo de negocio híbrido basado en la venta/alquiler del kit hardware IoT junto a una suscripción SaaS por analítica en la nube es viable y sostenible.
3. Creemos que utilizar hardware de bajo costo (microcontroladores ESP32, sensores de caudal por pulsos y cámaras ESP32) reducirá las barreras de adopción frente a competidores industriales.
4. Creemos que la trazabilidad de datos y el control humano sobre acciones críticas generarán confianza en los usuarios agrícolas.

##### Business Outcome Assumptions
1. Lograremos una tasa de conversión del 20 % de usuarios piloto hacia planes de suscripción pagados en los primeros 6 meses.
2. Mantendremos una tasa de cancelación (churn rate) inferior al 5 % mensual ofreciendo un valor cuantificable en ahorro de agua y energía.
3. Estableceremos alianzas estratégicas con al menos 2 empresas integradoras de riego local en el primer año.

##### User Assumptions
1. Los agricultores y jefes de fundo cuentan con smartphones o computadoras con conexión a internet para revisar notificaciones.
2. Los usuarios prefieren recibir alertas fotográficas e indicadores de caudal en tiempo real en su teléfono móvil antes que realizar recorridos extensos.
3. Los administradores aceptarán que el sistema cierre la válvula del sector y apague la bomba ante fugas críticas, siempre que la anomalía sea persistente, puedan elegir el modo manual y la reapertura requiera su autorización.
4. Los usuarios confiarán en la plataforma si la interfaz es intuitiva y muestra estados claros e información visual.

##### User Outcome and Benefit Assumptions
1. Los agricultores reducirán drásticamente el tiempo operativo dedicado a la inspección física de mangueras y tuberías.
2. Los usuarios obtendrán un ahorro cuantificable en los recibos de energía eléctrica o combustible asociados al bombeo.
3. Los productores protegerán la salud de sus cultivos al detectar focos de plagas en fases iniciales.
4. Los gestores obtendrán tranquilidad al disponer de supervisión y registros históricos las 24 horas del día.

##### Feature Assumptions
1. Creemos que un sistema de sensado diferencial de caudal por pulsos (entrada y salida) identificará fugas en tramos específicos con alta precisión.
2. Creemos que un módulo de cámara con un modelo de visión por computador identificará plagas foliares objetivo reduciendo falsos positivos.
3. Creemos que una válvula de corte accionada por servo, con modos de operación (solo monitoreo, manual y automático protegido), detendrá el paso del agua al sector y apagará la bomba de forma segura ante una anomalía persistente de caudal.
4. Creemos que un dashboard web y móvil responsive facilitará la visualización gráfica de métricas, historial de alertas y fotos capturadas.

---

#### 1.2.2.3. Lean UX Hypothesis Statements

1. **Hypothesis 1 (Dual Pulse Flow Sensing Feature):**
   We believe we will achieve **a 50% reduction in water volume lost during leakage events** if **tech-enabled farmers** attain **immediate detection and localized identification of hydraulic breaches** with **a dual pulse-flow sensing IoT node based on ESP32**.

2. **Hypothesis 2 (Camera Pest Detection Feature):**
   We believe we will achieve **a 30% reduction in crop losses caused by pests** if **farm managers and agronomists** attain **early visual identification of target pests on crop leaves** with **ESP32-S3 AI camera that runs a vision model in the field**.

3. **Hypothesis 3 (Safe Shutoff Valve Feature):**
   We believe we will achieve **higher user trust and lower water and energy losses during leak events** if **farm operations managers** attain **safe and traceable protection of their irrigation sectors** with **a servo-actuated shutoff valve that closes the sector and stops the pump only when a flow anomaly persists, with manual and protected automatic modes and authorized reopening**.

4. **Hypothesis 4 (Real-time Responsive Dashboard Feature):**
   We believe we will achieve **an active monthly platform adoption rate above 70%** if **farmers and farm leads** attain **real-time visibility of water flow metrics, alert history, and pest photos from any web browser or mobile device** with **a responsive web/mobile dashboard integrated with backend RESTful APIs**.

---

#### 1.2.2.4. Lean UX Canvas

A continuación se presenta la representación estructurada del **Lean UX Canvas** diseñado para la solución AgroLeak. El lienzo gráfico interactivo ha sido elaborado en la herramienta colaborativa **Miro** y se incluye su visualización centralizada:

![Lean UX Canvas](../assets/lean-ux-canvas.png)

*Figura 1.1. Lean UX Canvas para la plataforma AgroLeak.*

---

## 1.3. Segmentos objetivo

AgroLeak ha sido diseñada considerando la diversidad de actores en el sector agrícola tecnificado del Perú. A partir del análisis del dominio del problema, se identificaron dos segmentos objetivo principales con necesidades y características diferenciadas:

### Segmento 1: Pequeños y Medianos Agricultores Tecnificados
Este segmento agrupa a productores agrícolas independientes que han implementado sistemas de riego por goteo o aspersión en parcelas de mediano o pequeño tamaño para cultivos de valor comercial (frutales, hortalizas, legumbres).

**Características demográficas:**
* **Ubicación:** Perú, principalmente en valles agrícolas de la costa (Ica, La Libertad, Piura, Lambayeque) y valles interandinos.
* **Género:** Femenino y masculino.
* **Edad:** Entre 20 y 60 años
* **Ocupación:** Agricultores independientes, propietarios o arrendatarios de terrenos agrícolas de 5 a 50 hectáreas, y el personal técnico de riego que trabaja en estas parcelas
* **Nivel socioeconómico:** NSE C y D+ en zonas rurales y periurbanas.
* **Nivel tecnológico:** Usuarios habituales de smartphones con acceso a aplicaciones móviles (WhatsApp) e internet móvil.

**Datos estadísticos de sustento:**
* Según el Instituto Nacional de Estadística e Informática (INEI), la agricultura familiar tecnificada representa un sector clave en el país, donde más del 85 % de las unidades agropecuarias poseen menos de 10 hectáreas.
* Datos del MIDAGRI señalan que la falta de monitoreo continuo en redes de riego provoca pérdidas de agua de hasta un 40 %, afectando directamente los ingresos del pequeño productor.
* OSIPTEL (2024) confirma que la penetración de internet rural se encuentra cercana al 83 %, lo que permite el envío de notificaciones y alertas en tiempo real a los dispositivos móviles de los agricultores.

---

### Segmento 2: Jefes de Operaciones Agrícolas y Administradores de Fundo
Este segmento comprende a profesionales, ingenieros agrónomos y técnicos encargados de la gestión operativa, la programación de turnos de riego, el control de costos energéticos y la sanidad vegetal en agroempresas y fundos de mayor escala.

**Características demográficas:**
* **Ubicación:** Perú, en centros de producción agroindustrial y fundos exportadores.
* **Género:** Femenino y masculino.
* **Edad:** Entre 25 y 55 años.
* **Ocupación:** Jefes de fundo, administradores agrícolas, supervisores de riego tecnificado o ingenieros de sanidad vegetal.
* **Nivel de educación:** Educación superior técnica o universitaria completa (Agronomía, Ingeniería Agrícola, Ingeniería Industrial).
* **Nivel socioeconómico:** NSE B y C.
* **Nivel tecnológico:** Alto; habituados al uso de software de gestión, hojas de cálculo, sistemas de analítica y paneles de supervisión.

**Datos estadísticos de sustento:**
* En fundos agroindustriales, el costo de energía eléctrica o combustible para estaciones de bombeo representa entre el 15 % y 25 % del costo operativo total de producción.
* La detección tardía de brotes de plagas incrementa hasta en un 40 % los gastos en plaguicidas agroquímicos, mientras que un monitoreo fotográfico temprano permite aplicaciones focalizadas y un control fitosanitario más eficiente.
