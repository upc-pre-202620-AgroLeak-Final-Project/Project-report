# Capítulo V: Solution UI/UX Design

## 5.1. Style Guidelines

Las guías de estilo buscan que el productor identifique rápidamente qué ocurre, dónde ocurre y qué puede hacer sin interpretar términos ambiguos. El diseño evita presentar una anomalía de caudal como fuga confirmada o una inferencia visual como diagnóstico definitivo. Cuando existe una acción física disponible, la interfaz muestra primero la evidencia, el modo de actuación y los límites aplicables.

### 5.1.1. General Style Guidelines


| **Principio**             | **Aplicación en AgroLeak**                                                                   |
|---------------------------|----------------------------------------------------------------------------------------------|
| Claridad operativa        | Cada pantalla prioriza estado, ubicación, hora y siguiente acción.                           |
| Seguridad visible         | Las decisiones físicas muestran autorización, interlocks, duración y resultado.              |
| Evidencia antes de acción | Las alertas incluyen lecturas o imagen, confianza, repetición y regla aplicada.              |
| Control humano            | El usuario puede elegir MONITOR_ONLY, MANUAL_APPROVAL o SAFE_AUTO_DEMO.                      |
| Trazabilidad              | Cada evento conserva origen, dispositivo, actor, timestamp y resultado.                      |
| Uso en campo              | Tipografía legible, objetivos táctiles amplios, contraste alto y estados offline explícitos. |
| Consistencia              | Web, móvil y dispositivo utilizan los mismos nombres, severidades y estados.                 |

Identidad visual
La identidad combina un fondo verde oscuro asociado con el campo y el control, un verde menta para estados activos y un ámbar para advertencias que requieren revisión. El símbolo de gota comunica la relación con el riego; su uso no implica que la marca se limite a fugas, porque se acompaña con referencias visuales a visión artificial y protección del cultivo.

Token	Valor	Uso principal
Field Night	#071A18	Encabezados, navegación y fondos de alto contraste.
Control Green	#247A59	Acciones confirmadas, bordes y navegación activa.
Active Mint	#67E8A5	CTA principal, operación correcta y conectividad.
Alert Amber	#F4B942	Posible fuga, revisión requerida y autorización pendiente.
Surface Cream	#F5F7F2	Fondos de lectura y separación de secciones.
Ink	#0B1F2A	Texto principal sobre superficies claras.
Interface Blue	#1F4E79	Información, historial, recuperación y documentación.
La tipografía propuesta es Inter para productos digitales, con Arial o Segoe UI como alternativas de sistema. Los títulos usan peso 700 u 800; el cuerpo usa 400 o 500; los valores críticos usan 700. Se evita escribir párrafos completos en mayúsculas. Las etiquetas breves de estado pueden usar mayúsculas cuando mantienen legibilidad.

Los iconos son lineales y se acompañan con texto. Ningún estado depende únicamente del color: un evento incluye icono, etiqueta y descripción. Las fotografías deben mostrar contextos agrícolas reales, equipos instalados y zonas observadas; no deben sugerir precisión, rendimiento ni disponibilidad que todavía no hayan sido validados.

![AgroLeak Visual Style Guide](../assets/cap5/agroleak-visual-style-guide.png)

*AgroLeak Visual Style Guide*

#### Componentes y estados

| **Componente**         | **Regla de diseño**                                                                               |
|------------------------|---------------------------------------------------------------------------------------------------|
| Botón primario         | Una acción principal por vista; verbo explícito como Autorizar, Guardar o Solicitar demostración. |
| Botón secundario       | Alternativa reversible como Revisar evidencia, Cancelar o Volver.                                 |
| Tarjeta de estado      | Identifica sector, fuente, último dato válido y estado operativo.                                 |
| Alerta                 | Incluye severidad, origen, evidencia, fecha y acción disponible.                                  |
| Confirmación de acción | Resume el actuador, duración, límite y efecto esperado antes de confirmar.                        |
| Estado vacío           | Explica por qué no hay datos y ofrece una acción concreta.                                        |
| Estado offline         | Indica qué continúa operando localmente y qué información está pendiente de sincronizar.          |
| Error                  | Evita culpar al usuario; explica el problema, lo conservado y el siguiente paso seguro.           |


