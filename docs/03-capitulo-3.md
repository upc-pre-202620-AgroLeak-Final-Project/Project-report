# Capítulo III: Requirements Specification

## 3.1 User Stories

The following requirements are written in English and follow the professor’s requested structure. Each story includes a role, goal, benefit, and Given-When-Then acceptance criteria. They remain subject to refinement after interviews and prototype tests.

### Epics

| ID | Title | Description |
|---|---|---|
| EP01 | Public Website | Explain AgroLeak and collect qualified demonstration requests. |
| EP02 | Identity and Access | Protect private farm, device, and actuation information. |
| EP03 | Farm and Device Setup | Configure farms, plots, sensors, cameras, and actuators. |
| EP04 | Irrigation Protection | Detect persistent flow anomalies and manage valve closure. |
| EP05 | AI Pest Monitoring | Capture evidence, run inference, and confirm a target pest. |
| EP06 | Safe Actuation | Authorize and execute localized actions under safety limits. |
| EP07 | Alert Management | Notify users and preserve acknowledgment and resolution. |
| EP08 | Analytics and History | Review measurements, detections, actions, and summaries. |
| EP09 | Edge and Synchronization | Continue local operation and synchronize idempotently. |
| EP10 | Weather Context | Present external weather data as complementary context. |

### Visitor Stories

#### US01 - Browse the Public Website

**As a Visitor**, I want to browse AgroLeak’s public website so that I can understand how the product protects irrigation and monitors a target pest.

**Acceptance Criteria:**

- **Scenario: View the value proposition**
  - **Given** the Visitor opens the landing page,
  - **When** the page finishes loading,
  - **Then** it explains the two monitored risks, the IoT process, the safety approach, and the main benefits.

- **Scenario: Browse on a mobile device**
  - **Given** the Visitor uses a mobile device,
  - **When** the Visitor navigates through the page,
  - **Then** the content remains readable and usable without horizontal scrolling.

#### US02 - Request a Product Demonstration

**As a Visitor**, I want to submit my contact information so that I can request an AgroLeak demonstration or pilot conversation.

**Acceptance Criteria:**

- **Scenario: Submit a valid request**
  - **Given** the Visitor completes all required fields with valid information,
  - **When** the Visitor submits the form,
  - **Then** the request is registered and a confirmation message is displayed.

- **Scenario: Submit an incomplete request**
  - **Given** one or more required fields are empty,
  - **When** the Visitor submits the form,
  - **Then** the page identifies the missing fields and does not register the request.

### Registered User Stories

#### US03 - Sign In to the Platform

**As a Registered User**, I want to sign in securely so that I can access the farms and devices assigned to my account.

**Acceptance Criteria:**

- **Scenario: Successful sign-in**
  - **Given** the Registered User has valid credentials,
  - **When** the user submits the sign-in form,
  - **Then** the platform creates an authorized session and displays the dashboard.

- **Scenario: Invalid sign-in attempt**
  - **Given** the credentials are invalid,
  - **When** the user submits the form,
  - **Then** the platform rejects the request without revealing which credential is incorrect.

### Agricultural Producer Stories

#### US04 - Register a Farm and Plot

**As an Agricultural Producer**, I want to register my farm and plots so that I can organize every monitored location.

**Acceptance Criteria:**

- **Scenario: Register valid data**
  - **Given** the Agricultural Producer is signed in and provides the required data,
  - **When** the registration is confirmed,
  - **Then** the farm and plot are stored and associated with the producer.

- **Scenario: Register a duplicate plot name**
  - **Given** a plot with the same name already exists in the farm,
  - **When** the producer submits the duplicate,
  - **Then** the platform rejects it and requests a different name.

#### US05 - Configure an Irrigation Segment

**As an Agricultural Producer**, I want to assign inlet and outlet sensors and a shutoff valve to an irrigation segment so that AgroLeak can monitor and protect it.

**Acceptance Criteria:**

- **Scenario: Assign distinct devices**
  - **Given** two available flow sensors and one valve are registered,
  - **When** the producer assigns them to their roles,
  - **Then** the segment is saved and marked as ready for calibration.

- **Scenario: Reuse the same flow sensor**
  - **Given** the same sensor is selected as inlet and outlet,
  - **When** the producer submits the configuration,
  - **Then** the platform rejects it and explains that two distinct sensors are required.

