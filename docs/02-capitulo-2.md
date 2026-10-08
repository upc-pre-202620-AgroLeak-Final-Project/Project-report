<div style="page-break-before: always;"></div>

# Capítulo II: Requirements Elicitation & Analysis

En este capítulo se presenta la investigación de requisitos y el análisis del dominio para el desarrollo de AgroLeak. Se incluye el estudio comparativo de competidores en el mercado AgTech, el diseño y registro de entrevistas a profundidad con representantes de los segmentos objetivo, el proceso de Needfinding (User Personas, Task Matrix, Journey Maps y Empathy Maps), el modelado del negocio mediante Big Picture EventStorming y la definición del lenguaje ubicuo.

---

## 2.1. Competidores

En esta sección se analiza el panorama competitivo de las soluciones tecnológicas orientadas al monitoreo de riego, gestión hídrica y detección de amenazas en cultivos. El análisis permite identificar las principales características, fortalezas, debilidades y vacíos de las alternativas existentes en el mercado, con el propósito de determinar las oportunidades de diferenciación para AgroLeak como un kit IoT de ciclo cerrado accesible con IA en el borde.

### 2.1.1. Análisis competitivo

#### Competitive Analysis Landscape

<table border="1" cellspacing="0" cellpadding="7" width="100%">

<tr>
<th colspan="6" align="left">
Competitive Analysis Landscape
</th>
</tr>

<tr>
<th colspan="2" rowspan="2" align="left" valign="middle">
¿Por qué realizar este análisis?
</th>

<th colspan="4" align="left">
Escriba en el recuadro la pregunta que busca responder o el objetivo de este análisis.
</th>
</tr>

<tr>
<td colspan="4" align="left">
El objetivo del análisis es identificar las brechas existentes entre las plataformas de telemetría industrial de alto costo y las herramientas de monitoreo satelital, reconociendo oportunidades de diferenciación que posicionen a AgroLeak como un kit IoT accesible, de ciclo cerrado y con procesamiento en el borde (detección diferencial de caudal y visión por computador para plagas) para pequeños y medianos agricultores del Perú.
</td>
</tr>

<tr>

<th colspan="2" align="left" valign="middle">
(En la cabecera colocar por cada competidor nombre y logo)
</th>

<th align="center" valign="middle">
AgroLeak
<br><br>
<img src="../assets/agroleak-logo.png" width="85" alt="AgroLeak Logo">
</th>

<th align="center" valign="middle">
DropControl (WiseConn)
<br><br>
<img src="../assets/logo-dropcontroll.jpg" width="85" alt="DropControl Logo">
</th>

<th align="center" valign="middle">
CropX
<br><br>
<img src="../assets/cropx.jpg" width="85" alt="CropX Logo">
</th>

<th align="center" valign="middle">
Kilimo
<br><br>
<img src="../assets/kilimo-logo-jpg.png" width="85" alt="Kilimo Logo">
</th>

</tr>

<tr>

<th rowspan="2" align="center" valign="top">
Perfil
</th>

<th align="center" valign="middle">
Overview
</th>

<td valign="top">
Sistema IoT de ciclo cerrado con sensado diferencial de caudal, cámara IoT con visión artificial en el borde y corte automático por relé para prevención de fugas y plagas.
</td>

<td valign="top">
Sistema industrial de telemetría y automatización de riego por radiofrecuencia y la nube para grandes operaciones agrícolas.
</td>

<td valign="top">
Plataforma de monitoreo agronómico basada en sensores de suelo, datos meteorológicos e integración satelital para optimizar el riego.
</td>

<td valign="top">
Plataforma SaaS de gestión de riego basada en imágenes satelitales y datos agrometeorológicos sin necesidad de hardware en campo.
</td>

</tr>

<tr>

<th align="center" valign="middle">
Ventaja competitiva
</th>

<td valign="top">
Solución híbrida accesible (agua + sanidad vegetal) con actuación física de salvaguarda y procesamiento en el borde (Edge AI).
</td>

<td valign="top">
Alta precisión industrial, robustez en hardware de campo y amplia capacidad de automatización de válvulas en grandes extensiones.
</td>

<td valign="top">
Gran capacidad de integración de datos multi-fuente (suelo, clima, satélite) y algoritmos avanzados de recomendación de riego.
</td>

<td valign="top">
Cero costo de instalación de hardware y fácil escalabilidad en grandes superficies agrícolas mediante analítica satelital.
</td>

</tr>

<tr>

<th rowspan="2" align="center" valign="top">
Perfil de Marketing
</th>

<th align="center" valign="middle">
Mercado Objetivo
</th>

<td valign="top">
Pequeños y medianos agricultores tecnificados, jefes de operaciones y administradores de fundo en el Perú.
</td>

<td valign="top">
Grandes agroindustrias, fundos exportadores y corporaciones agrícolas con infraestructura de riego compleja.
</td>

<td valign="top">
Medianos y grandes productores agrícolas que buscan optimizar la fertilización y humedad del suelo.
</td>

<td valign="top">
Grandes productores de cultivos extensivos y agroexportadores orientados a la certificación de huella hídrica.
</td>

</tr>

<tr>

<th align="center" valign="middle">
Estrategias de Marketing
</th>

<td valign="top">
Posicionamiento basado en bajo costo, simplicidad de instalación, enfoque local e integración de protección hídrica y fitosanitaria.
</td>