### 5.1.2. Web, Mobile and IoT Style Guidelines

| **Superficie**     | **Criterios de diseño**                                                                                                                    |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Landing Page       | Narrativa comercial vertical, navegación por anclas, CTA visible, contenido responsive y explicación transparente de alcances y seguridad. |
| Web Application    | Densidad moderada, navegación lateral, filtros persistentes, comparación de series, evidencia ampliable y soporte completo de teclado.     |
| Mobile Application | Prioridad a alertas, evidencia y aprobaciones; objetivos táctiles mínimos de 44 px; flujos cortos y estados offline visibles.              |
| IoT Device         | Etiquetas físicas resistentes, LEDs con texto o leyenda, parada manual accesible, cableado identificado y estado seguro por defecto.       |

**Web Application.** El dashboard presenta un resumen de la granja y permite profundizar por parcela, tramo, punto de observación, alerta o período. Las gráficas no sustituyen los valores numéricos ni las unidades. Los controles de apertura, cierre o actuación se separan de los filtros de lectura y requieren confirmación cuando cambian un estado físico.

**Mobile Application.** La experiencia móvil se orienta a decisiones en campo. La pantalla inicial muestra alertas abiertas, sincronización y estado de dispositivos. Una autorización exige abrir la evidencia y confirmar la acción; no se permite ejecutar una acción física con un único toque accidental. Si se pierde conectividad, la aplicación diferencia los datos almacenados en el teléfono de la operación que sigue ejecutándose en el Edge.

**IoT Device.** La interfaz física emplea una carcasa rotulada, indicadores de alimentación, conectividad, operación y bloqueo, además de una parada manual. El verde indica operación normal, el ámbar solicita revisión y el rojo identifica bloqueo o falla; cada color debe tener una etiqueta o patrón de parpadeo documentado. La disposición evita que una persona confunda la electroválvula hidráulica con el actuador localizado del punto de observación.


## 5.2. Information Architecture

La arquitectura de información combina organización jerárquica, organización por tareas y orden cronológico. La jerarquía principal es Granja \> Parcela \> Tramo de riego o Punto de observación \> Evento. Las tareas prioritarias son monitorear, revisar evidencia, autorizar, resolver y consultar historial. Dentro de una alerta o historial, los eventos se muestran del más reciente al más antiguo.

![AgroLeak Information Architecture](../assets/cap5/information-architecture.png)

### 5.2.1. Organization Systems

| **Sistema de organización** | **Aplicación**                                          | **Ejemplo**                                         |
|-----------------------------|---------------------------------------------------------|-----------------------------------------------------|
| Jerárquico                  | Ubicación física y pertenencia de dispositivos.         | Granja Norte \> Parcela 2 \> Tramo 02.              |
| Orientado a tareas          | Acciones frecuentes del productor.                      | Revisar alerta, autorizar acción, cerrar incidente. |
| Cronológico                 | Eventos, telemetría, comandos y auditoría.              | Historial de las últimas 24 horas.                  |
| Por estado                  | Priorización operativa.                                 | Normal, revisión requerida, bloqueado, offline.     |
| Por fuente                  | Diferencia entre circuito hidráulico y circuito visual. | Caudal, plaga, actuador, sistema.                   |

La Landing Page utiliza una organización secuencial: propuesta de valor, problema, dos circuitos de protección, funcionamiento, seguridad, kit, preguntas y CTA. La aplicación web utiliza una organización jerárquica y por tareas. La aplicación móvil simplifica la jerarquía y prioriza alertas, evidencia y aprobaciones. El dispositivo IoT expone únicamente estados operativos y controles de seguridad.

### 5.2.2. Labeling Systems

Las etiquetas evitan absolutos no demostrados y mantienen correspondencia con el lenguaje ubicuo del capítulo II.