#### US06 - Configure a Flow Anomaly Rule

**As an Agricultural Producer**, I want to configure a percentage threshold and persistence duration so that anomaly detection reflects the calibrated segment.

**Acceptance Criteria:**

- **Scenario: Save valid parameters**
  - **Given** the segment has been calibrated,
  - **When** the producer enters values within the allowed ranges,
  - **Then** the platform versions and activates the new rule.

- **Scenario: Enter an invalid parameter**
  - **Given** the producer enters a negative threshold or duration,
  - **When** the rule is submitted,
  - **Then** the platform rejects it and keeps the previous active rule.

#### US07 - View Current Irrigation Status

**As an Agricultural Producer**, I want to view inlet flow, outlet flow, difference, and valve status so that I can understand the segment’s current condition.

**Acceptance Criteria:**

- **Scenario: View recent readings**
  - **Given** recent synchronized measurements exist,
  - **When** the producer opens the segment,
  - **Then** the platform displays values, unit, percentage, timestamp, quality, and valve status.

- **Scenario: View stale data**
  - **Given** the latest reading is older than the freshness limit,
  - **When** the producer opens the segment,
  - **Then** the platform marks the data as outdated and displays the last successful time.

#### US08 - Detect a Persistent Flow Anomaly

**As an Agricultural Producer**, I want AgroLeak to detect a persistent flow difference so that a possible incident is handled before more water is lost.

**Acceptance Criteria:**

- **Scenario: Difference remains above the rule**
  - **Given** the percentage difference is above the configured threshold,
  - **When** it remains above the threshold for the persistence duration,
  - **Then** the platform records a `FlowAnomalyConfirmed` event with the supporting readings.

- **Scenario: Difference is temporary**
  - **Given** the percentage briefly exceeds the threshold,
  - **When** it returns to range before the persistence duration,
  - **Then** the platform does not confirm an anomaly.

#### US09 - Close the Shutoff Valve Safely

**As an Agricultural Producer**, I want the shutoff valve to close after a confirmed anomaly so that the segment enters a safer state until it is inspected.

**Acceptance Criteria:**

- **Scenario: Close an enabled valve**
  - **Given** a flow anomaly is confirmed and automatic closure is enabled,
  - **When** the Edge controller receives the closure request,
  - **Then** it closes the valve, verifies feedback, records the action, and raises an alert.

- **Scenario: Valve feedback does not confirm closure**
  - **Given** a closure command was issued,
  - **When** feedback is not received within the timeout,
  - **Then** the system marks the action as failed, activates the local warning, and raises a critical alert.

#### US10 - Reopen a Valve after Inspection

**As an Agricultural Producer**, I want to reopen a closed valve only after recording an inspection so that irrigation does not resume without accountability.

**Acceptance Criteria:**

- **Scenario: Reopen after a valid inspection**
  - **Given** the anomaly is no longer active and an inspection result was recorded,
  - **When** an authorized producer confirms reopening,
  - **Then** the system opens the valve and stores the user, timestamp, and reason.

- **Scenario: Attempt reopening while the anomaly persists**
  - **Given** the anomaly condition is still active,
  - **When** the producer requests reopening,
  - **Then** the platform blocks the command and explains the unresolved condition.

#### US11 - Configure a Pest Observation Point

**As an Agricultural Producer**, I want to assign a camera, target pest, and confirmation rule to an observation point so that visual monitoring has an explicit scope.

**Acceptance Criteria:**

- **Scenario: Save a valid observation point**
  - **Given** a camera, plot, supported target pest, and valid rule are available,
  - **When** the producer confirms the setup,
  - **Then** the point is saved with its capture schedule and model version.

- **Scenario: Select an unsupported target pest**
  - **Given** the selected pest is not supported by the active model,
  - **When** the configuration is submitted,
  - **Then** the platform rejects it and lists the supported class.

#### US12 - Review an AI Pest Detection

**As an Agricultural Producer**, I want to review the annotated image, predicted class, confidence, and count so that I can evaluate the detection evidence.

**Acceptance Criteria:**

- **Scenario: Display a completed inference**
  - **Given** the Edge gateway completed an inference,
  - **When** the producer opens the observation,
  - **Then** the platform displays the original or annotated image, class, confidence, count, timestamp, and model version.