<td valign="top">
Ventas directas B2B, alianzas con empresas de ingeniería de riego y presencia en ferias agroindustriales internacionales.
</td>

<td valign="top">
Marketing de contenidos científicos, demostraciones de retorno de inversión y alianzas con fabricantes de maquinaria agrícola.
</td>

<td valign="top">
Enfoque en sostenibilidad ambiental, créditos de agua, alianzas corporativas y modelo 100 % software de suscripción.
</td>

</tr>

<tr>

<th rowspan="3" align="center" valign="top">
Perfil de Productos
</th>

<th align="center" valign="middle">
Productos y servicios
</th>

<td valign="top">
Sensado diferencial de caudal por pulsos.<br>
Cierre automático por electroválvula.<br>
Detección de plagas por cámara ESP32-CAM y Edge AI.<br>
Alertas en tiempo real.<br>
Dashboard web/móvil responsive.<br>
Bitácora de eventos y evidencia.
</td>

<td valign="top">
Nodos de campo inalámbricos (RF).<br>
Control automatizado de válvulas.<br>
Monitoreo de presión y caudal.<br>
Plataforma web/móvil de gestión.<br>
Integración con estaciones meteorológicas.
</td>

<td valign="top">
Sensores espirales de humedad de suelo.<br>
Telemetría celular/satelital.<br>
Recomendaciones automáticas de riego.<br>
Integración con modelos de enfermedad.<br>
Dashboard analítico.
</td>

<td valign="top">
Balance hídrico satelital.<br>
Recomendaciones semanales de riego.<br>
Reportes de eficiencia hídrica.<br>
Certificación de huella hídrica.<br>
Plataforma web y móvil.
</td>

</tr>

<tr>

<th align="center" valign="middle">
Precios y costos
</th>

<td valign="top">
Modelo de Kit IoT económico con pago inicial accesible y suscripción SaaS mensual de bajo costo.
</td>

<td valign="top">
Elevada inversión inicial en infraestructura hardware, licencias anuales de software y costo de mantenimiento especializado.
</td>

<td valign="top">
Costo moderado-alto por sensor de suelo e infraestructura de comunicación, más suscripción anual por hectárea.
</td>

<td valign="top">
Suscripción basada puramente en software (SaaS) cobrada por hectárea monitoreada al año.
</td>

</tr>

<tr>

<th align="center" valign="middle">
Canales de distribución
</th>

<td valign="top">
Venta directa web (Landing Page), distribuidores locales de equipos de riego y asociaciones de regantes.
</td>

<td valign="top">
Red de distribuidores autorizados de riego, integradores de tecnología agrícola y representantes comerciales directos.
</td>

<td valign="top">
Venta directa corporativa, distribuidores agrícolas y alianzas con plataformas AgTech socias.
</td>

<td valign="top">
Plataforma web digital, fuerza de ventas B2B y convenios con cooperativas agrícolas.
</td>

</tr>

<tr>

<th rowspan="4" align="center" valign="top">
Análisis SWOT
</th>

<th align="center" valign="middle">
Fortalezas
</th>

<td valign="top">
Solución de ciclo cerrado (Sense-Act).<br>
Doble propósito (agua + plagas).<br>
Bajo costo de hardware.<br>
Trazabilidad de datos en el borde.
</td>

<td valign="top">
Líder en automatización industrial.<br>
Hardware ultra-robusto.<br>
Gran alcance de cobertura por RF.<br>
Marca consolidada.
</td>

<td valign="top">
Tecnología de sensores patentada.<br>
Fuerte respaldo científico.<br>
Ecosistema de datos integrado.<br>
Analítica predictiva madura.
</td>

<td valign="top">
Cero despliegue de hardware.<br>
Fácil adopción e implementación.<br>
Escalabilidad inmediata.<br>
Fuerte enfoque en huella hídrica.
</td>

</tr>

<tr>

<th align="center" valign="middle">
Debilidades
</th>

<td valign="top">
Marca en fase inicial.<br>
Alcance acotado a parcelas/tramos delimitados en el MVP.<br>
Menor trayectoria comercial.
</td>

<td valign="top">
Costo inaccesible para pequeños productores.<br>
Instalación y configuración complejas.<br>
Sin módulo de visión para plagas foliares.
</td>

<td valign="top">
Requiere instalar sensores físicos de suelo.<br>
No detecta fugas de tuberías directamente.<br>
Sin mecanismos de corte automático de flujo.
</td>

<td valign="top">
No detecta roturas físicas o fugas repentinas en tuberías.<br>
Sin monitoreo in situ de plagas insecto a insecto.<br>
Dependiente de cobertura de nubes para satélite.
</td>

</tr>

<tr>

<th align="center" valign="middle">
Oportunidades
</th>

<td valign="top">
Alta penetración de internet en zonas rurales peruanas (83 %).<br>
Creciente necesidad de optimizar agua y reducir agroquímicos.<br>
Escasa competencia en soluciones IoT duales de bajo costo.
</td>

<td valign="top">
Expansión hacia megaproyectos de agroexportación.<br>
Integración con sistemas de fertirriego inteligente.
</td>

<td valign="top">
Crecimiento del mercado de agricultura de precisión.<br>
Expansión en mercados de América Latina.
</td>

<td valign="top">
Aumento de regulaciones ambientales sobre uso del agua.<br>
Alianzas con empresas multinacionales de alimentos.
</td>

</tr>

<tr>

<th align="center" valign="middle">
Amenazas
</th>