| **Concepto interno**  | **Etiqueta para el usuario**           | **Etiqueta que debe evitarse**     |
|-----------------------|----------------------------------------|------------------------------------|
| FlowAnomaly           | Posible fuga o anomalía de caudal      | Fuga confirmada                    |
| TargetPestConfirmed   | Plaga objetivo confirmada por la regla | Diagnóstico definitivo             |
| PestInference         | Detección de IA                        | Plaga eliminada                    |
| ValveClosureRequested | Cierre preventivo solicitado           | Reparación automática              |
| SafetyLockout         | Bloqueo de seguridad                   | Error desconocido                  |
| PendingSync           | Pendiente de sincronización            | Información perdida                |
| MANUAL_APPROVAL       | Requiere aprobación                    | Acción automática                  |
| SAFE_AUTO_DEMO        | Demostración automática segura         | Aplicación automática de pesticida |

Los botones utilizan verbos específicos: Revisar evidencia, Autorizar, Rechazar, Cerrar válvula, Registrar inspección, Reabrir después de inspección y Marcar como resuelta. Se evita Aceptar cuando no comunica el efecto de la acción.

### 5.2.3. SEO Tags and Meta Tags

La estrategia SEO corresponde únicamente a la Landing Page pública. Las aplicaciones autenticadas no deben indexarse.

| **Elemento**            | **Propuesta**                                                                                                                                               |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| lang                    | es-PE para la versión inicial; preparar recursos para inglés.                                                                                               |
| title                   | AgroLeak \| Detecta fugas y plagas. Actúa a tiempo.                                                                                                         |
| description             | AgroLeak detecta posibles fugas y una plaga objetivo con sensores, visión artificial y acciones localizadas para proteger el cultivo desde el propio campo. |
| viewport                | width=device-width, initial-scale=1                                                                                                                         |
| theme-color             | \#071A18                                                                                                                                                    |
| Encabezado principal    | Un solo h1 centrado en la propuesta de valor.                                                                                                               |
| Encabezados secundarios | Jerarquía semántica h2 y h3 sin saltos.                                                                                                                     |
| Texto alternativo       | Describe propósito y contenido de la imagen, no su apariencia decorativa.                                                                                   |
| Open Graph              | Título, descripción e imagen social cuando exista un recurso aprobado.                                                                                      |
| robots                  | index, follow solo al publicar una versión comercial revisada.                                                                                              |

Las palabras clave se incorporan de manera natural en el contenido: monitoreo de riego, detección de fugas agrícolas, cámara con inteligencia artificial, monitoreo de plagas, IoT agrícola y control localizado. No se repiten como listas ocultas ni se realizan afirmaciones de rendimiento sin evidencia.

### 5.2.4. Searching Systems

La Landing Page no requiere buscador por su extensión; la navegación por anclas y las preguntas frecuentes cubren la localización de contenido. Las aplicaciones sí requieren búsqueda contextual y filtros.

| **Área**            | **Criterios de búsqueda y filtrado**                                  |
|---------------------|-----------------------------------------------------------------------|
| Granjas y parcelas  | Nombre, código o ubicación registrada.                                |
| Dispositivos        | Device ID, tipo, estado, parcela y última comunicación.               |
| Alertas             | Estado, severidad, fuente, parcela, rango de fechas y texto.          |
| Historial           | Tipo de evento, actor, dispositivo, resultado y período.              |
| Evidencias de plaga | Punto de observación, clase, rango de confianza, validación y modelo. |

La búsqueda muestra coincidencias mientras el usuario escribe solo cuando existen datos locales suficientes. En conexión limitada, se indica que los resultados corresponden a información sincronizada. Los filtros activos permanecen visibles y pueden restablecerse con una sola acción.


### 5.2.5. Navigation Systems

