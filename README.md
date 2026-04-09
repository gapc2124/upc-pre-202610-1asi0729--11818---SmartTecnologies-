<div align="center">
  <img src="Resources/UPC/UPC-Logo.png" alt="Logo-UPC" width="150">

## Universidad Peruana de Ciencias Aplicadas

**Ingeniería de Software**

**Ciclo:** 2026-10

**Curso:** Desarrollo de Aplicaciones Open Source

**Sección:** 11881

**Profesor:** Efraín Ricardo Bautista Ubillús


----
## Informe de Trabajo Final
### SmartTecnologies

### SmartLock
#### Relación de integrantes
<br>

| Integrante                      | Código     |
|---------------------------------|------------|
| Palacios Tinoco Adrian Fernando | u202410817 |
|                                 |            |
|                                 |            |
|                                 |            |
|                                 |            |

</div>

<br><div align="center"><h3>Abril 2026</h3></div><br>
<div style="text-align: justify;"></div>

<br>

---
### Registro de Versiones

<div align="justify">

|**Versión**| **Fecha**  | **Autor**                                          | **Descripción de modificación**                                                                                                                 |
| - |------------|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
|1\.0| 07/04/2026 | Adrian Fernando Palacios Tinoco                    | Se agrego parte de la estructura del capitulo I del informe, asimismo se agrego la carátula, el startup profile; y antecedentes y problemáticas |

</div><br><br>

---

# Capítulo I: Introducción

## 1.1. Startup Profile
### 1.1.1. Descripción de la Startup
**Área:** Seguridad Digital y Control de Accesos

**SmartTecnologies** es una startup formada por un equipo de estudiantes de ingeniería de software de la Universidad Peruana de Ciencias Aplicadas (UPC) que nace con la meta de proponer una alternativa moderna a los sistemas de seguridad tradicionales, que muchas veces se quedan cortos en control y trazabilidad. Identificamos que la gestión de llaves físicas y el registro manual de entradas son procesos lentos y poco fiables, por lo que desarrollamos Smart Lock. Nuestra solución es una plataforma web integral que permite administrar y monitorear el ingreso a cualquier espacio físico desde un solo lugar, transformando la seguridad convencional en un sistema inteligente basado en datos y control en tiempo real.

* **Misión:** Nuestra misión en SmartTecnologies es darle a los administradores y dueños de espacios una herramienta tecnológica avanzada que simplifique cómo controlan sus accesos. Con Smart Lock, buscamos que el proceso de decidir quién entra y quién no deje de ser una preocupación, ofreciendo un sistema basado en reglas claras y alertas automáticas que garantice que cada movimiento quede registrado de forma transparente y segura.
<br></br>
* **Visión:** Nos proyectamos como la startup líder en digitalización de accesos dentro de la región, logrando que nuestra tecnología sea el estándar en edificios, oficinas y centros de estudio. Queremos que SmartTecnologies sea sinónimo de modernidad y eficiencia, impulsando una cultura donde la seguridad no sea una barrera, sino un proceso fluido y totalmente automatizado.
<br></br>
* **Valores:**

    * **Seguridad y Confidencialidad:** Como estudiantes de Ingeniería de Software, sabemos que los datos de acceso son críticos. Por eso, nos tomamos muy en serio la protección de la información, usando protocolos de autenticación y cifrado para que solo las personas autorizadas tengan el control.

    * **Precisión en los datos:** Nos comprometemos con la exactitud en la gestión de presupuestos y tareas, asegurando que la información reflejada en la plataforma sea un espejo fiel de la realidad del proyecto.

    * **Innovación aplicada:** No nos conformamos con lo que ya existe. Buscamos aplicar lo aprendido en nuestra formación para integrar funciones como la simulación de flujo sin hardware y reglas de acceso dinámicas que mantengan a Smart Lock a la vanguardia.

    * **Gestión Colaborativa y Simple:** Creemos que la tecnología debe ser fácil de usar. Centralizamos todo en un panel intuitivo para que la comunicación entre administradores y usuarios sea rápida, eliminando complicaciones innecesarias.

    * **Compromiso con la Excelencia:** Trabajamos para que nuestra plataforma soporte las exigencias de un entorno real, ofreciendo una herramienta robusta que aguante el flujo constante de usuarios sin perder fiabilidad.