<td valign="top">
Competidores internacionales reduciendo precios.<br>
Resistencia al cambio tecnológico en agricultores tradicionales.<br>
Inestabilidad en suministro de componentes electrónicos.
</td>

<td valign="top">
Aparición de alternativas IoT de bajo costo.<br>
Cambios en estándares de conectividad inalámbrica.
</td>

<td valign="top">
Nuevas tecnologías de sensado remoto no invasivo.<br>
Competencia de startups locales.
</td>

<td valign="top">
Sensibilidad a la precisión de datos satelitales gratuitos.<br>
Entrada de competidores con modelos híbridos.
</td>

</tr>

</table>

---

### 2.1.2. Estrategias y tácticas frente a competidores

**1. Estrategia de Solución Integral de Bajo Costo (Doble Protección Agua + Sanidad)**
Diferenciar a AgroLeak frente a competidores que solo venden telemetría hídrica (como DropControl) o analítica satelital (como Kilimo), ofreciendo una solución única que combina la detección física de fugas con la identificación fotográfica de plagas en un solo kit económico.

* **Tácticas:**
  * Promocionar el valor dual del producto en la Landing Page bajo el concepto *"Protege tu agua y cuida tus hojas con un solo dispositivo"*.
  * Demostrar en videos promocionales cómo el ahorro de un evento de fuga o la detección temprana de plagas recupera el costo del kit en la primera campaña agrícola.

**2. Estrategia de Ciclo Cerrado con Actuación Física Segura**
Posicionar la capacidad de actuación automática (cierre de electroválvula por relé) como un diferenciador crítico frente a plataformas puramente informativas o satelitales que no pueden detener el desperdicio de agua cuando ocurre una rotura en ausencia del agricultor.

* **Tácticas:**
  * Configurar modos de operación flexibles (`MONITOR_ONLY`, `MANUAL_APPROVAL`, `SAFE_AUTO_DEMO`) para dar control total al agricultor y eliminar el temor a cierres accidentales.
  * Incluir un botón físico de paro de emergencia y notificaciones inmediatas al celular para mantener siempre la supervisión humana.

**3. Estrategia de Autonomía en el Borde (Edge Computing)**
Aprovechar la capacidad del gateway Edge para procesar inferencias de IA y reglas hidráulicas localmente, superando la debilidad de competidores cloud dependientes de internet continuo en zonas rurales.

* **Tácticas:**
  * Implementar almacenamiento temporal SQLite en el borde para conservar lecturas e imágenes durante caídas de red, garantizando sincronización automática al restaurar la señal.
  * Resaltar en la comunicación comercial que el sistema sigue protegiendo el tramo de riego incluso si se interrumpe la conexión a internet.

**4. Estrategia de Alianzas Locales y Progresión Gradual**
Mitigar la falta de reconocimiento inicial de marca construyendo confianza mediante acompañamiento técnico directo en los valles agrícolas de Lima y alianzas estratégicas.

* **Tácticas:**
  * Ofrecer instalaciones piloto asistidas y demostraciones con maquetas funcionales ante asociaciones de regantes y cooperativas locales.
  * Diseñar un modelo de precios transparente (*Kit Hardware + Suscripción SaaS accesible*) adaptado a la economía del pequeño y mediano productor peruano.

## 2.2. Entrevistas

En esta sección se aborda la investigación cualitativa de campo a través de la recolección de información obtenida mediante entrevistas a profundidad con representantes de los dos segmentos objetivo identificados. El propósito de este proceso es validar las hipótesis planteadas en la etapa de Lean UX, profundizar en los flujos de trabajo actuales (*As-Is*) e identificar los puntos de dolor reales en torno a la gestión del agua y la sanidad vegetal.

---

### 2.2.1. Diseño de entrevistas

Para la recolección de datos se diseñó un cuestionario de entrevista semiestructurada compuesto por preguntas abiertas, estructurado de forma que abarque variables demográficas, hábitos tecnológicos y la problemática operativa específica de cada perfil. El diseño busca extraer datos objetivos (escala, tipo de riego, cultivos, dispositivos) e impresiones subjetivas (frustraciones, nivel de confianza en la automatización y expectativas de solución).

#### Segmento 1: Pequeños y Medianos Agricultores Tecnificados
El objetivo del cuestionario para este segmento es comprender la rutina diaria de inspección en campo, la frecuencia e impacto económico de los incidentes hídricos (fugas o roturas) y los métodos tradicionales de observación de plagas en hojas.

**Preguntas para las entrevistas:**

