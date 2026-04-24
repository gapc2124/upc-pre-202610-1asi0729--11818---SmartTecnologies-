# Capítulo IV: Product Design

## 4.1. Style Guidelines.
Se describen las directrices que aseguran la uniformidad
estética del proyecto.<br>

### 4.1.1. General Style Guidelines.
**Colors:**
<br>
Elegimos una paleta que grite **seguridad y tecnología**, pero sin cansar la vista (pensando en administradores que estarán pegados al dashboard monitoreando accesos).
<br>
* **Azul Oscuro (#1B263B):** Es nuestro color estrella. Da esa seriedad y confianza que necesitas cuando hablas de controlar quién entra a tu edificio u oficina.
* **Casi Negro (#0D1B2A):** Lo usamos para los textos importantes. No es negro puro porque eso agota la vista en sesiones largas, pero tiene el peso suficiente para que se lea claro.
* **Gris Neutro (#E0E1DD):** Este va de fondo en las secciones. Es limpio y hace que los demás elementos resalten sin esfuerzo.
* **Azul Eléctrico (#3E92CC):** Este es nuestro "call to action". Si hay algo que el usuario tiene que clickear sí o sí (como el botón de "Abrir Puerta" o "Guardar Configuración"), va en este color.

<img src="/Resources/Style%20Guidelines/Paleta-de-colores/Paleta-de-colores.PNG">


**Branding**<br>
El logo de **SmartLock** es directo al grano: un **candado**. Elegimos este isotipo porque es el símbolo universal de la seguridad física; no necesitamos complicarlo con más adornos para que el usuario entienda qué hacemos. Lo que lo hace moderno es su diseño minimalista y limpio. Acompañando al candado, la tipografía del nombre es sólida y de cortes precisos. Queríamos que la identidad visual transmitiera esa firmeza y robustez que se espera de un sistema de seguridad confiable, alejándonos de cualquier estética que pudiera parecer "frágil" o improvisada.

<img src="/Resources/Logo/SmartLock-Logo.png">

**Typography** <br>
Nos fuimos por **Inter**. ¿Por qué? Porque cuando tienes una lista gigante de registros de entrada y salida, necesitas una letra que se lea perfecto en pantallas de cualquier tamaño. Es una fuente *sans-serif* optimizada para entornos digitales.
* **Bold:** Para los títulos de sección y alertas que no puedes ignorar.
* **Semi-Bold:** Para encabezados de tablas o nombres de usuarios.
* **Regular:** Para el cuerpo de texto y los logs de acceso.
* *Referencia:* [Inter - Google Fonts](https://fonts.google.com/specimen/Inter)

**Spacing**<br>
Para que no todo esté tirado al azar, usamos la regla de los **8px**. Si vas a separar algo, que sea múltiplo de 8. En el código, **solo usamos `rem`** para que la interfaz sea escalable y se adapte bien si el usuario cambia el tamaño de fuente de su navegador.

| Categoría | Medida (rem / px) | Aplicación en el Diseño |
| :--- | :--- | :--- |
| **X-Small** | 0.25 rem / 4 px | Alineación de iconos y micro-ajustes de posición. |
| **Small** | 0.5 rem / 8 px | Espacio entre un texto y su campo de entrada (input). |
| **Medium** | 1.0 rem / 16 px | Relleno interno (padding) de botones y tarjetas. |
| **Large** | 1.5 rem / 24 px | Margen entre componentes de un mismo bloque funcional. |
| **X-Large** | 2.0 rem / 32 px | Distancia entre contenedores de información independientes. |
| **Section** | 4.0 rem / 64 px | El espacio grande entre bloques estructurales de la página. |

> **Nota técnica:** Queda prohibido usar píxeles (`px`) estáticos para márgenes o paddings. Todo debe ir en `rem` siguiendo la escala de arriba.

**Dimensions (Tono y Comunicación)**<br>
El estilo de comunicación de SmartLock es **directo y técnico**. Como ingenieros, no queremos meterle "floro" innecesario al usuario.
* Si alguien intenta entrar y no tiene permiso, el sistema dice **"Acceso Denegado"**, sin vueltas.
* Usamos términos que un jefe de seguridad entienda rápido (como "Trazabilidad", "Cifrado" o "Autenticación").
* La idea es que la plataforma sea una herramienta de trabajo estricta, libre de narrativa irrelevante, para que la toma de decisiones sea rápida.

---

### 4.1.2. Web Style Guidelines

Aquí es donde aterrizamos todo para que la plataforma web se vea de nivel profesional:

1.  **Cero Adornos:** Si un botón o un icono no ayuda a monitorear o gestionar la seguridad, se quita. Queremos una interfaz limpia donde el control sea el protagonista.
2.  **Todo es Responsive:** El administrador puede estar en su oficina con un monitor gigante o en la entrada con su tablet. La estructura no debe romperse y los elementos deben ser fáciles de tocar/clickear en cualquier dispositivo.
3.  **Jerarquía Visual:** Usamos el contraste y los colores semánticos para que el ojo sepa qué es urgente.
* **Rojo:** Alertar brechas de seguridad o intentos fallidos.
* **Verde/Azul:** Accesos válidos y sistema operativo.
* **Amarillo:** Dar advertencias ante cualquier problema.
## 4.2. Information Architecture.
En SmartLock, la arquitectura de la información no es solo un menú de opciones; es el cerebro que permite que un administrador no entre en pánico cuando hay cientos de personas moviéndose por sus instalaciones. En el mundo de la seguridad digital, un segundo de duda puede ser un problema grave. Por eso, hemos diseñado una estructura donde la información crítica (como quién entró por la puerta principal hace un segundo) siempre está a la vista, eliminando cualquier "floro" visual que distraiga de lo importante: el control total y en tiempo real.

---

### 4.2.1. Organization Systems.
Para que SmartLock sea realmente eficiente tanto para el guardia en la puerta como para el administrador del sistema, hemos decidido combinar varios sistemas de organización:

### **Organización visual del contenido**
* **Jerárquica (Visual Hierarchy):** Elegimos este sistema porque en seguridad hay datos que "gritan" más fuerte que otros. En el Dashboard, los intentos de acceso fallidos o las alertas de puertas forzadas utilizan un tamaño y color prominente (rojo/bold). No es solo estética; es una estrategia para que el ojo del usuario sepa qué atender primero sin tener que leer toda la pantalla.
* **Organización secuencial (Step-by-step):** Registrar una nueva cerradura inteligente o dar de alta a un nuevo usuario puede ser tedioso. Lo dividimos en pasos claros (Identificación > Asignación de Permisos > Vinculación de Hardware) para evitar que el usuario se sienta abrumado y garantizar que no se salte ningún protocolo de seguridad.

### **Esquemas de categorización de contenido**
* **Por tópicos (Zonas de Acceso):** Organizamos la info por "Zonas" (ej. Piso 1, Almacén, Oficinas). Es la forma más lógica en la que un administrador piensa su espacio físico.
* **Según audiencia (Roles de Usuario):** El "Usuario Final" solo ve su llave digital y su historial personal. El "Administrador" ve todo el panel de control y analíticas. Esto "limpia" la interfaz de cada usuario, mostrándole solo lo que es relevante para su rol.
* **Cronológico:** Es vital para el Log de Eventos. Si pasa algo, necesitamos reconstruir la historia de forma lineal. Mostramos los ingresos por hora y fecha para que la trazabilidad sea impecable.
* **Alfabético:** Lo reservamos para el directorio de usuarios y empleados, donde la búsqueda por nombre de la A a la Z es la forma más rápida de encontrar a alguien.

---
### 4.2.2. Labeling Systems.

En el sistema de etiquetado de SmartLock, hemos huido del lenguaje genérico. Queremos que el usuario sienta que el software es una herramienta técnica y profesional:

* **Panel de Control:** En lugar de "Inicio", porque aquí es donde realmente se gestiona todo el hardware.
* **Bitácora de Accesos:** Suena más profesional que "Historial". Da la idea de un registro oficial y serio de cada movimiento para auditorías.
* **Credenciales Digitales:** Término usado para referirse a los permisos de acceso de los usuarios, reforzando la idea de seguridad y autenticación.
* **Puntos de Control:** En lugar de "Puertas", porque SmartLock puede controlar desde una puerta hasta un torniquete o una barrera vehicular.

---

### 4.2.3. SEO Tags and Meta Tags
Queremos que SmartLock sea lo primero que aparezca cuando una empresa busque modernizar su seguridad.

### **Landing Page**
* **Título:** `<title>SmartLock | Control de Accesos Inteligente y Seguridad Digital</title>`
* **Descripción:** `<meta name="description" content="Moderniza la seguridad de tu edificio. SmartLock ofrece gestión de accesos en tiempo real, trazabilidad total y control desde la nube para oficinas y universidades."/>`
* **Keywords:** `<meta name="keywords" content="SmartLock, Control de accesos, Seguridad digital, Cerraduras inteligentes, Trazabilidad, SmartTecnologies, Software de seguridad Perú, ConTech."/>`
* **Autor:** `<meta name="author" content="SmartTecnologies" />`

### **Web Application**
* **Título:** `<title>Dashboard SmartLock - Gestión de Accesos</title>`
* **Descripción:** `<meta name="description" content="Panel de administración de SmartLock. Monitorea ingresos, gestiona usuarios y configura tus puntos de control en tiempo real."/>`

---

### 4.2.4. Searching Systems.
No queremos que el usuario "busque", queremos que "encuentre" rápido:

* **Búsqueda Predictiva:** A medida que el administrador escribe (ej. un DNI o nombre), el sistema sugiere usuarios registrados para ahorrar tiempo.
* **Filtros de Facetas:** El usuario puede refinar los registros por **Rango de fechas**, **Zona de acceso**, **Estado de ingreso** (Exitoso/Denegado) y **Tipo de usuario**, evitando la sobrecarga de información.
* **Búsqueda por Dispositivo:** Permite localizar rápidamente una cerradura o sensor específico dentro de toda la infraestructura mediante su ID técnico.

---
### 4.2.5. Navigation Systems.
La navegación en SmartLock está pensada para ser "invisible" y eficiente:

* **Menú Lateral Retráctil:** Prioriza el espacio de trabajo central para ver los mapas de calor y tablas de acceso, manteniendo los módulos principales a un solo clic.
* **Migas de Pan (Breadcrumbs):** Vital para no perderse cuando navegas por sedes (ej. Sedes > Lima Centro > Piso 3 > Laboratorio A), permitiendo al usuario ubicarse en todo momento.
* **Acciones Contextuales:** El sistema ofrece botones inteligentes según el estado del punto de control (ej. si una puerta detecta una intrusión, el botón principal será "Bloquear Acceso" o "Contactar Seguridad").
## 4.3. Landing Page UI Design.
En esta sección se detalla el proceso de diseño de la interfaz de usuario para la página de aterrizaje de **SmartLock**. El diseño se centra en la conversión de usuarios y la exposición clara de la propuesta de valor del sistema de control de acceso.
### 4.3.1. Landing Page Wireframe.
El wireframe de baja fidelidad define la estructura visual y la jerarquía de la información. Se ha priorizado una navegación intuitiva, destacando las funcionalidades principales y los beneficios de seguridad del sistema.
![Landing Page Wireframe](/Resources/LandingPage/Wireframe%20Landing%20Page.png)
* **Elementos clave:** Estructura de navegación, sección hero con llamado a la acción (CTA) y secciones de beneficios para el segmento de negocios.
### 4.3.2. Landing Page Mock-up.
El mock-up de alta fidelidad integra la identidad visual de la marca, incluyendo la paleta de colores, tipografía y elementos gráficos finales. Este diseño representa la apariencia exacta que tendrá la aplicación web una vez implementada.
![Landing Page Mock-up](/Resources/LandingPage/Mockup%20Landing%20Page.png)
* **Detalles estéticos:** Uso de contrastes para mejorar la legibilidad y elementos visuales que refuerzan la confianza y modernidad del sistema **SmartLock**.
## 4.4. Web Applications UX/UI Design.
### 4.4.1. Web Applications Wireframes.
### 4.4.2. Web Applications Wireflow Diagrams.
### 4.4.3. Web Applications Mock-ups.
### 4.4.4. Web Applications User Flow Diagrams.
## 4.5. Web Applications Prototyping.
## 4.6. Domain-Driven Software Architecture.

En esta sección se define la arquitectura de software de **SmartLock** utilizando los principios de Diseño Orientado al Dominio (Domain-Driven Design - DDD). Nuestro enfoque busca alinear la complejidad técnica del sistema con las necesidades reales del negocio (control de accesos "Asset-Light"). 

Para la representación de la arquitectura, utilizaremos el **Modelo C4**, el cual nos permite visualizar el sistema en diferentes niveles de abstracción (Contexto, Contenedores y Componentes), facilitando la comprensión tanto para *stakeholders* de negocio como para el equipo de desarrollo. El stack tecnológico base seleccionado incluye React con TypeScript para el Frontend, Python para el Backend, y despliegue en la infraestructura de AWS.

### 4.6.1. Design-Level Event Storming

En esta sección se detalla el diseño táctico del sistema, profundizando en la arquitectura y los componentes técnicos necesarios para implementar la solución. A diferencia del Big Picture, el **Design-Level Event Storming** se enfoca en definir los límites de los agregados, los comandos que disparan cambios de estado y las políticas que gobiernan las reglas de negocio.

![Design-Level Event Storming](/Resources/Chapter4/eventStormin/design-level.jpeg)

**Descripción de los componentes identificados:**

* **Comandos (Azul):** Representan las intenciones de los usuarios o sistemas externos para realizar una acción específica (ej. "Generar Código QR", "Validar Acceso").
* **Agregados (Amarillo):** Son las entidades o grupos de objetos que mantienen la consistencia de los datos y ejecutan la lógica de negocio ante un comando.
* **Políticas (Lila):** Definen reacciones automáticas del sistema ante eventos específicos ("Siempre que ocurra el Evento X, ejecutar el Comando Y").
* **Modelos de Lectura (Verde):** Representan la información que el usuario visualiza en la interfaz para poder tomar una decisión y ejecutar un comando.
* **Eventos de Dominio (Naranja):** Indican que algo relevante para el negocio ha sucedido exitosamente (ej. "Código QR Generado", "Acceso Denegado").

Este modelado permite al equipo de desarrollo tener una guía clara para la implementación de los servicios y la definición de la lógica en el código.
### 4.6.2. Software Architecture Context Diagram

In this section, the team introduces the Software Architecture Context Diagram. This high-level overview illustrates the **SmartLock** software system as a central entity, surrounded by the key user personas and the external systems it interacts with to deliver its "Asset-Light" access control value proposition.

![Software Architecture Context Diagram](/Resources/Chapter4/umlfiles/contextDiagram.png)

**Explicación del diagrama:**

* **SmartLock System:** Es el núcleo de la plataforma que centraliza la lógica de generación de códigos QR dinámicos y la validación de reglas de acceso.
* **Usuarios:** El diagrama identifica al **Administrator** (configuración), **Security Staff** (validación móvil) y **Attendee** (usuario final) como los actores principales.
* **Sistemas Externos:** Se detalla la integración con **AWS SES** para la gestión de correos electrónicos y **Twilio API** para el envío de alertas críticas de seguridad vía SMS.

### 4.6.3. Software Architecture Container Level Diagram

In this section, the team presents the **Container Diagram** for SmartLock. This diagram expands the system's context to reveal the software containers that compose it (web applications, mobile applications, APIs, and databases). It illustrates the high-level distribution of responsibilities, exposes key technology decisions—such as Angular for the frontend, Java Spring Boot for the backend, and MySQL for persistence—and details how these containers communicate through the AWS cloud infrastructure.

![Software Architecture Container Diagram](/Resources/Chapter4/umlfiles/containerDiagram.png)

#### Diagram Explanation

The Container Diagram breaks down the internal architecture of SmartLock into the following key components:

* **Landing Page & Web Application (Frontend):** Developed using **Angular, TypeScript, and TailwindCSS**. The web application acts as a Single Page Application (SPA) that consumes the backend API. Both containers are hosted on **AWS S3** and distributed globally via **Amazon CloudFront** to ensure low latency and security via HTTPS.
* **Scanner Mobile App:** A specialized application for security staff, optimized for scanning QR codes and communicating with the server with minimal latency.
* **Core Backend API:** The system's main engine, developed in **Java using the Spring Boot framework**. It centralizes all domain-driven business logic (DDD), validates access attempts, and generates encrypted dynamic QR codes. It is deployed on **AWS Elastic Beanstalk** for automated load balancing and scaling.
* **Relational Database:** A **MySQL** database hosted on **Amazon RDS**, serving as the single source of truth. it ensures the immutability of access logs (audit trails) and the integrity of user profiles and access rules.
* **Communication:** The frontend and mobile app communicate asynchronously with the Backend API via **JSON over HTTPS**. The backend interacts with the database through **JDBC** and with third-party services (AWS SES and Twilio) via REST APIs.

### 4.6.4. Software Architecture Components Diagrams

In this section, the team presents the **Component Diagram** for the Core Backend API container. This diagram zooms into the Java Spring Boot application to illustrate its internal structure based on Domain-Driven Design (DDD) and Layered Architecture. It shows how the system is divided into Controllers (Presentation), Services (Business Logic/Domain), and Repositories (Data Access), and how these components interact to execute the access control logic.

![Software Architecture Component Diagram](/Resources/Chapter4/umlfiles/componentDiagram.png)

#### Diagram Explanation

The Component Diagram breaks down the **Core Backend API** into the following functional layers:

* **Controllers (Presentation Layer):**
  * **Auth & Security Controller:** Exposes REST endpoints to handle user login, 2FA verification, and JSON Web Token (JWT) issuance.
  * **Access Validation Controller:** Receives API calls from the Scanner Mobile App to validate dynamic QR payloads in real-time.
  * **Space Manager Controller:** Provides endpoints for administrators (via the Web App) to perform CRUD operations on physical spaces and configure access schedules.

* **Services (Domain / Business Logic Layer):**
  * **Access Credential Service (Core Domain):** The heart of the system. It evaluates complex access policies, generates dynamic QR codes using cryptographic signatures, and determines whether an access attempt is granted or denied.
  * **Authentication Service:** Implements Role-Based Access Control (RBAC) and manages the lifecycle of credentials and tokens.
  * **Notification Publisher:** Uses the Spring ApplicationEventPublisher to asynchronously delegate alerts to prevent blocking the main execution thread during access validations.

* **Repositories (Infrastructure Layer):**
  * **Audit & Log Repository:** Uses Spring Data JPA to securely write immutable logs of every access attempt and security event into the database.
  * **Domain Data Repository:** Manages the persistence of user profiles, organizational data, doors, and policies.

* **Communication Flow:** The web and mobile applications send HTTP requests to the **Controllers**. These controllers delegate the business logic to the **Services**. The services evaluate the rules and use the **Repositories** to interact with the MySQL database via JDBC, or use the **Notification Publisher** to dispatch asynchronous emails and SMS via AWS SES and Twilio.

## 4.7. Software Object-Oriented Design

En esta sección, el equipo presenta el diseño orientado a objetos del software, detallando la implementación interna y la estructura de componentes para cada *Bounded Context* de **SmartLock**. Los diagramas a continuación ilustran cómo se ha aplicado el enfoque de *Domain-Driven Design* (DDD) a nivel de código, definiendo claramente las responsabilidades, los límites de los agregados y los patrones de diseño utilizados tanto en la capa de presentación (Frontend) como en la lógica de negocio (Backend). Esta estructura garantiza un código modular, mantenible y altamente escalable.

---

### 4.7.1. Class Diagrams.

#### Diagrama de clases (Frontend)

<img src="/Resources/Diagram-Class/Frontend/Class-Diagram-Frontend-image.png">

El diagrama organiza el frontend de SmartLock en cinco 
Bounded Contexts (Authentication, Organization, User, 
Security y Subscription), lo que permite aislar la lógica 
de negocio y asegurar que cada módulo evolucione de forma 
independiente. Dentro de estos contextos, se implementan 
los 8 Agregados definidos, donde entidades raíz como Security 
y Organization encapsulan a Door y Office respectivamente; 
esto garantiza la integridad del sistema, ya que cualquier 
cambio de estado físico o estructural debe ser validado 
por su respectiva raíz de agregado antes de impactar la interfaz.

Bajo el enfoque DDD, la aplicación utiliza un EventBus 
en la capa Shared para comunicar eventos entre contextos
de forma desacoplada y emplea el patrón Assembler para
transformar los datos crudos de la API en objetos de dominio 
con comportamiento propio. Los Stores de la capa de aplicación 
gestionan estos agregados mediante Signals, permitiendo 
que la interfaz reaccione instantáneamente a cambios operativos 
—como la apertura de una puerta o la actualización de un perfil—
sin comprometer la separación de responsabilidades ni la pureza 
del modelo de negocio.

#### Diagrama de clases (Backend)

<img src="/Resources/Diagram-Class/Backend/Class-Diagram-Backend-image.png">

El backend de nuestro proyecto SmartLock lo hemos armado siguiendo 
a tope la arquitectura DDD en SpringBoot, separando todo en los 5 
Bounded Contexts y los 8 agregados que sacamos del Event Storming 
para que no sea un espagueti de código. Usamos Aggregate Roots como 
Security y Organization para mandar sobre entidades como Door y Office, 
asegurando que ninguna puerta se abra si no pasa por las reglas del 
negocio. Metimos patrones que vimos en clase como el Assembler para 
limpiar los datos que vienen del front, usamos Records para que los 
DTOs sean inmutables y puras Interfaces en los servicios y repositorios 
para que el sistema sea fácil de mantener y escalar si luego queremos 
cambiar algo de la base de datos o la lógica de las suscripciones.

## 4.8. Database Design.

---

### 4.8.1. Database Diagrams.

<img src="/Resources/Data-Base-Diagram/Data-Base-Diagram-image.png">

El diagrama de base de datos para SmartLock se ha estructurado bajo un 
enfoque de normalización 3FN y Domain-Driven Design (DDD), organizando 
la información en Bounded Contexts que actúan como Aggregate Roots 
(como Users y Organization) para garantizar la integridad operativa y 
la escalabilidad mediante el uso de tipos de datos atómicos en MySQL. 
Desde la perspectiva de seguridad y persistencia, el diseño separa 
estrictamente las credenciales en authentications y los datos sensibles 
en user_profiles (con correos encriptados) para cumplir con las leyes 
de protección de datos, mientras que la tabla access_logs asegura una 
auditoría inmutable de cada evento físico. Finalmente, la arquitectura 
está totalmente optimizada para un ORM como Hibernate, facilitando el 
mapeo de relaciones uno-a-muchos y uno-a-uno mediante claves foráneas 
claras y tipos bigint, lo que permite un manejo eficiente de la carga 
perezosa (Lazy Loading) y una transición fluida del modelo relacional 
al código en Spring Boot.

---
