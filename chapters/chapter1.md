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

|**Integrante**|**Perfil**|**Imagen**|
|:-------------|----------|:--------:|
| **Juan David Ayllon Pauccar**|"Estudiante de 5to ciclo de Ingeniería de Software en la UPC. Cuento con conocimientos técnicos avanzados en desarrollo con C++, SQL, Python Intermedio, HTML, CSS. Me distingo por ser un integrante responsable y con gran capacidad de comunicación asertiva, facilitando la coordinación y el flujo de trabajo dentro del equipo. Mi compromiso con el proyecto SmartLock se refleja en mi disposición para aprender, resolver desafíos complejos y asegurar que cada entrega cumpla con los estándares esperados."|<img src="../Resources/Chapter1/Students profiles/Juan David-Ayllon.jpg" width="2000"/>
| **Imanol Fabrizio Limache Coronel**|Soy un estudiante al que le gusta aprender cosas nuevas, sobre todo si se relacionan a la programación, además de la resolución de problemas.|<img src="../Resources/Chapter1/Students profiles/Imanol-Limache.jpeg" width="2000"/>|
|**Huaman Oscco Aldo Jesus - u20231h067**|Estudiante de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas (UPC). Actualmente cursando el 5to ciclo de la carrera, asumo la responsabilidad de investigar y aplicar conocimientos y habilidades de desarrollo en **SmarLock** de manera eficiente para culminarlo con exito.|<img src="/Resources/Chapter1/Students profiles/Aldo-Jesus.png" alt="Foto de Aldo Jesus Huaman Oscco" width="2000"/> |
|**Peñaranda Caldas Gabriel Augusto - u202210836**|Estudiante de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas (UPC). Me encuentro llevando cursos de 5to y 6to ciclo de la carrera. Cuento con habilidades sobresalientes en cloud, python, typescript y UX/UI. Además se ser alguien muy preocupado por mis compañeros de equipo y amigable que las demás personas. Me comprometo a que el proyecto **SmartLock** se lleve a cabo con éxito brindando responsabilidad y puntualidad en las entregas y avances del proyecto.|<img src="/Resources/Chapter1/Students profiles/Gabriel-Peniaranda.jpg" alt="Foto de Gabriel Peñaranda Caldas" width="2000"/> |
|**Palacios Tinoco Adrian Fernando - u202410817** | Estudiante de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas (UPC). Me encuentro cursando el 5to ciclo de la carrera. Cuento con habilidades tanto blandas como tecnicas. Por un lado, entre mis habilidades blandas destaco el trabajo en equipo, comunicacion efectiva y escucha activa. Por otro lado, mis habilidades entre mis habilidades tecnicas es el diseño de base de datos, analisis de requisitos, diseño de software y como lenguajes destaco mi conocimiento en C++, JavaScript, Python, Java y SQL. Me comprometo a que el proyecto **SmartLock** se lleve a cabo con éxito brindando responsabilidad y puntualidad en las entregas y avances del proyecto. | <img src="/Resources/Chapter1/Students profiles/Adrian-Palacios.jpg" alt="Foto de Adrian Fernando Palacios Tinoco" width="2000"/> |

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
| :------------------ | :------------------- |
| Las empresas pierden tiempo y vulneran su seguridad gestionando accesos con métodos inflexibles o sin monitoreo en tiempo real. | - Conseguir suscripciones al Plan Básico/Pro.<br>- Alta retención mensual.<br>- Reducción de incidentes de seguridad de los clientes. |
| **3. Users / Customers** | **4. User Benefits** |
| - Administradores de instalaciones / RRHH.<br>- Personal de monitoreo / Prevención.<br>- Empleados (usuarios finales). | - Tranquilidad al tener control total de quién entra y cuándo.<br>- Ahorro de tiempo en auditorías.<br>- Alertas automáticas sin esfuerzo manual. |
| **5. Solutions / Ideas** | **6. Hypotheses** |
| - Panel en tiempo real.<br>- Sistema de reglas por horario y roles.<br>- Motor de alertas de anomalías.<br>- Log de auditoría inmutable. | - Creemos que reduciremos el tiempo de respuesta ante incidentes en un 50% si el personal logra identificar anomalías usando las alertas automáticas.<br>- Creemos que aumentaremos la adopción del Plan Pro si RRHH logra automatizar la entrada usando el control por franjas horarias. |
| **7. What's the most important thing to learn first?** | **8. What's the least amount of work we need to do to learn this? (MVP)** |
| ¿Los administradores confiarán en la gestión de permisos a través de una interfaz web antes de conectar hardware real? | Construir la plataforma web funcional con la función de **Simulación de acceso a puertas** para demostrar el flujo lógico a clientes potenciales. |
### 1.3. Segmentos objetivo
---

Para el desarrollo de **Smart Lock**, se han definido los siguientes segmentos objetivo, integrando sus perfiles, necesidades y comportamientos en la gestión de accesos:

| **Segmento** | **Descripción del Perfil** | **Necesidades Principales** | **Características Psicográficas y Comportamentales** |
| :--- | :--- | :--- | :--- |
| **Gerentes de Operaciones, TI y Seguridad Corporativa** | Líderes responsables de una empresa preocupada por la infraestructura y seguridad de sus espacios de trabajo, desde startups en crecimiento hasta corporativos con múltiples oficinas y alto flujo de personal. | - Centralizar el control de accesos de múltiples sedes en una sola plataforma.<br>- Eliminar la vulnerabilidad de las llaves físicas y tarjetas clonables.<br>- Automatizar el registro de asistencia y la revocación inmediata de permisos a gran escala. | - Priorizan la escalabilidad y la integración con herramientas SaaS existentes.<br>- Toman decisiones basadas en datos y registros de auditoría inmutables.<br>- Buscan máxima eficiencia operativa reduciendo el error humano en porterías. |
| **Administradores de Eventos y Espacios de Alto Tráfico** | Profesionales encargados de la logística en centros de convenciones, ferias o complejos de oficinas que requieren gestionar entradas masivas por periodos específicos. | - Creación rápida de credenciales digitales temporales para invitados o contratistas.<br>- Monitoreo en tiempo real de la ocupación por zonas para evitar aglomeraciones.<br>- Despliegue del sistema sin depender de instalaciones de hardware pesadas o fijas. | - Valoran la agilidad y la capacidad de respuesta inmediata ante incidentes.<br>- Están familiarizados con protocolos de seguridad dinámica (2FA y alertas móviles).<br>- Prefieren interfaces intuitivas que permitan delegar tareas de control de forma sencilla. |