1. **Información general y escala:** ¿En qué zona agrícola se ubica su parcela, cuántas hectáreas administra y qué tipo de cultivo con riego tecnificado opera actualmente?
2. **Proceso de riego actual:** ¿Cómo programa y realiza el control del riego en sus parcelas y qué herramientas o métodos utiliza para verificar que el agua fluya correctamente?
3. **Puntos de dolor hídricos:** ¿Con qué frecuencia se presentan fugas, desacoples de mangueras o variaciones no deseadas de caudal, y cuánto tiempo transcurre habitualmente hasta que las detecta?
4. **Consecuencias operativas:** Cuando ocurre una pérdida de agua no detectada a tiempo, ¿qué impacto genera en el costo de energía de bombeo, consumo de agua o en la salud de la planta?
5. **Inspección de plagas:** ¿De qué manera realiza actualmente el monitoreo y conteo de plagas u organismos dañinos en las hojas de sus cultivos?
6. **Uso de tecnología:** ¿Qué tipo de dispositivos (smartphone, tablet, laptop) utiliza en su día a día y qué tan cómodo se siente recibiendo notificaciones o alertas en su celular?
7. **Recepción de propuesta hídrica:** Si un sistema IoT detectara una diferencia persistente de caudal y pudiera cerrar la válvula de forma automática para evitar pérdidas, ¿qué tan seguro o dispuesto se sentiría de utilizarlo?
8. **Recepción de propuesta fitosanitaria:** ¿Qué valor le aportaría recibir una alerta en su celular con la fotografía anotada de la hoja y la identificación del insecto detectado por una cámara instalada en el lote?
9. **Visualización de información:** ¿Qué datos o métricas considera indispensables ver en un panel móvil para tomar decisiones rápidas sobre su riego y sanidad vegetal?
10. **Expectativa comercial:** ¿Bajo qué modalidad de adquisición (compra del equipo + suscripción mensual o alquiler) le resultaría más accesible probar esta tecnología en su parcela?

---

#### Segmento 2: Jefes de Operaciones Agrícolas y Administradores de Fundo
El cuestionario dirigido a este segmento profesional busca profundizar en la eficiencia operativa a mayor escala, el control de costos de bombeo, la integración de datos agronómicos y los protocolos de seguridad requeridos para la adopción de actuadores automatizados.

**Preguntas para las entrevistas:**

1. **Perfil profesional y contexto:** ¿Cuál es su rol dentro del fundo, qué extensión agrícola tiene a su cargo y qué tipo de sistema de riego (goteo/aspersión) y supervisión fitosanitaria operan?
2. **Gestión de telemetría y costos:** ¿Cómo monitorean actualmente los volúmenes de agua utilizados y cuál es el impacto financiero de las fallas hidráulicas en el presupuesto operativo de la empresa?
3. **Identificación de fugas y anomalías:** ¿Qué procedimientos siguen actualmente para detectar desbalances de caudal o tuberías dañadas en sectores alejados de la estación principal?
4. **Manejo fitosanitario:** ¿Cómo coordinan con los supervisores de sanidad la detección temprana de plagas y qué criterio aplican para decidir una aplicación localizada vs. una fumigación general?
5. **Aceptación de Edge AI:** ¿Qué nivel de confianza le genera un modelo de visión por computador procesado en el borde que identifique y clasifique insectos objetivo a partir de capturas de cámara?
6. **Requisitos de seguridad y control:** ¿Qué salvaguardas o modos de operación (manual vs. automático) consideraría indispensables antes de autorizar que un sistema IoT corte el flujo de agua o active un actuador en campo?
7. **Trazabilidad y auditoría:** ¿Qué importancia tiene para la gestión del fundo disponer de una bitácora con registro de eventos (timestamp, lectura de caudal, fotografía de la plaga, regla aplicada y acción ejecutada)?
8. **Plataforma y conectividad:** Ante problemas habituales de señal de internet en campo, ¿cómo valora que el sistema conserve los datos localmente en el borde y los sincronice al restablecerse la red?
9. **Integración tecnológica:** ¿Qué características debe tener un dashboard de administración web para que resulte útil tanto para los operadores en campo como para la gerencia?
10. **Criterios de adopción:** ¿Cuáles son los principales indicadores de retorno de inversión (ROI) o eficiencia que evaluarían para decidir la contratación e implementación de AgroLeak en el fundo?

### 2.2.2. Registro de entrevistas

En esta sección se presentan las entrevistas realizadas a los integrantes de los segmentos objetivo. Cada registro incluye los datos relevantes de la persona entrevistada, la evidencia audiovisual y un resumen basado en sus respuestas al cuestionario de la sección 2.2.1.

#### Segmento 1: Pequeños y medianos agricultores tecnificados

##### Entrevista 1

**Entrevistado:** Pendiente de incorporar desde la rama `main`.

**Edad y ubicación:** Pendiente de incorporar desde la rama `main`.

**Evidencia de la entrevista:**

> Insertar aquí la imagen o captura correspondiente a la entrevista.

**Enlace del video:** Pendiente de incorporar desde la rama `main`.

**Resumen:** Pendiente de incorporar y redactar a partir del video de la entrevista.

#### Segmento 2: Jefes de operaciones agrícolas y administradores de fundo

##### Entrevista 1

**Entrevistado:** Pendiente de incorporar desde la rama `main`.

**Edad y ubicación:** Pendiente de incorporar desde la rama `main`.

**Evidencia de la entrevista:**

> Insertar aquí la imagen o captura correspondiente a la entrevista.

**Enlace del video:** Pendiente de incorporar desde la rama `main`.

**Resumen:** Pendiente de incorporar y redactar a partir del video de la entrevista.

##### Entrevista 2

**Entrevistado:** Alexis Alarcón Vargas.

**Edad:** 32 años.

**Distrito:** Cañete.

<img src="../assets/imagen-entrevista-2.png">


**Enlace del video:** [entrevista-sector-2.mp4](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202516291_upc_edu_pe/IQBUZID357uxQYUte2Gb4geMARDM9A0AdXGqjCBTxWvffuV?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=Lhg1P9)

