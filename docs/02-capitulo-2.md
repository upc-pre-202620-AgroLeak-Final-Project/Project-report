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

#### Entrevista 1

<img width="1102" height="618" alt="Captura de pantalla 2026-10-04 a la(s) 9 05 35 p  m" src="https://github.com/user-attachments/assets/f009fba5-7343-4391-b7a7-e6b57b4790ce" />

[ENTREVISTA 1](https://drive.google.com/file/d/1lvKcFmLgGJu_Ca_NJWwq2QYOh67I5BB2/view?usp=share_link)

**Nombre:** Ingeniero Vega

**Edad:** 27

**Residencia:** Palpa, Ica

**Segmento Objetivo:** Empresa agrícola (Mediano productor de palta y cítricos)

**Duración:** 09:00 minutos

**Resumen:** El Ing. Vega administra una empresa agrícola de 8 hectáreas en la costa de Palpa, Ica, enfocada en el cultivo de palta y cítricos mediante un sistema de riego por goteo con bombeo y válvulas por sector. Actualmente, tanto la verificación del riego como la inspección de plagas se realizan de forma manual, lo que ocasiona que problemas frecuentes como mangueras desacopladas, fugas o goteros obstruidos tarden horas o hasta el siguiente turno en detectarse. Esto genera desperdicio de agua, sobrecostos en energía eléctrica/combustible y afectaciones en el rendimiento de los cultivos por exceso o falta de riego.

Muestra alta receptividad hacia una solución tecnológica orientada a la gestión móvil (smartphone) que emita alertas puntuales. Para la gestión hídrica, prefiere recibir notificaciones por diferencia de caudal con la opción de cerrar las válvulas de manera remota/manual antes de habilitar un automatizado total. En el ámbito fitosanitario, valora la detección por cámara que envíe la imagen, el tipo de plaga y el sector afectado para ejecutar intervenciones focalizadas. Comercialmente, solicita un modelo de entrada accesible mediante alquiler, suscripción mensual o un pago inicial por instalación con mantenimiento económico, evaluando la compra definitiva tras comprobar el ahorro de recursos e insumos.

#### Entrevista 2

<img width="1102" height="618" alt="Captura de pantalla Entrevista 2" src="https://i.postimg.cc/W30DmYNn/Captura-de-pantalla-(384).png" />

**URL:** https://upcedupe-my.sharepoint.com/:v:/g/personal/u202222846_upc_edu_pe/IQCAaAcW1oK_Tqof8YVhn2hPAeoTG09J7UKSdoKXZTXxL40?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=cwsQ3o 

**Nombre:** Michael Quispe

**Edad:** 24

**Residencia:** Cañete, Lima

**Segmento Objetivo:** Asistente Técnico de Riego

**Duración:** 04:00 minutos

**Resumen:** El usuario validó la necesidad urgente de automatizar la detección de fugas, indicando que actualmente dependen de recorridos físicos que retrasan la respuesta, lo que genera desperdicio de agua y daño al cultivo. Confirmó que la propuesta de recibir alertas móviles, evidencias fotográficas y opciones de cierre remoto reduciría significativamente el tiempo de reacción, validando la viabilidad y necesidad del proyecto AgroLeak en campo.

### 2.2.3. Análisis de entrevistas

## 2.3. Needfinding

El Needfinding organiza los hallazgos disponibles sobre la supervisión del riego y la sanidad vegetal. Su base empírica son los resúmenes de la **Entrevista 1 al Ing. Vega y la Entrevista 2 a Michael Quispe**, registrados en [2.2.2](#registro-de-entrevistas). La muestra disponible es **n = 2**; si bien aporta perspectivas complementarias (desde la administración y desde la asistencia técnica), no permite afirmar que los hallazgos representen estadísticamente a todos los integrantes de los [dos segmentos objetivo](01-capitulo-1.md#13-segmentos-objetivo).

**Alcance y criterio de evidencia.** Se revisaron los capítulos del informe, los assets existentes y la rama `ENTREVISTAS`, que contiene los registros documentales. No se localizaron transcripciones completas ni minutajes exactos, por lo que se utilizan paráfrasis de los resúmenes, sin citas textuales ni marcas de tiempo inventadas. Las preguntas de 2.2.1 y las hipótesis del capítulo I no se tratan como respuestas de participantes.

Cada afirmación remite a un identificador de evidencia. **E** indica un dato explícito del resumen, **I** una interpretación del equipo pendiente de validar y **N/D** información no documentada. Los artefactos de UXPressia se construyeron con la evidencia de E1. E2 corrobora los dolores de detección tardía, pero corresponde a un rol técnico operativo distinto, por lo que su persona y su mapa de empatía quedan *Por confirmar*. El segmento 2 (jefes de operaciones y administradores de fundo) no tiene entrevista.

Los identificadores **E1** remiten a la Entrevista 1 (Ing. Vega) y los identificadores **E2** remiten a la Entrevista 2 (Michael Quispe). No representan participantes adicionales fuera de los mencionados.

| ID | Evidencia disponible en los resúmenes | Ubicación en el registro |
| :--- | :--- | :--- |
| <a id="e1-a"></a>E1-A | Ing. Vega, 27 años, residente en Palpa, Ica; administra una empresa agrícola de 8 hectáreas de palta y cítricos con riego por goteo, bombeo y válvulas por sector. | Datos de identificación y primer párrafo del resumen E1. |
| <a id="e1-b"></a>E1-B | La verificación del riego y la inspección de plagas son manuales. Se describen problemas frecuentes de mangueras desacopladas, fugas o goteros obstruidos; su detección puede tardar horas o hasta el siguiente turno. | Primer párrafo del resumen E1. No se documenta una frecuencia numérica. |
| <a id="e1-c"></a>E1-C | Los incidentes generan desperdicio de agua, sobrecostos de electricidad/combustible y afectaciones del rendimiento por exceso o falta de riego. | Primer párrafo del resumen E1. No se cuantifican pérdidas. |
| <a id="e1-d"></a>E1-D | Receptividad hacia gestión móvil y alertas puntuales. Prefiere avisos por diferencia de caudal y cierre remoto/manual antes de habilitar automatización total. | Segundo párrafo del resumen E1. Preferencia futura, no herramienta actual. |
| <a id="e1-e"></a>E1-E | Valora recibir imagen, tipo de plaga y sector afectado para orientar intervenciones focalizadas. | Segundo párrafo del resumen E1. No acredita que ya utilice cámaras o IA. |
| <a id="e1-f"></a>E1-F | Solicita entrada accesible por alquiler, suscripción o instalación con mantenimiento económico; evaluaría la compra después de comprobar ahorro de recursos e insumos. | Segundo párrafo del resumen E1. Sin presupuesto ni disposición de pago cuantificados. |
| <a id="e2-a"></a>E2-A | Michael Quispe, 24 años, residente en Cañete, Lima; se desempeña como Asistente Técnico de Riego. | Datos de identificación del resumen E2. |
| <a id="e2-b"></a>E2-B | La detección de fugas en la operación diaria depende exclusivamente de la realización de recorridos físicos por las parcelas. | Primer tramo del resumen E2. Denota una limitación y dependencia operativa limitante (I). |
| <a id="e2-c"></a>E2-C | La dependencia de inspecciones presenciales genera una latencia perjudicial, retrasando significativamente la capacidad de respuesta ante anomalías hidráulicas. | Primer tramo del resumen E2. Confirma el dolor (pain point) de ineficiencia temporal descrito en la problemática (I). |
| <a id="e2-d"></a>E2-D | Las consecuencias directas de esta detección tardía se traducen en dos frentes: pérdida económica por desperdicio de agua y afectación agronómica por daño directo al cultivo. | Primer tramo del resumen E2. No se especifican métricas exactas del volumen de agua perdida ni del porcentaje de merma (N/D). |
| <a id="e2-e"></a>E2-E | Valora como urgente y altamente necesaria la automatización del proceso de detección para superar las limitaciones del recorrido físico. | Primer y segundo tramo del resumen E2. |
| <a id="e2-f"></a>E2-F | Confirmación de que la combinación de alertas móviles, evidencias fotográficas (monitoreo) y opciones de cierre remoto (actuación) lograría reducir drásticamente el tiempo de reacción operativa. | Segundo tramo del resumen E2. Valida directamente la hipótesis de valor de AgroLeak (solución IoT de ciclo cerrado). |
| <a id="e2-g"></a>E2-G | Conclusión general del usuario: la plataforma AgroLeak es una solución viable, coherente con la realidad del campo y representa una necesidad real para el personal técnico. | Cierre del resumen E2. Disposición positiva hacia la adopción tecnológica (I). |

**Proyectos en UXPressia** (espacio de trabajo del equipo; requieren acceso):

| Entregable | Enlace |
| :--- | :--- |
| User Persona P1 | [Ing. Vega · Productor tecnificado (P1)](https://uxpressia.com/w/undLx/p/9lwEE) |
| User Task Matrix | [User Task Matrix · AgroLeak](https://uxpressia.com/w/undLx/m/e2tit) |
| Journey J1 (As-Is) | [Supervisión del riego](https://uxpressia.com/w/undLx/m/eAS51) |
| Journey J2 (As-Is) | [Inspección de plagas](https://uxpressia.com/w/undLx/m/sJ3Vm) |
| Empathy Map P1 | [Empathy Map P1 · Ing. Vega](https://uxpressia.com/w/undLx/p/SldzD) |

### 2.3.1. User Personas

Se construyó una persona por segmento respaldado por evidencia. **P1 · Ing. Vega** representa al segmento 1 (pequeños y medianos agricultores tecnificados) y usa el formato nativo de persona de UXPressia: nombre, demografía, objetivos, cita, antecedentes, motivaciones, frustraciones y tecnología.

Solo se registraron atributos documentados en E1-A a E1-F. El género, los ingresos, el estado civil, el sistema operativo y los canales actuales quedan como N/D, y no se usó fotografía para no atribuir una identidad ficticia. La cita es una paráfrasis de E1-D. La sección *Evidencia y límites* de la ficha deja constancia de estas restricciones.

La **Entrevista 2** (Michael Quispe, Asistente Técnico de Riego) corrobora la detección tardía por recorridos físicos ([E2-B](#e2-b), [E2-C](#e2-c)), pero describe un rol técnico operativo. Su persona en UXPressia queda *Por confirmar*. El segmento 2 (jefaturas y administración de fundo) aún no tiene entrevista.

![User Persona P1 en UXPressia](../assets/images/needfinding/uxpressia-persona-p1.png)

*Figura 2.3.1. User Persona P1 · Ing. Vega. Fuente: E1-A a E1-F. Elaborado en [UXPressia](https://uxpressia.com/w/undLx/p/9lwEE).*

### 2.3.2. User Task Matrix

UXPressia no ofrece un módulo específico de matriz de tareas, por lo que se elaboró como un mapa de UXPressia en formato de tabla. Las **filas** son tareas del usuario y las **columnas** son perfiles (P1 y segmento 2), cada una dividida en *Frecuencia* e *Importancia*, más una columna de estado y evidencia.

La frecuencia solo se expresa en los términos que admite el resumen; donde la periodicidad no está documentada se indica N/D. La importancia es una **inferencia** del equipo basada en el impacto o en la preferencia declarada. Todas las celdas del segmento 2 figuran como *Por confirmar*.

| Tarea | P1 · Frecuencia | P1 · Importancia | Segmento 2 | Estado · evidencia |
| :--- | :--- | :--- | :--- | :--- |
| T01. Verificar el riego por sector | Actual; periodicidad N/D | Alta (I) | Por confirmar | Actual · [E1-A](#e1-a), [E1-B](#e1-b), [E1-C](#e1-c) |
| T02. Detectar desacoples, fugas u obstrucciones | Frecuentes; detección en horas o turno siguiente | Alta (I) | Por confirmar | Actual · [E1-B](#e1-b), [E1-C](#e1-c) |
| T03. Inspeccionar plagas | Actual; periodicidad N/D | Relevante (I) | Por confirmar | Actual · [E1-B](#e1-b), [E1-E](#e1-e) |
| T04. Decidir cierre remoto/manual ante aviso de caudal | No aplica al As-Is | Relevante (I) | Por confirmar | Futura deseada · [E1-D](#e1-d) |
| T05. Revisar imagen, tipo de plaga y sector | No aplica al As-Is | Relevante (I) | Por confirmar | Futura deseada · [E1-E](#e1-e) |
| T06. Evaluar ahorro y modalidad de adquisición | Ocasional (I) | Alta (I) | Por confirmar | Criterio de adopción · [E1-F](#e1-f) |
| T07. Coordinar personal, autorizar y consolidar reportes | N/D | N/D | Por confirmar | Por investigar · guion 2.2.1 |

![User Task Matrix en UXPressia](../assets/images/needfinding/uxpressia-task-matrix.png)

*Figura 2.3.2. User Task Matrix. Elaborada en [UXPressia](https://uxpressia.com/w/undLx/m/e2tit).*

### 2.3.3. User Journey Mapping

Se elaboraron dos journeys **As-Is**, que describen el proceso actual del caso E1 antes de AgroLeak. Cada uno incluye etapas, objetivos, acciones, touchpoints, problemas, emociones, oportunidades y curva de experiencia.

Solo se registran como touchpoints los elementos físicos documentados. No se agregaron herramientas actuales (WhatsApp, cuadernos, software) porque la entrevista no las menciona. Las etapas sin información se marcan N/D. Las emociones y la curva de experiencia son interpretaciones del equipo (I), pendientes de validar con el usuario.

- **J1 · Supervisión del riego:** operación del riego → verificación manual → detección tardía del incidente → atención y corrección (N/D).
- **J2 · Inspección de plagas:** inspección manual del cultivo → identificación del hallazgo → decisión de intervención → seguimiento. Las tres últimas etapas son mayormente N/D.

![Journey J1 As-Is en UXPressia](../assets/images/needfinding/uxpressia-journey-j1-riego.png)

*Figura 2.3.3a. Journey J1 As-Is · Supervisión del riego. Elaborado en [UXPressia](https://uxpressia.com/w/undLx/m/eAS51).*

![Journey J2 As-Is en UXPressia](../assets/images/needfinding/uxpressia-journey-j2-plagas.png)

*Figura 2.3.3b. Journey J2 As-Is · Inspección de plagas. Elaborado en [UXPressia](https://uxpressia.com/w/undLx/m/sJ3Vm).*

La principal oportunidad es reducir el tiempo hasta advertir un incidente de riego sin quitarle al usuario el control de la decisión ([E1-D](#e1-d)). La atención actual de incidentes y el ciclo fitosanitario deben reconstruirse en la siguiente ronda de entrevistas.

### 2.3.4. Empathy Mapping

El mapa de empatía de P1 usa la plantilla *Empathy map* de UXPressia, con las secciones ¿con quién empatizamos?, qué necesita hacer, qué ve, qué dice, qué hace, qué escucha, qué piensa y siente, *pains* y *gains*. Lo que dice se presenta como paráfrasis. En *piensa y siente* se separa la receptividad reportada (E1-D) de las interpretaciones (I). La sección *qué escucha* queda N/D porque la entrevista no documenta influencias de terceros. No se elaboró un mapa para el segmento 2 por falta de evidencia.

![Empathy Map P1 en UXPressia](../assets/images/needfinding/uxpressia-empathy-map-p1.png)

*Figura 2.3.4. Empathy Map P1 · Ing. Vega. Elaborado en [UXPressia](https://uxpressia.com/w/undLx/p/SldzD).*

## 2.4. Big Picture EventStorming

El Big Picture EventStorming se construyó en **Miro** tomando como fuente la lógica implementada en la aplicación web de AgroLeak ([AgroLeak-webapp](https://github.com/upc-pre-202620-AgroLeak-Final-Project/AgroLeak-webapp), Angular) y en la API que consume ([AgroLeak-backend](https://github.com/upc-pre-202620-AgroLeak-Final-Project/AgroLeak-backend), Spring Boot). Los eventos, reglas y umbrales del tablero corresponden a validaciones existentes en esos repositorios. Lo que el código no define se registró como hotspot rojo *Por confirmar*. Web, móvil e IoT se tratan como canales y no como Bounded Contexts, y no se asumen microservicios: el backend es un monolito modular.

**Tablero:** [AgroLeak · Big Picture Event Storming en Miro](https://miro.com/app/board/uXjVHZuDZWk=/). El trabajo está en la zona inferior del tablero, debajo del contenido previo, ordenado del Paso 1 al Paso 10.

**Leyenda (convención de EventStorming):** naranja = evento de dominio (en pasado); azul = comando; amarillo claro = actor (persona); rosado = sistema externo o dispositivo; morado = política o regla de negocio; verde = *read model*; amarillo = agregado; rojo = *pain point* / Por confirmar; línea roja vertical = evento pivote.

### 2.4.1. Proceso de modelado

El tablero sigue los diez pasos de EventStorming que solicita el curso. Cada paso es un marco acumulativo: conserva los elementos del paso anterior y agrega una nueva capa.

| Paso | Resultado en Miro |
| :--- | :--- |
| 1. Unstructured Exploration | Lluvia libre de 39 eventos de dominio en notas naranjas, redactados en pasado y sin orden. |
| 2. Timelines | Los eventos se ordenan de izquierda a derecha y se eliminan duplicados. Las alternativas y excepciones se apilan bajo el evento principal (p. ej., *Lectura de sensor registrada* / *Lectura rechazada*). |
| 3. Pain Points | Notas rojas con problemas y preguntas abiertas (*Por confirmar*), ubicadas bajo el evento afectado. |
| 4. Pivotal Points | Líneas rojas verticales después de los eventos pivote: *Sesión iniciada*, *Dispositivo asignado a sector*, *Posible fuga detectada*, *Alerta creada* y *Válvula operada (CONFIRMED)*. Delimitan seis fases: acceso; configuración del fundo y dispositivos; monitoreo y detección; plagas, conectividad y alertas; atención y actuación; cierre y análisis. |
| 5. Commands | Notas azules con la acción que provoca cada evento y, encima, el actor que la ejecuta (FARMER, TECHNICIAN, ADMIN). |
| 6. Policies | Notas moradas con las reglas del código que reaccionan a eventos: umbrales de fuga, obstrucción, presión y plagas; deduplicación de alertas; modo MANUAL. |
| 7. Read Models | Notas verdes con la información que el usuario consulta para decidir: perfil, estructura del fundo, dispositivos, telemetría, observaciones, alertas, estado de la válvula y dashboard. |
| 8. External Systems | Notas rosadas con dispositivos y sistemas externos: gateway/sensores IoT, cámara y actuador/válvula. |
| 9. Aggregates | Notas amarillas con las entidades del backend que reciben comandos y emiten eventos: User, Farm, Field, Sector, Crop, Device, SensorReading, IrrigationSettings, ValveCommand, PestObservation y Alert. |
| 10. Bounded Contexts | Los agregados, comandos, eventos, políticas y vistas se reagrupan por responsabilidad en ocho contextos, con flechas *upstream → downstream*. Se complementa con una ficha por contexto y un resumen de decisiones pendientes. |

![Paso 1: Unstructured Exploration](../assets/images/event-storming/miro-paso-01-unstructured-exploration.png)

*Figura 2.4.1.1. Paso 1 · Unstructured Exploration.*

![Paso 2: Timelines](../assets/images/event-storming/miro-paso-02-timelines.png)

*Figura 2.4.1.2. Paso 2 · Timelines.*

![Paso 3: Pain Points](../assets/images/event-storming/miro-paso-03-pain-points.png)

*Figura 2.4.1.3. Paso 3 · Pain Points.*

![Paso 4: Pivotal Points](../assets/images/event-storming/miro-paso-04-pivotal-points.png)

*Figura 2.4.1.4. Paso 4 · Pivotal Points.*

![Paso 5: Commands](../assets/images/event-storming/miro-paso-05-commands.png)

*Figura 2.4.1.5. Paso 5 · Commands.*

![Paso 6: Policies](../assets/images/event-storming/miro-paso-06-policies.png)

*Figura 2.4.1.6. Paso 6 · Policies.*

![Paso 7: Read Models](../assets/images/event-storming/miro-paso-07-read-models.png)

*Figura 2.4.1.7. Paso 7 · Read Models.*

![Paso 8: External Systems](../assets/images/event-storming/miro-paso-08-external-systems.png)

*Figura 2.4.1.8. Paso 8 · External Systems.*

![Paso 9: Aggregates](../assets/images/event-storming/miro-paso-09-aggregates.png)

*Figura 2.4.1.9. Paso 9 · Aggregates.*

![Paso 10: Bounded Contexts](../assets/images/event-storming/miro-paso-10-bounded-contexts.png)

*Figura 2.4.1.10. Paso 10 · Bounded Contexts.*

### 2.4.2. Flujos modelados y reglas de negocio

| Proceso | Secuencia principal (comando → evento) | Reglas tomadas del código | Por confirmar |
| :--- | :--- | :--- | :--- |
| A. Identidad y acceso | Registrar cuenta → *Cuenta registrada*; Iniciar sesión → *Sesión iniciada*; Cerrar sesión → *Sesión cerrada* | Email único; rol inicial FARMER; la API exige JWT; TECHNICIAN solo lee | Asignación de roles TECHNICIAN/ADMIN; recuperación de contraseña |
| B. Estructura agrícola | Crear fundo → Agregar parcela → Agregar sector → Registrar cultivo | El fundo pertenece a quien lo crea; no se elimina un elemento con dependientes | ¿El sector equivale al tramo de riego del capítulo III? |
| C. Dispositivos | Registrar dispositivo → *Dispositivo asignado a sector*; *Dispositivo marcado ONLINE / OFFLINE* | ONLINE al recibir lectura (salvo MAINTENANCE); OFFLINE tras más de 300 s sin actividad | Aprovisionamiento físico, credenciales y firmware |
| D. Telemetría y detección | Registrar lectura → *Snapshot evaluado* → *Posible fuga (LEAK)*, *Posible obstrucción* o *Presión fuera de rango* | Lecturas emparejadas en 120 s; fuga si la entrada es ≥ 3 L/min y la diferencia ≥ 20 %; obstrucción si la salida es ≤ 5 L/min y la presión ≥ 3,2 bar; presión fuera de 1–4 bar | Persistencia antes de alertar; regla para humedad de suelo; MQTT, operación offline y sincronización |
| E. Control de válvula | Solicitar apertura/cierre → *Comando solicitado (PENDING)* → *Comando enviado al actuador* → *Válvula operada (CONFIRMED)* o *Ejecución fallida (FAILED)* | Solo en modo MANUAL; solo VALVE o GATEWAY; un comando pendiente por válvula; no se cambia de modo con un comando pendiente | AUTO_SAFE (cierre automático ante LEAK); canal real al actuador; timeout; alerta ante FAILED; reapertura tras inspección |
| F. Plagas | Registrar observación → *Plaga detectada (PestDetected)* u *Observación bajo umbral* | PestDetected si el conteo es ≥ 5 y la confianza ≥ 0,7 | Visión artificial real; validación humana (inferencia ≠ plaga confirmada); control localizado |
| G. Alertas | *Alerta creada* → Reconocer → Resolver | No se crea una alerta si ya hay otra del mismo tipo sin resolver; una alerta resuelta no puede reconocerse | Notificaciones push/WhatsApp; escalamiento; origen de la severidad CRITICAL |
| H. Analítica y demo | Consultar dashboard y gráficos (*read models*); Ejecutar escenario demo → *Escenario demo ejecutado* | La pérdida estimada es la diferencia de caudal; el escenario demo solo inyecta lecturas | Línea base para afirmar ahorro; reportes exportables |

Se distinguen la **solicitud** (*Comando de válvula solicitado*), la **ejecución** (*Comando enviado al actuador*) y la **confirmación** (*Válvula operada · CONFIRMED* o *Ejecución fallida · FAILED*). En la versión actual, la confirmación la simula el usuario desde la web.

### 2.4.3. Bounded Contexts identificados

Los límites coinciden con los módulos del backend y de la aplicación web, porque cada uno conserva sus propias reglas e información.

| Bounded Context | Responsabilidad | Términos propios | Relaciones |
| :--- | :--- | :--- | :--- |
| IAM | Registro, autenticación JWT, roles y perfil | Usuario, rol, token | *Upstream* de todos: identidad y rol del usuario |
| Farm Management | Farm → Field → Sector → Crop y pertenencia | Fundo, parcela, sector, cultivo | *Upstream* de Devices, Pest Monitoring y Alerts |
| Devices | Inventario IoT y estado operativo | Dispositivo, tipo, ONLINE/OFFLINE, lastSeen | *Upstream* de Monitoring, Irrigation y Pest Monitoring; origina DEVICE_OFFLINE |
| Monitoring | Lecturas validadas y detección de fuga, obstrucción y presión | Lectura, snapshot, ventana, umbral | *Upstream* de Alerts y Analytics |
| Irrigation | Modo de operación y ciclo del comando de válvula | Comando OPEN/CLOSE, PENDING/CONFIRMED/FAILED, MONITOR_ONLY/MANUAL/AUTO_SAFE | *Downstream* de Devices; vínculo con LEAK por confirmar (AUTO_SAFE) |
| Pest Monitoring | Observaciones de plaga y evento PestDetected | Observación, conteo, confianza | Publica PestDetected hacia Alerts |
| Alerts | Alertas sin duplicados, reconocimiento y resolución | Alerta, tipo, severidad, estado | *Downstream* de Monitoring, Devices y Pest Monitoring |
| Analytics | Vistas de lectura: dashboard y gráficos | Consumo, pérdida estimada, KPI | Consume a los demás; no controla dispositivos |

![Fichas y resumen de Bounded Contexts](../assets/images/event-storming/miro-paso-10b-fichas-y-resumen.png)

*Figura 2.4.3. Paso 10 (detalle) · Ficha de cada Bounded Context y resumen de decisiones pendientes.*

### 2.4.4. Decisiones pendientes (Por confirmar)

1. Quién asigna los roles TECHNICIAN y ADMIN; recuperación de contraseña.
2. Si el *Sector* equivale al tramo de riego del capítulo III; fundos con varios usuarios (segmento 2).
3. Aprovisionamiento físico, credenciales y firmware de los dispositivos.
4. Persistencia temporal antes de alertar una fuga (el backend evalúa cada snapshot).
5. Regla de negocio para la humedad de suelo (se registra, pero no se evalúa).
6. Transporte real MQTT/streaming, operación sin conectividad y sincronización Edge.
7. Canal real al actuador y confirmación automática (hoy simulada).
8. Timeout y alerta cuando un comando queda PENDING o termina FAILED.
9. AUTO_SAFE: cierre automático ante LEAK (preparado, no implementado).
10. Reapertura tras inspección y efecto real de MONITOR_ONLY.
11. Visión artificial real (Edge AI) que genere las observaciones.
12. Validación humana o de especialista: distinguir inferencia de plaga confirmada.
13. Control localizado de plagas (US14–US15), sin implementación.
14. Notificaciones push/WhatsApp y escalamiento de alertas no atendidas.
15. Qué regla genera la severidad CRITICAL.
16. Línea base para afirmar ahorro de agua o energía; reportes exportables.
17. *Actuation Safety* ([capítulo IV](04-capitulo-4.md#4111-candidate-context-discovery)) no existe como contexto en el código: decidir si se mantiene como BC o se integra en Irrigation.
18. Alcance de la aplicación móvil (el repositorio AgroLeak-android solo contiene un README).

## 2.5. Ubiquitous Language
