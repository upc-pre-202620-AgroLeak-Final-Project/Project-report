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

**Entrevistado:** Por completar después de realizar la entrevista.

**Edad y ubicación:** Por completar.

**Evidencia de la entrevista:**

> Insertar aquí la imagen o captura de la Entrevista 2 del Segmento 2.

**Enlace del video:** Por agregar cuando esté disponible.

**Resumen:** Por redactar a partir del video y de las respuestas al cuestionario de la sección 2.2.1.

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

> Artefacto pendiente: insertar en esta sección la ficha de User Persona creada en UXPressia, una vez contrastada con las entrevistas del segmento.

### 2.3.2. User Task Matrix

La User Task Matrix permite identificar y comparar las tareas que realizan los entrevistados, considerando su frecuencia e importancia. Se elaborará en UXPressia a partir de las entrevistas y se presentará mediante las imágenes correspondientes a cada segmento.

**Segmento 1: Pequeños y medianos agricultores tecnificados**

> Insertar aquí la imagen de la User Task Matrix del Segmento 1, elaborada en UXPressia con base en las entrevistas.

**Segmento 2: Jefes de operaciones agrícolas y administradores de fundo**

> Insertar aquí la imagen de la User Task Matrix del Segmento 2, elaborada en UXPressia con base en las entrevistas.

### 2.3.3. User Journey Mapping

Los User Journey Maps se elaborarán en UXPressia a partir del proceso actual (*As-Is*) descrito por los entrevistados. Cada mapa debe reflejar las etapas de la tarea, las acciones y puntos de contacto del usuario, sus dificultades y emociones, así como las oportunidades de mejora identificadas. No se deben presentar como observados los pasos que no hayan sido confirmados en las entrevistas.

**Journey Map del Segmento 1: Pequeño o mediano agricultor tecnificado**

> Artefacto pendiente: insertar el Journey Map elaborado en UXPressia con base en las entrevistas.

**Journey Map del Segmento 2: Jefe de operaciones agrícolas o administrador de fundo**

> Artefacto pendiente: insertar el Journey Map elaborado en UXPressia con base en las entrevistas.

### 2.3.4. Empathy Mapping

Los Empathy Maps se elaborarán en UXPressia mediante la síntesis de expresiones y comportamientos observados en las entrevistas. Las secciones de lo que la persona dice, piensa, hace y siente, así como sus dificultades y beneficios esperados, deberán derivarse de evidencia y conservar el contexto de cada segmento.

**Empathy Map del Segmento 1: Pequeño o mediano agricultor tecnificado**

> Artefacto pendiente: insertar el Empathy Map elaborado en UXPressia con base en las entrevistas.

**Empathy Map del Segmento 2: Jefe de operaciones agrícolas o administrador de fundo**

> Artefacto pendiente: insertar el Empathy Map elaborado en UXPressia con base en las entrevistas.

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
| **Tramo de riego** | Segmento de la infraestructura de riego cuyo flujo se monitorea mediante lecturas asociadas a sus puntos de entrada y salida. |
| **Caudal** | Volumen de agua que circula por un punto del sistema de riego durante un intervalo de tiempo. |
| **Lectura de caudal** | Medición reportada por un sensor en un punto del tramo de riego, con su valor y referencia temporal. |
| **Telemetría** | Datos enviados por los dispositivos de campo para supervisar el estado de los sensores, el flujo de agua y otros elementos monitoreados. |
| **Anomalía persistente de caudal** | Diferencia entre las lecturas de entrada y salida que se mantiene durante el periodo definido por las reglas del sistema. Los umbrales y la duración deben precisarse en el diseño del producto. |
| **Fuga** | Pérdida no deseada de agua en el sistema de riego, cuya detección puede apoyarse en la evaluación de lecturas de caudal. |
| **Dispositivo IoT** | Sensor o actuador instalado en campo que captura mediciones o ejecuta acciones relacionadas con el monitoreo y la protección del riego. |
| **Gateway Edge** | Componente situado en el borde que recibe o procesa datos de dispositivos y puede ejecutar capacidades locales aun cuando la conectividad con la nube no esté disponible. |
| **Inferencia en el borde (Edge AI)** | Procesamiento local de una imagen mediante un modelo de IA para estimar la presencia o clasificación de una plaga. |
| **Observación de plaga** | Registro asociado a una captura de imagen y al resultado producido por el modelo de detección; no equivale por sí solo a una confirmación agronómica. |
| **Alerta** | Aviso generado por el sistema para comunicar una condición relevante, como una anomalía de caudal o una observación de plaga. |
| **Solicitud de cierre de válvula** | Petición de ejecutar el cierre preventivo de una válvula después de que las reglas de protección determinen que corresponde. |
| **Actuación de válvula** | Acción física de apertura o cierre ejecutada por el actuador, cuyo resultado debe registrarse y verificarse. |
| **Estado seguro** | Condición de protección definida para el sistema después de una situación de riesgo. El cierre solicitado y el cierre confirmado deben distinguirse; una acción no confirmada no debe registrarse como exitosa. |
| **Sincronización idempotente** | Envío o reintento de datos almacenados localmente sin crear registros duplicados cuando una misma operación se procesa más de una vez. |
| **Bounded Context (contexto delimitado)** | Límite dentro del cual un modelo y sus términos tienen un significado consistente. Los contextos específicos de AgroLeak se definirán y documentarán a partir del EventStorming. |

Los nombres y definiciones de esta tabla constituyen una base de trabajo, no una decisión final sobre la arquitectura. Después del taller de Event Storming, el equipo deberá ajustar el vocabulario para que los términos coincidan con los eventos, comandos, reglas y Bounded Contexts acordados.