**Resumen:** Alexis Alarcón Vargas, ingeniero agrónomo y jefe de Operaciones Agrícolas de la agroexportadora El Sur, supervisa el fundo San José, ubicado en el valle de Cañete. El fundo cuenta con 45 hectáreas —30 de palto Hass y 15 de uva de mesa— y utiliza riego por goteo automatizado desde casetas de bombeo. La programación del riego se realiza semanalmente según la evapotranspiración; sin embargo, el registro del volumen real de agua y de las presiones se lleva manualmente en cuadernos de campo, cuyos datos se transcriben a Excel al día siguiente.

Entre las dificultades identificadas, señaló que la falta de información en tiempo real retrasa la detección de errores humanos y roturas de líneas, afecta la uniformidad del riego y complica las auditorías. Indicó que ocurren entre tres y cinco fugas al mes debido a desacoples o fallas en mangueras y sellos. Estos incidentes generan sobrecostos de energía, desperdicio de fertilizantes disueltos y riesgos de penalización en certificaciones como GlobalG.A.P. y en auditorías de huella hídrica.

En sanidad vegetal, el fundo cuenta con evaluadores que monitorean plagas como queresa, arañita roja y trips. Los reportes pueden tardar entre 24 y 48 horas, por lo que las decisiones de aplicación suelen abarcar lotes completos en lugar de focalizarse en las áreas afectadas. Para sus actividades utiliza diariamente una laptop y un smartphone, y consulta dashboards web y notificaciones push.

Respecto a la actuación automática de válvulas, considera necesarios interlocks que validen la persistencia de una anomalía y permisos con credenciales para autorizar la reapertura después de una inspección física. También valoró las alertas fitosanitarias con fotografías y un porcentaje de certeza de la IA, que, según su estimación, podrían contribuir a reducir hasta en un 30 % el consumo de fitosanitarios. Entre los indicadores que considera útiles para un panel menciona el balance de caudal de entrada y salida en litros por minuto, el registro de incidencias, la bitácora de acciones sobre válvulas y la eficiencia hídrica.

Finalmente, indicó que para una agroempresa sería adecuado un modelo SaaS B2B con suscripción por hectárea, que incluya el arrendamiento del hardware, garantía y mantenimiento, de modo que pueda gestionarse como gasto operativo.

### 2.2.3. Análisis de entrevistas

En esta sección se describirán los principales hallazgos identificados al revisar las entrevistas. El análisis se redactará en forma narrativa, contrastando las respuestas de los entrevistados y relacionando cada necesidad o dificultad con la evidencia obtenida en los videos.

**Segmento 1: Pequeños y medianos agricultores tecnificados**

Pendiente de completar cuando se incorporen y revisen las entrevistas de este segmento.

**Segmento 2: Jefes de operaciones agrícolas y administradores de fundo**

Pendiente de completar cuando se incorporen y revisen las entrevistas de este segmento, incluida la Entrevista 2.

**Síntesis de hallazgos**

Pendiente de redactar a partir de los hallazgos verificados en ambos segmentos.

## 2.3. Needfinding

### 2.3.1. User Personas

Las User Personas se elaborarán en UXPressia a partir de los hallazgos obtenidos de las entrevistas, diferenciando las características verificadas de cada segmento objetivo. Las fichas deben representar necesidades, objetivos, comportamientos, frustraciones y contexto tecnológico sustentados por la evidencia, sin atribuirles características no observadas.

**Persona del Segmento 1: Pequeño o mediano agricultor tecnificado**

> Artefacto pendiente: insertar en esta sección la ficha de User Persona creada en UXPressia, una vez contrastada con las entrevistas del segmento.

**Persona del Segmento 2: Jefe de operaciones agrícolas o administrador de fundo**

La persona **Ing. Vega** representa el arquetipo de productor tecnificado utilizado para el Needfinding de este segmento. Según la ficha de UXPressia, tiene 27 años, administra una empresa agrícola de 8 hectáreas de palta y cítricos en Palpa (Ica), y opera con riego por goteo, bombeo y válvulas por sector. Sus objetivos incluyen detectar oportunamente fugas y obstrucciones, recibir alertas en el smartphone, localizar posibles plagas y comprobar el ahorro antes de adoptar la solución. La ficha también señala que actualmente la verificación del riego y la inspección de plagas se realizan manualmente.

<img src="../assets/ing-vega-person.png" alt="User Persona Ing. Vega, jefe de operaciones agrícolas" width="100%">

### 2.3.2. User Task Matrix

En esta sección se presenta la User Task Matrix de AgroLeak. La matriz organiza las tareas de los segmentos objetivo y permite compararlas según su frecuencia (F) e importancia (I), en una escala de **Alta, Media y Baja**.

Las tareas que se muestran a continuación se identificaron a partir de los flujos del Event Storming y del alcance funcional de AgroLeak. Las valoraciones de frecuencia e importancia son **preliminares**: deben contrastarse con las entrevistas y con el Needfinding antes de considerarse hallazgos validados. En particular, las tareas de configuración y mantenimiento del sistema pueden corresponder a un administrador o técnico autorizado, y no necesariamente al agricultor.