| **Superficie**     | **Navegación principal**                                                   | **Navegación contextual**                                 |
|--------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| Landing Page       | Anclas: solución, funcionamiento, kit, seguridad y preguntas.              | CTA hacia demostración o piloto.                          |
| Web Application    | Barra lateral: resumen, riego, plagas, alertas, historial y configuración. | Breadcrumb de granja, parcela y elemento.                 |
| Mobile Application | Barra inferior: inicio, alertas, evidencia y cuenta.                       | Acciones dentro del detalle de alerta.                    |
| IoT Device         | Sin navegación jerárquica.                                                 | Botón de prueba controlada, parada y reinicio autorizado. |

El sistema conserva la ubicación del usuario al volver desde una evidencia. Las rutas protegidas redirigen al inicio de sesión y regresan al destino original después de autenticarse. La acción Atrás nunca ejecuta ni revierte un comando físico.


## 5.3. Landing Page UI Design

### 5.3.1. Landing Page Wireframe

Los wireframes de la landing page representan la estructura y jerarquía de sus secciones antes de aplicar el diseño visual final. Permiten revisar la navegación, la presentación de la propuesta de valor y la ubicación de las llamadas a la acción.

> Insertar aquí las imágenes de los wireframes de la landing page cuando se incorporen a `assets/cap5`.

### 5.3.2. Landing Page Mock-up

Los siguientes mockups muestran la propuesta visual de la landing page de AgroLeak. En conjunto presentan la solución, explican su funcionamiento y el kit, muestran el contexto de uso en campo, detallan los precios referenciales y permiten solicitar una demostración.

#### Sección de inicio

La pantalla inicial introduce la propuesta de valor de AgroLeak: proteger el agua y el cultivo mediante monitoreo local y control humano. Incluye la navegación principal, llamadas a solicitar una demostración y una vista resumida de la detección de una diferencia de caudal.

<img src="../assets/cap5/landing-mockup-1.jpg.png" alt="Mockup de inicio de la landing page de AgroLeak" width="100%">

#### Sección de solución

Esta sección presenta los dos problemas que atiende la solución: las diferencias de caudal en el riego y las señales visuales de posibles plagas. Explica el uso de evidencia y revisión, evitando presentar una inferencia como diagnóstico definitivo.

<img src="../assets/cap5/landing-mockup-2.jpg.png" alt="Mockup de la sección de solución de AgroLeak" width="100%">

#### Sección de funcionamiento y kit

El diseño describe el flujo general de la solución —sensar, validar, actuar y trazar— y presenta los componentes principales del kit IoT propuesto para el MVP.

<img src="../assets/cap5/landing-mockup-3.jpg.png" alt="Mockup del funcionamiento y kit IoT de AgroLeak" width="100%">

#### Sección de contexto de uso en campo

La sección relaciona la interfaz con el entorno agrícola mediante imágenes de operación, riego localizado y evidencia visual de plagas. Su objetivo es explicar cómo la tecnología acompaña la revisión del productor.

<img src="../assets/cap5/landing-mockup-4.jpg.png" alt="Mockup de contexto de uso de AgroLeak en campo" width="100%">

#### Sección de precios referenciales

Esta vista comunica una propuesta referencial de pago por el kit y planes de suscripción. Los precios se presentan como parte del mockup y deben validarse antes de tratarse como una oferta comercial definitiva.

<img src="../assets/cap5/landing-mockup-6.jpg.png" alt="Mockup de precios referenciales de AgroLeak" width="100%">

#### Sección de solicitud de demostración

El formulario permite que una persona interesada registre información de contacto y datos generales de su operación agrícola para solicitar una demostración o piloto.

<img src="../assets/cap5/landing-mockup-5.jpg.png" alt="Mockup del formulario para solicitar una demostración de AgroLeak" width="100%">
## 5.4. Applications UX/UI Design

### 5.4.1. Applications Wireframes

Los wireframes de la aplicación web muestran la estructura de las pantallas operativas de AgroLeak antes del acabado visual. Las vistas cubren el acceso a la plataforma y los módulos de gestión, monitoreo y atención de alertas.

#### Acceso a la aplicación

El wireframe de inicio de sesión organiza los campos de acceso y la entrada al centro de operaciones. El wireframe de registro presenta la creación de una cuenta para utilizar la plataforma.