### 1.1.2. Perfiles de integrantes del equipo

| **Integrante**                                   | **Perfil**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |                                                       **Imagen**                                                       |
|:-------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------:|
| **Nombre y apellido**                            |
| **Nombre y apellido**                            |
| **Nombre y apellido**                            |
| **Nombre y apellido**                            |
| **Palacios Tinoco Adrian Fernando - u202410817** | Estudiante de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas (UPC). Me encuentro cursando el 5to ciclo de la carrera. Cuento con habilidades tanto blandas como tecnicas. Por un lado, entre mis habilidades blandas destaco el trabajo en equipo, comunicacion efectiva y escucha activa. Por otro lado, mis habilidades entre mis habilidades tecnicas es el diseño de base de datos, analisis de requisitos, diseño de software y como lenguajes destaco mi conocimiento en C++, JavaScript, Python, Java y SQL. Me comprometo a que el proyecto **SmartLock** se lleve a cabo con éxito brindando responsabilidad y puntualidad en las entregas y avances del proyecto. | <img src="Resources/Students profiles/Adrian-Palacios.jpg" alt="Foto de Adrian Fernando Palacios Tinoco" width="150"/> |

## 1.2. Solution Profile
### 1.2.1. Antecedentes y problemática

**5W's y 2H's**

Para definir el problema central de Smart Lock, hemos aplicado la técnica de análisis detallado:
<br>

* **What?**
  <br>
  La falta de un sistema centralizado, auditable y seguro para gestionar el ingreso de personal, lo que genera vulnerabilidades en la seguridad física y administrativa.<br><br>


* **Why?**
  <br>
  Porque los sistemas convencionales no ofrecen trazabilidad. No se puede saber con certeza quién entró a una hora específica si no existe un registro digital automático y protegido contra alteraciones. <br><br>

* **Who?**
  <br>
  Administradores de oficinas, gestores de espacios de coworking y dueños de propiedades residenciales o comerciales que carecen de un control estricto sobre sus accesos.<br><br>

* **When?**
  <br>
  El problema se manifiesta diariamente, especialmente en horarios fuera de oficina o durante cambios de turno, donde el control se vuelve crítico y propenso a errores humanos.<br><br>

* **Where?**
  <br>
  En entornos urbanos con alta densidad de oficinas y espacios compartidos donde el flujo de personas es constante y difícil de registrar manualmente.<br><br>

* **How?**
  <br>
  La problemática se agrava mediante el uso de llaves duplicadas sin permiso, el olvido de registros en cuadernos físicos y la incapacidad de revocar accesos de manera inmediata ante una baja de personal.<br><br>

* **How much?**
  <br>
  El costo de una brecha de seguridad o la pérdida de activos por un acceso no autorizado puede ascender a miles de soles, sumado al gasto constante en cerrajería tradicional que representa un flujo de caja ineficiente para las startups y PYMES.

### 1.2.2. Lean UX Process
#### 1.2.2.1. Lean UX Problem Statements
El dominio de nuestro producto es la gestión de seguridad y control de acceso a espacios físicos (Domain). Actualmente, nuestros administradores de edificios, dueños de negocios y personal de seguridad (Customer Segments) sufren por la falta de visibilidad en tiempo real, la dificultad para gestionar permisos temporales o por horarios, y la tediosa tarea de auditar accesos manualmente (Pain Points). Esto genera una brecha significativa de seguridad y eficiencia operativa frente a sistemas tradicionales que son inflexibles o ciegos ante anomalías (Gap).