| Tareas (Tasks) | Agricultor tecnificado: Frecuencia | Agricultor tecnificado: Importancia | Jefe de operaciones / administrador: Frecuencia | Jefe de operaciones / administrador: Importancia |
| :--- | :---: | :---: | :---: | :---: |
| Consultar el estado general del fundo, sus parcelas y sectores | Por validar | Por validar | Por validar | Por validar |
| Revisar lecturas de caudal y el estado de los dispositivos asignados a los sectores | Por validar | Por validar | Por validar | Alta |
| Revisar si el sistema detectó una posible fuga, obstrucción o presión fuera de rango | Por validar | Por validar | Por validar | Alta |
| Consultar observaciones de plagas y la evidencia capturada | Por validar | Por validar | Por validar | Alta |
| Consultar, reconocer y dar seguimiento a las alertas | Por validar | Por validar | Por validar | Alta |
| Revisar el estado de una solicitud de apertura o cierre de válvula y confirmar el resultado cuando corresponda | Por validar | Por validar | Por validar | Por validar |
| Consultar el historial de telemetría, alertas y acciones ejecutadas | Por validar | Por validar | Por validar | Por validar |
| Configurar o actualizar fundos, parcelas, sectores y cultivos | Por validar | Por validar | Por validar | Por validar |
| Registrar dispositivos y asignarlos a un sector | Por validar | Por validar | Por validar | Por validar |
| Cambiar el modo de operación del sistema, de acuerdo con los permisos definidos | Por validar | Por validar | Por validar | Por validar |
| Revisar métricas y reportes para tomar decisiones operativas y comprobar el ahorro de recursos | Por validar | Por validar | Por validar | Alta |

Las valoraciones **Alta** de importancia para el Segmento 2 reflejan los objetivos explícitos de la ficha de Ing. Vega (detección oportuna, alertas, identificación de plagas y comprobación del ahorro); no representan una medición estadística. La frecuencia de las tareas y las valoraciones del Segmento 1 quedan **Por validar** hasta completar la síntesis del Needfinding de ambos segmentos. Si una tarea no corresponde a un segmento, se debe marcar como **No aplica** en lugar de asignarle una valoración.

### 2.3.3. User Journey Mapping

Los User Journey Maps se elaborarán en UXPressia a partir del proceso actual (*As-Is*) descrito por los entrevistados. Cada mapa debe reflejar las etapas de la tarea, las acciones y puntos de contacto del usuario, sus dificultades y emociones, así como las oportunidades de mejora identificadas. No se deben presentar como observados los pasos que no hayan sido confirmados en las entrevistas.

**Journey Map del Segmento 1: Pequeño o mediano agricultor tecnificado**

> Artefacto pendiente: insertar el Journey Map elaborado en UXPressia con base en las entrevistas.

**Journey Map del Segmento 2: Jefe de operaciones agrícolas o administrador de fundo**

El Journey Map de Ing. Vega representa cuatro etapas de la supervisión del riego: operación, verificación manual, detección tardía de incidencias y atención/corrección. En el proceso actual descrito por la ficha, la revisión manual puede retrasar la detección de fugas u obstrucciones; como oportunidades se identifican alertas oportunas en el smartphone, evidencia que facilite localizar el problema y control manual o remoto de la válvula antes de habilitar una automatización completa.

<img src="../assets/ing-vega-journey-map.png" alt="User Journey Map de Ing. Vega, jefe de operaciones agrícolas" width="100%">

### 2.3.4. Empathy Mapping

Los Empathy Maps se elaborarán en UXPressia mediante la síntesis de expresiones y comportamientos observados en las entrevistas. Las secciones de lo que la persona dice, piensa, hace y siente, así como sus dificultades y beneficios esperados, deberán derivarse de evidencia y conservar el contexto de cada segmento.

**Empathy Map del Segmento 1: Pequeño o mediano agricultor tecnificado**

> Artefacto pendiente: insertar el Empathy Map elaborado en UXPressia con base en las entrevistas.

**Empathy Map del Segmento 2: Jefe de operaciones agrícolas o administrador de fundo**

El Empathy Map de Ing. Vega sintetiza las necesidades de supervisar el riego, detectar fugas y obstrucciones a tiempo, recibir alertas y conocer la evidencia de posibles plagas para intervenir de forma focalizada. También recoge frustraciones relacionadas con la revisión manual, el desperdicio de agua y los costos de bombeo, así como el interés en comprobar el ahorro antes de adoptar la solución. La ficha identifica expresamente algunos aspectos —como herramientas actuales, conectividad y tamaño/calidad del equipo— como no documentados, por lo que no se presentan aquí como hechos.

<img src="../assets/ing-vega-empathy-map.png" alt="Empathy Map de Ing. Vega, jefe de operaciones agrícolas" width="100%">

## 2.4. Big Picture Event Storming

El Big Picture Event Storming de AgroLeak se elaboró en Miro para representar los eventos del dominio, las acciones que los originan, los actores y sistemas participantes, y las reglas que conectan los procesos. Los siguientes pasos muestran el desarrollo del modelado, desde la identificación de eventos hasta la delimitación de los Bounded Contexts.

### Paso 1: Domain Events — Eventos de dominio

Se identifican los hechos relevantes que ocurren en el dominio y se expresan en pasado. Estos eventos permiten describir qué sucede en AgroLeak durante la configuración del fundo, el monitoreo del riego, la detección de plagas y la atención de alertas.

<img src="../assets/step-1.jpg" alt="Paso 1: identificación de eventos de dominio en AgroLeak" width="100%">

### Paso 2: Timelines — Ordenar los eventos

Los eventos identificados se organizan cronológicamente de izquierda a derecha para representar la secuencia de cada proceso y hacer visibles las alternativas y excepciones.

<img src="../assets/step-2.jpg" alt="Paso 2: líneas de tiempo de los eventos de AgroLeak" width="100%">