<img src="../assets/cap5/wireframe-login.png" alt="Wireframe de inicio de sesión de la aplicación web AgroLeak" width="100%">

<img src="../assets/cap5/wireframe-registro.png" alt="Wireframe de registro de usuario de la aplicación web AgroLeak" width="100%">

#### Dashboard

El dashboard resume el estado operativo mediante indicadores, telemetría, alertas y estado de los dispositivos.

<img src="../assets/cap5/wirefram-dashboard.png" alt="Wireframe del dashboard de AgroLeak" width="100%">

#### Gestión de fundos

Esta vista permite consultar los fundos registrados y acceder a la gestión de su estructura agrícola.

<img src="../assets/cap5/wirefram-fundos.png" alt="Wireframe de gestión de fundos" width="100%">

#### Gestión de dispositivos

El wireframe organiza el listado de dispositivos IoT y permite revisar su estado y datos de asociación.

<img src="../assets/cap5/wirefram-dispositivos.png" alt="Wireframe de gestión de dispositivos IoT" width="100%">

#### Monitoreo

La pantalla de monitoreo presenta indicadores de telemetría y un espacio para consultar el historial de lecturas en un periodo seleccionado.

<img src="../assets/cap5/wireframe-monitoreo.png" alt="Wireframe del módulo de monitoreo" width="100%">

#### Alertas

Esta vista agrupa las alertas para facilitar su revisión y priorización según el estado y la severidad.

<img src="../assets/cap5/wireframe-alertas.png" alt="Wireframe del módulo de alertas" width="100%">

#### Control de riego

El wireframe de riego presenta el espacio de interacción con las válvulas y la consulta del resultado reportado por el dispositivo.

<img src="../assets/cap5/wirefram-control-riego.png" alt="Wireframe del módulo de control de riego" width="100%">

#### Monitoreo de plagas

Esta pantalla organiza las observaciones asociadas a cámaras y sectores, y contempla el acceso al registro de una nueva observación.

<img src="../assets/cap5/wireframe-plagas.png" alt="Wireframe del módulo de monitoreo de plagas" width="100%">

#### Perfil de usuario

El wireframe del perfil presenta la información de identidad y rol del usuario dentro de AgroLeak.

<img src="../assets/cap5/wireframe-perfil.png" alt="Wireframe del perfil de usuario" width="100%">

### 5.4.2. Applications Wireflow Diagrams

### 5.4.3. Applications Mock-ups

Los siguientes mockups presentan la propuesta visual de alta fidelidad para las principales pantallas de la aplicación web de AgroLeak. En conjunto, muestran el acceso a la plataforma y los módulos para consultar el estado de la operación, gestionar fundos y dispositivos, monitorear telemetría, revisar alertas y observar los módulos de riego y plagas.

#### Inicio de sesión

La pantalla de inicio de sesión permite al usuario ingresar a la plataforma y acceder al centro de operaciones.

<img src="../assets/cap5/inicio-seion-mockup.jpg" alt="Mockup de inicio de sesión de AgroLeak" width="100%">

#### Registro de usuario

El formulario de registro presenta los campos necesarios para crear una cuenta en AgroLeak.

<img src="../assets/cap5/inicio-sesion-mockup2.jpg" alt="Mockup de registro de usuario de AgroLeak" width="100%">

#### Dashboard

El dashboard ofrece una vista ejecutiva de la operación, con indicadores de consumo y pérdida estimada, alertas activas, plagas detectadas, telemetría y estado de los dispositivos.

<img src="../assets/cap5/dashboard-pricipal-mockup.jpg" alt="Mockup del dashboard principal de AgroLeak" width="100%">

#### Gestión de fundos

La vista de fundos permite consultar las unidades agrícolas registradas y acceder a la gestión de su estructura.

<img src="../assets/cap5/fundos-mockup.jpg" alt="Mockup de gestión de fundos en AgroLeak" width="100%">

#### Gestión de dispositivos IoT

Este módulo presenta el listado de dispositivos registrados y permite revisar datos como su tipo, estado, ubicación y sector asociado.