- **Scenario: Display an uncertain observation**
  - **Given** confidence is below the configured threshold,
  - **When** the producer opens the observation,
  - **Then** the platform labels it as uncertain and does not present it as a confirmed pest.

#### US13 - Confirm a Target Pest

**As an Agricultural Producer**, I want AgroLeak to confirm the target pest only when the complete rule is met so that isolated or uncertain images do not trigger an action.

**Acceptance Criteria:**

- **Scenario: Meet class, confidence, and repetition conditions**
  - **Given** target-pest detections exceed the confidence threshold,
  - **When** the required number occurs within the configured window,
  - **Then** the platform records a `TargetPestConfirmed` event and creates an alert.

- **Scenario: Detect a non-target insect**
  - **Given** the model classifies an observation as `NON_TARGET_INSECT`,
  - **When** the inference is processed,
  - **Then** the evidence is stored but no pest confirmation or control request is created.

#### US14 - Authorize a Localized Control Action

**As an Agricultural Producer**, I want to approve or reject a localized control request so that I remain responsible for the intervention.

**Acceptance Criteria:**

- **Scenario: Approve a valid request**
  - **Given** a target pest is confirmed and all safety checks pass,
  - **When** an authorized producer approves the request before it expires,
  - **Then** the platform sends a signed, time-limited actuation command to the Edge controller.

- **Scenario: Reject or ignore a request**
  - **Given** a control request is pending,
  - **When** the producer rejects it or its approval window expires,
  - **Then** no actuator command is sent and the decision is recorded.

#### US15 - Execute a Localized Control Action

**As an Agricultural Producer**, I want AgroLeak to execute a bounded localized action so that the prototype responds physically without exceeding safety limits.

**Acceptance Criteria:**

- **Scenario: Execute within limits**
  - **Given** a valid command reaches an enabled actuator with no lockout,
  - **When** the Edge controller validates duration and daily count,
  - **Then** it activates the mechanism for the authorized duration and records start, stop, and result.

- **Scenario: A safety condition fails**
  - **Given** the actuator is disabled, locked out, or at its daily limit,
  - **When** an actuation command arrives,
  - **Then** the controller rejects it, keeps the actuator off, and raises a safety alert.

#### US16 - Validate or Correct a Pest Detection

**As an Agricultural Producer**, I want to mark an observation as correct, incorrect, or uncertain so that the team can analyze model errors without silently changing historical evidence.

**Acceptance Criteria:**

- **Scenario: Submit a validation label**
  - **Given** the producer can view an observation,
  - **When** the producer selects a validation label and optional comment,
  - **Then** the platform stores the annotation separately from the original inference.

- **Scenario: Edit a previous validation**
  - **Given** a validation already exists,
  - **When** an authorized user changes it,
  - **Then** the platform versions the change and preserves the audit trail.

#### US17 - Manage Alerts and Resolution

**As an Agricultural Producer**, I want to acknowledge and resolve irrigation and pest alerts so that every incident has a traceable outcome.

**Acceptance Criteria:**

- **Scenario: Acknowledge an open alert**
  - **Given** an alert is open,
  - **When** the producer acknowledges it,
  - **Then** the platform records the user and acknowledgment time.

- **Scenario: Resolve an alert**
  - **Given** the producer completed the required action,
  - **When** the producer records the result and closes the alert,
  - **Then** the platform stores the resolution, user, and closing time.

#### US18 - Browse Monitoring and Actuation History

**As an Agricultural Producer**, I want to filter readings, detections, alerts, and actions so that I can reconstruct what happened in a selected period.

**Acceptance Criteria:**

- **Scenario: Apply valid filters**
  - **Given** historical records exist,
  - **When** the producer selects a date range, plot, and event type,
  - **Then** the platform returns matching records in chronological order.

- **Scenario: No records match**
  - **Given** no records match the selected criteria,
  - **When** the filters are applied,
  - **Then** the platform displays an empty result without clearing the filters.

#### US19 - View Quantitative Summaries

**As an Agricultural Producer**, I want to view hydraulic and pest-monitoring summaries so that I can understand the selected period.

**Acceptance Criteria:**