### Paso 3: Commands — Identificar comandos

Se incorporan las acciones o solicitudes que pueden provocar los eventos, expresadas como comandos. Cada comando debe estar relacionado con el actor o sistema que lo inicia y con el resultado que produce.

<img src="../assets/step-3.jpg" alt="Paso 3: comandos del dominio AgroLeak" width="100%">

### Paso 4: Actors — Identificar actores

Se identifican los usuarios y roles que participan en los procesos y que pueden iniciar comandos o responder a eventos, de acuerdo con las responsabilidades definidas para AgroLeak.

<img src="../assets/step-4.jpg" alt="Paso 4: actores participantes en los procesos de AgroLeak" width="100%">

### Paso 5: Hotspots — Identificar puntos de atención

Se señalan dudas, problemas, excepciones y decisiones pendientes que requieren aclaración del equipo o validación con los usuarios. Los hotspots ayudan a distinguir las reglas confirmadas de los aspectos aún no resueltos.

<img src="../assets/step-5.jpg" alt="Paso 5: hotspots y puntos pendientes del dominio AgroLeak" width="100%">

### Paso 6: Policies — Reglas de negocio y reacciones automáticas

Se identifican las políticas que reaccionan a eventos y pueden iniciar comandos o generar nuevos eventos. En AgroLeak, este paso permite documentar las reglas que relacionan las lecturas de caudal, la detección de anomalías, la generación de alertas y las solicitudes de actuación, según lo definido en el dominio.

<img src="../assets/step-6.jpg" alt="Paso 6: políticas y reglas de negocio de AgroLeak" width="100%">

### Paso 7: Read Models — Información consultada para decidir

Se representan las vistas de información que necesitan los usuarios o sistemas para consultar el estado del proceso y tomar decisiones, por ejemplo, la información de monitoreo, alertas o historial que efectivamente contempla el sistema.

<img src="../assets/step-7.jpg" alt="Paso 7: read models consultados en AgroLeak" width="100%">

### Paso 8: External Systems — Dispositivos y sistemas externos

Se identifican los dispositivos y sistemas externos que participan en los flujos, tales como sensores, cámaras, gateway, actuadores o servicios de comunicación, de acuerdo con su participación en la solución.

<img src="../assets/step-8.jpg" alt="Paso 8: sistemas y dispositivos externos de AgroLeak" width="100%">

### Paso 9: Aggregates — Agregados

Se agrupan los eventos y comandos alrededor de los agregados que protegen las reglas e invariantes del dominio. Cada agregado recibe comandos y, cuando corresponde, emite eventos que reflejan el resultado de la operación.

<img src="../assets/step-9.jpg" alt="Paso 9: agregados del dominio AgroLeak" width="100%">

### Paso 10: Bounded Contexts — Contextos delimitados

Se delimitan los contextos a partir de las responsabilidades del dominio, agrupando sus agregados y relacionándolos mediante las políticas o interacciones correspondientes. Los límites representan modelos con lenguaje y responsabilidades consistentes; no implican necesariamente que cada contexto sea una aplicación o un microservicio independiente.

<img src="../assets/step-10.jpg" alt="Paso 10: Bounded Contexts de AgroLeak" width="100%">

## 2.5. Ubiquitous Language

El Ubiquitous Language establece términos comunes entre los usuarios del dominio, el equipo del proyecto y los artefactos de análisis y diseño. Esta primera versión se basa en el contexto del proyecto y debe contrastarse con las expresiones utilizadas por los entrevistados y con los resultados del Event Storming en Miro.