Nuestra visión es proporcionar a las empresas una plataforma web inteligente y escalable que no solo permita o deniegue el acceso, sino que automatice el monitoreo mediante reglas, alertas y un historial detallado en tiempo real (Vision/Strategy). Para comenzar a validar nuestra solución, nos enfocaremos en un segmento inicial de pequeñas y medianas empresas (pymes) o espacios de coworking que requieran un control estricto de horarios para sus empleados sin invertir inicialmente en hardware complejo (Initial Segment).
#### 1.2.2.2. Lean UX Assumptions
**Business Assumptions (Suposiciones del Negocio):**

- Creemos que las empresas están dispuestas a pagar una suscripción mensual recurrente (modelo SaaS) en lugar de un pago único por un software de escritorio tradicional.

- Creemos que la simulación de acceso a puertas será suficiente para convencer a los primeros clientes (early adopters) del valor del software antes de integrarlo con hardware físico.

- Creemos que el límite de usuarios y de historial en el "Plan Básico" será el principal motivador para que los clientes escalen al "Plan Profesional".

**User Assumptions (Suposiciones del Usuario):**

- Creemos que el personal de monitoreo adoptará la verificación de dos pasos (2FA) sin considerarlo un bloqueo para su productividad.

- Creemos que los administradores valoran más recibir alertas automáticas (ej. intentos fallidos o fuera de horario) que revisar un historial de registros de forma manual.
#### 1.2.2.3. Lean UX Hypothesis Statements
- Hipótesis 1 (Alertas): Creemos que reduciremos el tiempo de respuesta ante incidentes de seguridad en un 50% si el personal de monitoreo logra identificar anomalías instantáneamente usando el sistema de alertas por intentos fallidos repetidos o accesos fuera de horario.

- Hipótesis 2 (Gestión de roles): Creemos que aumentaremos la adopción del Plan Profesional si los administradores de recursos humanos logran automatizar la entrada de su personal usando el control de acceso segmentado por franjas horarias y días laborales.

- Hipótesis 3 (Seguridad): Creemos que las empresas confiarán la auditoría de sus instalaciones a nuestra plataforma si los auditores internos logran rastrear exactamente quién autorizó un ingreso usando el historial detallado de eventos y la autenticación segura (2FA).

#### 1.2.2.4. Lean UX Canvas

| 1. Business Problem | 2. Business Outcomes |
| :--- | :--- |
| Las empresas pierden tiempo y vulneran su seguridad gestionando accesos con métodos inflexibles o sin monitoreo en tiempo real. | - Conseguir suscripciones al Plan Básico/Pro.<br>- Alta retención mensual.<br>- Reducción de incidentes de seguridad de los clientes. |
| **3. Users / Customers** | **4. User Benefits** |
| - Administradores de instalaciones / RRHH.<br>- Personal de monitoreo / Prevención.<br>- Empleados (usuarios finales). | - Tranquilidad al tener control total de quién entra y cuándo.<br>- Ahorro de tiempo en auditorías.<br>- Alertas automáticas sin esfuerzo manual. |
| **5. Solutions / Ideas** | **6. Hypotheses** |
| - Panel en tiempo real.<br>- Sistema de reglas por horario y roles.<br>- Motor de alertas de anomalías.<br>- Log de auditoría inmutable. | - Creemos que reduciremos el tiempo de respuesta ante incidentes en un 50% si el personal logra identificar anomalías usando las alertas automáticas.<br>- Creemos que aumentaremos la adopción del Plan Pro si RRHH logra automatizar la entrada usando el control por franjas horarias. |
| **7. What's the most important thing to learn first?** | **8. What's the least amount of work we need to do to learn this? (MVP)** |
| ¿Los administradores confiarán en la gestión de permisos a través de una interfaz web antes de conectar hardware real? | Construir la plataforma web funcional con la función de **Simulación de acceso a puertas** para demostrar el flujo lógico a clientes potenciales. |
### 1.3. Segmentos objetivo