- **Scenario: Generate a summary**
  - **Given** valid synchronized data exists,
  - **When** the producer opens analytics for a period,
  - **Then** the platform displays flow statistics, anomaly count, target-pest detections, false-positive labels, and actions.

- **Scenario: Exclude invalid data**
  - **Given** some readings or inferences are invalid,
  - **When** the summary is calculated,
  - **Then** the platform excludes them and identifies the excluded record count.

#### US20 - View Weather Context

**As an Agricultural Producer**, I want to view basic weather information so that I can use it as complementary context when reviewing the plot.

**Acceptance Criteria:**

- **Scenario: Weather service is available**
  - **Given** the plot has valid coordinates and the provider is available,
  - **When** the producer opens the plot overview,
  - **Then** the platform displays the selected weather variables and provider timestamp.

- **Scenario: Weather service is unavailable**
  - **Given** the provider cannot be reached,
  - **When** the overview loads,
  - **Then** the platform labels the weather data as unavailable without blocking AgroLeak monitoring.

### Developer Technical Stories

#### TS01 - Receive Device Telemetry through the Edge API

**As a Developer**, I want the Edge API to receive authenticated telemetry so that each record has a trusted device, timestamp, and source.

**Acceptance Criteria:**

- **Scenario: Receive a valid payload**
  - **Given** a registered device sends a supported payload with valid credentials,
  - **When** the Edge API validates it,
  - **Then** the record is stored in SQLite and acknowledged with its local identifier.

- **Scenario: Reject an invalid payload**
  - **Given** required fields or credentials are invalid,
  - **When** the payload reaches the Edge API,
  - **Then** the API rejects it and records a security or validation event without storing it as valid telemetry.

#### TS02 - Run Pest Inference at the Edge

**As a Developer**, I want the gateway to run the versioned pest model locally so that detections can continue without Internet connectivity.

**Acceptance Criteria:**

- **Scenario: Process a supported image**
  - **Given** an authorized camera provides a valid image,
  - **When** the inference worker processes it,
  - **Then** it stores class, confidence, count, regions, model version, and processing time.

- **Scenario: Fail to process an image**
  - **Given** the image is corrupt or the model cannot run,
  - **When** processing fails,
  - **Then** the worker records the failure, creates no pest confirmation, and preserves diagnostic metadata.

#### TS03 - Enforce Actuator Safety Interlocks

**As a Developer**, I want all actuator commands to pass local safety checks so that cloud errors or duplicated messages cannot cause unsafe repetition.

**Acceptance Criteria:**

- **Scenario: Accept a valid idempotent command**
  - **Given** the command is signed, current, unique, and within limits,
  - **When** the Edge controller validates it,
  - **Then** it executes the action once and stores the command identifier.

- **Scenario: Receive a duplicated or expired command**
  - **Given** the command identifier was processed or its expiry time passed,
  - **When** the controller receives it,
  - **Then** it rejects the command and keeps the actuator state unchanged.

#### TS04 - Synchronize Pending Edge Records

**As a Developer**, I want the Edge API to synchronize pending records with the Cloud REST API so that temporary Internet interruptions do not erase monitoring history.

**Acceptance Criteria:**

- **Scenario: Synchronize after connectivity returns**
  - **Given** pending records exist and Internet connectivity returns,
  - **When** synchronization runs,
  - **Then** records are sent in order and marked as synchronized after confirmation.

- **Scenario: Retry without duplicates**
  - **Given** a previous request timed out after reaching the Cloud API,
  - **When** the Edge retries the same batch,
  - **Then** the Cloud API uses idempotency keys and creates no duplicates.

#### TS05 - Upload Evidence Images Securely

**As a Developer**, I want to upload evidence images with integrity metadata so that every inference remains traceable to its source.

**Acceptance Criteria:**

- **Scenario: Upload a valid image**
  - **Given** a supported image and metadata are available,
  - **When** the Edge API synchronizes them,
  - **Then** the Cloud stores the object reference, checksum, observation point, capture time, and model result.

- **Scenario: Reject an unsupported image**
  - **Given** the format or size is unsupported,
  - **When** upload is attempted,
  - **Then** the API rejects it and preserves the local record for diagnosis.

#### TS06 - Preserve an Auditable Action Log

**As a Developer**, I want commands, approvals, device feedback, and failures to be immutable audit records so that every physical action can be reconstructed.