<img src="../assets/cap5/dispositivos-mockup.jpg" alt="Mockup de gestión de dispositivos IoT en AgroLeak" width="100%">

#### Monitoreo

La pantalla de monitoreo organiza las lecturas de caudal, presión y humedad del suelo, junto con filtros por dispositivo y periodo e historial de telemetría.

<img src="../assets/cap5/monitoreo-mockup.jpg" alt="Mockup del módulo de monitoreo de AgroLeak" width="100%">

#### Alertas

El módulo de alertas permite revisar incidencias y priorizarlas mediante filtros por estado y severidad.

<img src="../assets/cap5/alertas-mockup.jpg" alt="Mockup del módulo de alertas de AgroLeak" width="100%">

#### Control de riego

Esta pantalla presenta el módulo para operar válvulas y consultar la confirmación reportada por los dispositivos.

<img src="../assets/cap5/control-riego-mockup.jpg" alt="Mockup del módulo de control de riego de AgroLeak" width="100%">

#### Monitoreo de plagas

La vista organiza las observaciones de plagas asociadas a cámaras y sectores, y presenta el acceso para registrar una nueva observación.

<img src="../assets/cap5/monitoreo-plagas-mockup.jpg" alt="Mockup del módulo de monitoreo de plagas de AgroLeak" width="100%">

#### Perfil de usuario

El perfil muestra la identidad y el rol del usuario dentro de la aplicación, además de la opción para cerrar sesión.

<img src="../assets/cap5/profile-mockup.jpg" alt="Mockup del perfil de usuario de AgroLeak" width="100%">

### 5.4.4. Applications User Flow Diagrams

A continuación se presenta el User Flow Diagram de la aplicación web AgroLeak. El diagrama representa las rutas de navegación propuestas desde el ingreso a la plataforma hasta las principales tareas operativas, como consultar fundos y parcelas, monitorear el riego, revisar alertas y gestionar dispositivos. Permite visualizar los puntos de decisión y las alternativas de navegación contempladas en el diseño.

<img src="../assets/cap5/applications-user-flow-diagrams.jpg" alt="Diagrama de flujo de usuario de la aplicación web AgroLeak" width="100%">


## 5.5. Applications Prototyping

Los prototipos de AgroLeak deben permitir simular la interacción y la navegación de la aplicación en navegadores web de escritorio y móviles. Las decisiones de interacción se orientan a que el usuario pueda revisar el estado operativo, abrir la evidencia de una alerta y localizar la acción disponible antes de actuar. La navegación y la organización de estas tareas se relacionan con la arquitectura de información de la sección 5.2, en particular con sus sistemas de navegación, y con los criterios de interacción y seguridad definidos en la sección 5.1.

El siguiente User Flow representa las rutas previstas para la aplicación web y orienta los recorridos que deben demostrarse en los prototipos. El diagrama complementa los wireframes y mockups, pero por sí solo no demuestra una simulación de interacción y navegación.

<img src="../assets/cap5/applications-user-flow-diagrams.jpg" alt="Flujo funcional previsto para el prototipo web de AgroLeak" width="100%">

El recorrido contempla que, después de iniciar sesión, el usuario llegue al dashboard y seleccione una tarea operativa. Desde allí puede consultar un fundo o parcela, revisar lecturas y observaciones, inspeccionar una alerta y, cuando corresponda, acceder al control de riego. Las acciones que puedan modificar el estado de un actuador deben presentar evidencia, solicitar autorización cuando aplique y comunicar el resultado recibido del dispositivo.

#### Prototipo en navegador de escritorio



## 5.6. IoT Device Design

Esta sección documenta la propuesta de diseño físico y de circuito de los dispositivos IoT de AgroLeak. El diseño debe mostrar cómo se capturan las lecturas de riego y las imágenes para el monitoreo de plagas, cómo se comunican sus estados y cómo se mantienen las salvaguardas de actuación. Las decisiones de interfaz física deben mantener consistencia con las pautas para dispositivos IoT de la sección 5.1.2; los eventos y estados que se muestran al usuario deben ser coherentes con la arquitectura de información de la sección 5.2.