---

# Capítulo II: Requirements Elicitation & Analysis


## 2.1 Competidores

### 2.1.1 Análisis Competitivo

### 2.1.2. Estrategias y tácticas frente a competidores.

## 2.2 Entrevistas

### 2.2.1 Diseño de entrevistas

### 2.2.2 Registro de entrevistas

### 2.2.3 Análisis de entrevistas

## 2.3 Needfinding

### 2.3.1. User Personas.
### 2.3.2. User Task Matrix.
### 2.3.3. User Journey Mapping.
### 2.3.4. Empathy Mapping.
### 2.3.5. As-is Scenario Mapping.

## 2.4. Big Picture Event Storming.
## 2.5. Ubiquitous Language

---
# Capítulo III: Requirements Specification

## 3.1. User Stories.

| Epic / Story ID | Título | Descripción | Criterios de Aceptación | Relacionado con (Epic ID) |
| :--- | :--- | :--- | :--- | :--- |
| **US-XX** | | | **Escenario 1:** <br>Dado que <br>Cuando <br>Entonces | **EP-XX** |
| | | | | |

## 3.2. Impact Mapping

## 3.3. Product Backlog

---
# Capítulo IV: Product Design

## 4.1. Style Guidelines.
### 4.1.1. General Style Guidelines.
### 4.1.2. Web Style Guidelines.
## 4.2. Information Architecture.
### 4.2.1. Organization Systems.
### 4.2.2. Labeling Systems.
### 4.2.3. SEO Tags and Meta Tags
### 4.2.4. Searching Systems.
### 4.2.5. Navigation Systems.
## 4.3. Landing Page UI Design.
### 4.3.1. Landing Page Wireframe.
### 4.3.2. Landing Page Mock-up.
## 4.4. Web Applications UX/UI Design.
### 4.4.1. Web Applications Wireframes.
### 4.4.2. Web Applications Wireflow Diagrams.
### 4.4.3. Web Applications Mock-ups.
### 4.4.4. Web Applications User Flow Diagrams.
## 4.5. Web Applications Prototyping.
## 4.6. Domain-Driven Software Architecture.
### 4.6.1. Design-Level Event Storming.
### 4.6.2. Software Architecture Context Diagram.
### 4.6.3. Software Architecture Container Diagrams.
### 4.6.4. Software Architecture Components Diagrams.
## 4.7. Software Object-Oriented Design.
### 4.7.1. Class Diagrams.
## 4.8. Database Design.
### 4.8.1. Database Diagrams.

---
# Capítulo V: Product Implementation, Validation & Deployment.
## 5.1. Software Configuration Management.
### 5.1.1. Software Development Environment Configuration.
### 5.1.2. Source Code Management.
### 5.1.3. Source Code Style Guide & Conventions.
### 5.1.4. Software Deployment Configuration.
## 5.2. Landing Page, Services & Applications Implementation.
### 5.2.1. Sprint 1
#### 5.2.1.1. Sprint Planning 1.
#### 5.2.1.2. Aspect Leaders and Collaborators.
#### 5.2.1.3. Sprint Backlog 1.
#### 5.2.1.4. Development Evidence for Sprint Review.
#### 5.2.1.5. Execution Evidence for Sprint Review.
#### 5.2.1.6. Services Documentation Evidence for Sprint Review.
#### 5.2.1.7. Software Deployment Evidence for Sprint Review.
#### 5.2.1.8. Team Collaboration Insights during Sprint.
## 5.3. Validation Interviews.
### 5.3.1. Diseño de Entrevistas.
### 5.3.2. Registro de Entrevistas.
### 5.3.3. Evaluaciones según heurísticas.
## 5.4. Video About-the-Product.
---
# Conclusiones
# Bibliografía

# Anexos