**Acceptance Criteria:**

- **Scenario: Record a completed action**
  - **Given** an actuator action starts and stops,
  - **When** Edge feedback is synchronized,
  - **Then** the Cloud stores command, authorizer, timestamps, device, requested duration, actual duration, and result.

- **Scenario: Prevent direct history replacement**
  - **Given** an authenticated user edits a current configuration,
  - **When** the change is saved,
  - **Then** historical action records remain unchanged and a new configuration version is created.

## 3.2 Impact Mapping

### Business Goal BG01

**Lograr que al menos 3 productores completen una prueba guiada de los dos circuitos y que 2 manifiesten intención de participar en un piloto durante el ciclo 2026-2.**

| Actor | Impacto esperado | Deliverable | User Stories |
|---|---|---|---|
| Productor | Comprende y atiende una anomalía hidráulica | Dashboard, alerta y válvula | US07-US10, US17 |
| Productor | Evalúa evidencia de una plaga objetivo | Observación anotada y regla | US11-US13, US16 |
| Productor | Conserva control sobre la intervención | Aprobación y acción localizada | US14-US15 |
| Productor | Reconstruye incidentes | Historial y analítica | US18-US20 |
| Equipo | Demuestra operación distribuida segura | Edge, IA, sync y auditoría | TS01-TS06 |

### Business Goal BG02

**Conseguir al menos 5 solicitudes calificadas de demostración mediante el Landing Page antes de finalizar TB2.**

| Actor | Impacto esperado | Deliverable | User Stories |
|---|---|---|---|
| Visitante | Comprende producto y límites | Landing Page responsive | US01 |
| Visitante | Solicita una prueba | Formulario y confirmación | US02 |

Elaborar el artefacto final en UXPressia, insertar captura y agregar URL pública.

## 3.3 Product Backlog

La priorización favorece primero los dos circuitos IoT de punta a punta, sus salvaguardas y la evidencia necesaria para demostrarlos.

| Orden | ID | Título | Descripción resumida | Story Points |
|---:|---|---|---|---:|
| 1 | TS01 | Receive device telemetry | Persistencia Edge autenticada. | 5 |
| 2 | US07 | View irrigation status | Lecturas y estado de válvula. | 5 |
| 3 | US08 | Detect flow anomaly | Umbral y persistencia. | 8 |
| 4 | US09 | Close shutoff valve | Cierre y feedback seguro. | 8 |
| 5 | TS02 | Run pest inference | Inferencia Edge versionada. | 8 |
| 6 | US12 | Review AI detection | Imagen, clase y confianza. | 5 |
| 7 | US13 | Confirm target pest | Regla por confianza y repetición. | 8 |
| 8 | TS03 | Enforce safety interlocks | Validación local de comandos. | 8 |
| 9 | US15 | Execute localized control | Actuación limitada y trazable. | 8 |
| 10 | US14 | Authorize control | Aprobación o rechazo. | 5 |
| 11 | US17 | Manage alerts | Ciclo de atención. | 5 |
| 12 | TS04 | Synchronize Edge records | Sync idempotente. | 8 |
| 13 | TS05 | Upload evidence images | Integridad y almacenamiento. | 5 |
| 14 | TS06 | Preserve audit log | Historial de actuaciones. | 5 |
| 15 | US01 | Browse public website | Propuesta y CTA. | 5 |
| 16 | US02 | Request demonstration | Captación de prospectos. | 3 |
| 17 | US03 | Sign in | Acceso seguro. | 5 |
| 18 | US04 | Register farm and plot | Organización de ubicaciones. | 5 |
| 19 | US05 | Configure segment | Sensores y válvula. | 5 |
| 20 | US06 | Configure flow rule | Parámetros calibrados. | 3 |
| 21 | US11 | Configure observation point | Cámara, plaga y modelo. | 5 |
| 22 | US10 | Reopen after inspection | Reapertura autorizada. | 5 |
| 23 | US16 | Validate detection | Etiqueta de usuario. | 3 |
| 24 | US18 | Browse history | Filtros y línea de tiempo. | 5 |
| 25 | US19 | View summaries | Métricas hidráulicas y visuales. | 5 |
| 26 | US20 | View weather context | Adaptador externo. | 3 |