Para documentar los circuitos se utilizará Wokwi o Cirkit Designer. En cada caso se debe incluir y explicar el diagrama correspondiente y el flujo de interacción del prototipo. El diagrama funcional que se presenta a continuación ayuda a explicar la lógica del nodo de riego, pero no sustituye el diseño físico ni el diagrama detallado del circuito.

### 5.6.1. Flujo de funcionamiento del dispositivo

| **Etapa** | **Protección del riego** | **Monitoreo de plagas** |
|---|---|---|
| Captura | Se obtienen lecturas de caudal en los puntos definidos para el tramo de riego y, si el diseño del nodo lo contempla, otras variables asociadas. | La cámara captura imágenes del cultivo en un punto de observación identificado. |
| Validación local | El Edge valida la calidad de las lecturas y compara los valores conforme a reglas de persistencia y umbrales que deben configurarse y probarse. | El procesamiento de visión artificial analiza la imagen y produce una observación con la clase detectada y su nivel de confianza. |
| Evento | Si la anomalía persiste, se genera un evento de posible fuga o condición anómala; no se presenta como fuga confirmada sin verificación. | Se genera una observación de posible plaga para que el usuario revise la evidencia y el nivel de confianza. |
| Acción y seguridad | Según el modo configurado y las salvaguardas, el sistema puede emitir una solicitud de cierre de válvula. El dispositivo informa el resultado y conserva el estado seguro ante una falla. | La plataforma comunica la observación para su revisión; la inferencia no activa por sí sola una aplicación de pesticidas. |
| Comunicación y trazabilidad | Los eventos, lecturas y resultados de actuación se sincronizan con la plataforma cuando hay conectividad, preservando su origen y marca de tiempo. | La imagen o referencia a la evidencia, la observación y su estado de revisión quedan asociados al punto y al momento de captura. |

La reapertura de una válvula debe requerir las condiciones de autorización y verificación física definidas para el proyecto. Los umbrales, intervalos de muestreo, tiempos de persistencia, comportamiento ante pérdida de conectividad y componentes electrónicos concretos deben documentarse según el diseño y las pruebas realizadas; no se infieren únicamente de este flujo conceptual.

El siguiente esquema resume el flujo propuesto para el nodo de protección del riego: el ESP32 recibe datos de caudal de entrada y salida, presión y humedad del suelo, aplica reglas locales y puede activar una alerta sonora/visual y un actuador. Corresponde al nodo de riego; no representa el subsistema de cámara e identificación de plagas ni detalla conexiones eléctricas.

<img src="../assets/cap5/diagrama-simulacion.png" alt="Esquema funcional del nodo IoT de protección de riego de AgroLeak" width="100%">

*Esquema conceptual del nodo IoT de AgroLeak para monitoreo de riego y respuesta local.*

El servo SG90 que aparece en el esquema debe entenderse como un actuador de demostración para el prototipo o la simulación. No equivale por sí solo a una válvula hidráulica apta para controlar el flujo de agua en campo; la selección e integración del actuador real deberá especificarse y validarse aparte.

### 5.6.2. Diseño físico de los dispositivos IoT

El diseño físico debe mostrar la disposición propuesta de los componentes y de la interfaz local de cada dispositivo, considerando la instalación y el uso en un entorno agrícola. Los indicadores, controles y estados físicos deben seguir las pautas de legibilidad, identificación y operación segura definidas en la sección 5.1.2.



### 5.6.3. Diagramas de circuito y simulación

Para cada dispositivo IoT del alcance, incluir un diagrama de circuito elaborado en Wokwi o Cirkit Designer. El diagrama debe permitir identificar la placa, los sensores y actuadores considerados, sus conexiones y el flujo de interacción que se demostrará. Si se usa Wokwi para simular el circuito, la captura debe corresponder al montaje efectivamente construido y probado; esta simulación no demuestra por sí sola una instalación en campo ni la precisión de los sensores.