| Término | Definición en el dominio de AgroLeak |
| :--- | :--- |
| **Fundo** | Unidad de operación agrícola administrada por un productor, administrador o equipo de operaciones. |
| **Parcela** | Área de cultivo dentro de un fundo que puede ser supervisada como parte de la operación agrícola. |
| **Sector** | Área operativa del fundo a la que se asocian cultivos y dispositivos, según la organización registrada en AgroLeak. |
| **Cultivo** | Tipo de cultivo registrado para una parcela o sector del fundo. |
| **Tramo de riego** | Parte de la infraestructura de riego monitoreada por uno o más dispositivos; su equivalencia con el término **sector** debe confirmarse con el modelo de datos y la lógica de la aplicación. |
| **Caudal** | Volumen de agua que circula por un punto del sistema de riego durante un intervalo de tiempo. |
| **Lectura de caudal** | Medición reportada por un sensor en un punto del tramo de riego, con su valor, unidad y referencia temporal. |
| **Balance de caudal** | Comparación entre el caudal medido en distintos puntos de un tramo, como la entrada y la salida. En la entrevista se mencionó el uso de litros por minuto; los puntos de medición y criterios de diferencia deben corresponder a la configuración real del sistema. |
| **Presión de riego** | Presión registrada en el sistema de riego para supervisar sus condiciones de operación. Los rangos aceptables deben definirse según la instalación y no inferirse únicamente de una entrevista. |
| **Programación de riego** | Planificación de los periodos o volúmenes de riego para un cultivo o sector. La entrevista indica que puede considerar la evapotranspiración, pero AgroLeak no debe presentarse como generador de esa programación salvo que esa función esté definida. |
| **Evapotranspiración** | Pérdida de agua hacia la atmósfera por evaporación y transpiración de las plantas; puede utilizarse como dato de referencia para planificar el riego. |
| **Telemetría** | Datos enviados por los dispositivos de campo para supervisar el estado de los sensores, el flujo de agua y otros elementos monitoreados. |
| **Registro de campo** | Anotación manual de mediciones, observaciones o incidencias realizada durante la operación agrícola. En la entrevista, los datos de cuadernos de campo se transcribían posteriormente a Excel. |
| **Snapshot** | Captura o conjunto puntual de datos evaluado por el sistema para mostrar el estado de las lecturas y detectar posibles condiciones anómalas. El contenido exacto debe mantenerse alineado con la implementación. |
| **Anomalía persistente de caudal** | Diferencia entre las lecturas de entrada y salida que se mantiene durante el periodo definido por las reglas del sistema. Los umbrales y la duración deben precisarse en el diseño del producto. |
| **Fuga** | Pérdida no deseada de agua en el sistema de riego, cuya detección puede apoyarse en la evaluación de lecturas de caudal. |
| **Dispositivo IoT** | Sensor o actuador instalado en campo que captura mediciones o ejecuta acciones relacionadas con el monitoreo y la protección del riego. |
| **Dispositivo asignado** | Dispositivo registrado y asociado a un sector para participar en el monitoreo o la actuación correspondiente. |
| **Estado del dispositivo** | Condición reportada por el sistema para indicar si un dispositivo se encuentra conectado (*ONLINE*) o sin conexión (*OFFLINE*). |
| **Modo de operación** | Configuración que determina cómo se comporta el sistema frente a condiciones detectadas. Los modos y permisos disponibles deben corresponder a los definidos en la aplicación y en las reglas del dominio. |
| **Interlock** | Salvaguarda que condiciona o bloquea una actuación hasta que se cumplan reglas de seguridad definidas. En la entrevista se solicitó validar la persistencia de una anomalía antes de permitir una respuesta automática; la regla concreta debe acordarse en el diseño del sistema. |
| **Gateway Edge** | Componente situado en el borde que recibe o procesa datos de dispositivos y puede ejecutar capacidades locales aun cuando la conectividad con la nube no esté disponible. |
| **Inferencia en el borde (Edge AI)** | Procesamiento local de una imagen mediante un modelo de IA para estimar la presencia o clasificación de una plaga. |
| **Evaluación fitosanitaria** | Inspección del cultivo para identificar y registrar la presencia de plagas. En el proceso descrito por el entrevistado, evaluadores realizan esta actividad y consolidan reportes. |
| **Observación de plaga** | Registro asociado a una captura o inspección y, cuando corresponde, al resultado de inferencia. Una observación detectada por el sistema no equivale por sí sola a una confirmación agronómica. |
| **Porcentaje de confianza de la inferencia** | Valor producido por un modelo que expresa su nivel de confianza en una clasificación. No debe interpretarse como certeza ni como confirmación agronómica. |
| **Alerta** | Aviso generado por el sistema para comunicar una condición relevante, como una posible fuga, una observación de plaga u otra condición definida por las reglas. |
| **Estado de alerta** | Estado del ciclo de vida de una alerta. El tablero contempla estados como **ACTIVE**, **ACKNOWLEDGED** y **RESOLVED**; sus transiciones deben corresponder a las acciones disponibles en la aplicación. |
| **Comando de válvula** | Solicitud de apertura o cierre dirigida al actuador. La solicitud, el envío de la orden y el resultado confirmado son hechos distintos. |
| **Estado de ejecución** | Resultado reportado para una actuación, por ejemplo, pendiente, confirmada o fallida. No se debe tratar una orden enviada como una actuación confirmada. |
| **Autorización de reapertura** | Permiso requerido para volver a abrir una válvula después de una actuación de protección. El entrevistado indicó que debería darse tras una inspección física y con credenciales autorizadas; la regla y los roles permitidos deben definirse formalmente. |
| **Bitácora de auditoría (audit log)** | Registro trazable de incidencias y acciones realizadas sobre el sistema, incluyendo las operaciones relacionadas con las válvulas cuando estén disponibles. |
| **Eficiencia hídrica** | Indicador utilizado para evaluar la relación entre el agua empleada y la operación o producción agrícola. Su fórmula y datos de cálculo deben acordarse antes de presentarlo como métrica del producto. |
| **Estado seguro** | Condición de protección definida para el sistema después de una situación de riesgo. El cierre solicitado y el cierre confirmado deben distinguirse; una acción no confirmada no debe registrarse como exitosa. |
| **Sincronización idempotente** | Envío o reintento de datos almacenados localmente sin crear registros duplicados cuando una misma operación se procesa más de una vez. |
| **Bounded Context (contexto delimitado)** | Límite dentro del cual un modelo y sus términos tienen un significado consistente. Los nombres y responsabilidades deben mantenerse alineados con los límites acordados en el paso 10 del Event Storming. |

Los nombres y definiciones de esta tabla constituyen la base del lenguaje de dominio a partir del Event Storming, la lógica de la aplicación y la entrevista del Segmento 2. Los términos recogidos de una entrevista reflejan lo expresado por ese participante; no implican por sí solos que AgroLeak ya implemente o haya aprobado esas reglas o métricas. Deben contrastarse con las demás entrevistas y mantenerse consistentes en los requisitos, diseños y diagramas. En particular, el equipo debe confirmar si **sector** y **tramo de riego** representan la misma unidad, y validar los estados y transiciones de alertas, dispositivos y comandos de válvula con la implementación.