# Capítulo V: Product Implementation, Validation & Deployment.
## 5.1. Software Configuration Management.

En esta sección, el equipo establece las decisiones, herramientas y convenciones que permiten mantener la consistencia técnica durante el ciclo de vida de **SmartLock**. Para la gestión del código fuente, se utiliza **GitHub** bajo una estrategia de **GitHub Flow**, donde las ramas `main` y `develop` centralizan el código estable, aplicando la convención de **Conventional Commits** para garantizar un historial de cambios legible.

El entorno de desarrollo se ha estandarizado utilizando **Visual Studio Code** para el frontend y **IntelliJ IDEA** para el backend. El stack tecnológico comprende una **Landing Page** construida con HTML, CSS y JavaScript; una **Web Application** desarrollada en **Angular con TypeScript** utilizando **TailwindCSS** para el diseño de interfaces; y un **Backend** robusto desarrollado en **Java (JDK 17+)** gestionado con Maven. La persistencia de datos se maneja en **MySQL 8.0**, siguiendo convenciones de nomenclatura en `snake_case` y normalización 3FN para las tablas del sistema.

En cuanto a la configuración del despliegue, el equipo ha optado por un ecosistema basado íntegramente en **Amazon Web Services (AWS)**. El frontend se aloja en buckets de **Amazon S3** distribuidos mediante **Amazon CloudFront** para asegurar baja latencia y certificados SSL vía HTTPS. El backend se despliega sobre **AWS Elastic Beanstalk** para aprovechar el autoescalado y balanceo de carga, mientras que la base de datos se gestiona a través de **Amazon RDS (MySQL)**, lo que garantiza respaldos automatizados y alta disponibilidad. Finalmente, se utiliza **GitHub Actions** para automatizar el pipeline de CI/CD, permitiendo que cada integración validada se sincronice de forma inmediata con la infraestructura de nube.

### 5.1.1. Software Development Environment Configuration

En esta sección, se especifican las herramientas y productos de software utilizados por los miembros del equipo para colaborar en todas las fases del ciclo de vida de **SmartLock**. La configuración del entorno de desarrollo asegura la interoperabilidad y consistencia técnica, cubriendo desde la gestión del proyecto hasta el despliegue final en la nube.

| Producto | Categoría | Propósito de uso | Ruta de Referencia / Descarga |
| :--- | :--- | :--- | :--- |
| **Jira Software** | Project & Requirements Management | Gestión del Product Backlog, planificación de Sprints y seguimiento de User Stories. | [https://upc-team-open-source.atlassian.net/](https://upc-team-open-source.atlassian.net/) |
| **Figma** | Product UX/UI Design | Diseño de Wireframes, Mock-ups y prototipado interactivo de la Web App y Landing Page. | [https://www.figma.com/](https://www.figma.com/) |
| **UXPressia** | Product UX Design | Elaboración de artefactos de diseño de experiencia como User Personas y Journey Maps. | [https://uxpressia.com/](https://uxpressia.com/) |
| **Visual Studio Code** | Software Development | IDE principal para el desarrollo del Frontend (Angular) y la Landing Page (HTML/CSS/JS). | [https://code.visualstudio.com/](https://code.visualstudio.com/) |
| **IntelliJ IDEA** | Software Development | IDE principal para el desarrollo del Backend RESTful API utilizando Java y Spring Boot. | [https://www.jetbrains.com/idea/](https://www.jetbrains.com/idea/) |
| **MySQL Workbench** | Software Development | Herramienta para el diseño, modelado y gestión local de la base de datos relacional. | [https://dev.mysql.com/downloads/workbench/](https://dev.mysql.com/downloads/workbench/) |
| **GitHub** | SCM & Software Documentation | Repositorio centralizado de código fuente y documentación técnica del proyecto. | [https://github.com/202610-1asi0729-11881-SmartIndustries](https://github.com/202610-1asi0729-11881-SmartIndustries) |
| **AWS Management Console** | Software Deployment | Gestión y monitoreo de servicios en la nube (S3, CloudFront, Elastic Beanstalk y RDS). | [https://aws.amazon.com/console/](https://aws.amazon.com/console/) |
| **Swagger / OpenAPI** | Software Documentation | Documentación interactiva y pruebas de los servicios web RESTful del backend. | Integrado en el Core Backend API. |

---### 5.1.2. Source Code Management

En esta sección, el equipo establece los medios y el esquema de organización que aplicará para el seguimiento de modificaciones durante el ciclo de vida de **SmartLock**. Para ello, utilizamos **GitHub** como plataforma centralizada y sistema de control de versiones.

A continuación, se presentan los enlaces a la organización y los 4 repositorios que conforman la solución integral:

* **Organización en GitHub:** [https://github.com/202610-1asi0729-11881-SmartIndustries](https://github.com/202610-1asi0729-11881-SmartIndustries)
* **Landing Page:** [https://github.com/202610-1asi0729-11881-SmartIndustries/-SmartLock--website](https://github.com/202610-1asi0729-11881-SmartIndustries/-SmartLock--website)
* **Frontend Web Application:** [https://github.com/202610-1asi0729-11881-SmartIndustries/-SmartLock--webapp](https://github.com/202610-1asi0729-11881-SmartIndustries/-SmartLock--webapp)
* **Web Services (Core Backend API):** [https://github.com/202610-1asi0729-11881-SmartIndustries/-SmartLock--platform](https://github.com/202610-1asi0729-11881-SmartIndustries/-SmartLock--platform)
* **Project Report:** [https://github.com/202610-1asi0729-11881-SmartIndustries/-SmartLock--report](https://github.com/202610-1asi0729-11881-SmartIndustries/-SmartLock--report)

#### Implementación de GitFlow
Para mantener un flujo de trabajo ordenado, el equipo ha implementado **GitFlow** como *workflow* de control de versiones. Este modelo estructura nuestro trabajo en las siguientes ramas (*branches*):

**Ramas Principales:**
* `main`: Rama principal que contiene el código estable y listo para producción.
* `develop`: Rama de integración donde se fusionan las nuevas características antes de pasar a producción.

**Ramas de Soporte y Convenciones:**
* **Feature branches:** Cada nueva historia de usuario tiene su propia rama. Se crean a partir de `develop` y se fusionan de vuelta en `develop`.
  * *Convención de nombre:* `feature/<descripcion-corta>` (Ejemplo: `feature/qr-generation`).
* **Release branches:** Se utilizan para preparar una nueva versión para producción. Se ramifican desde `develop` y se fusionan en `main` y `develop`.
  * *Convención de nombre:* `release/v<version>` (Ejemplo: `release/v1.1.0`).
* **Hotfix branches:** Destinadas a solucionar errores críticos en producción. Se crean desde `main` y se fusionan en `main` y `develop`.
  * *Convención de nombre:* `hotfix/<descripcion-error>` (Ejemplo: `hotfix/login-crash`).

#### Semantic Versioning (SemVer)
Para nombrar las versiones en nuestras ramas de Release y en los *tags* de producción, aplicamos **Semantic Versioning 2.0.0** (`vMAJOR.MINOR.PATCH`):
* **MAJOR:** Cambios incompatibles en la API.
* **MINOR:** Nuevas funcionalidades retrocompatibles.
* **PATCH:** Corrección de errores retrocompatibles.

#### Conventional Commits
El equipo aplica el estándar **Conventional Commits** en todos los mensajes de los commits para asegurar un historial legible:
* `feat`: Nueva característica (ej. `feat(auth): add login`).
* `fix`: Corrección de un error (ej. `fix(ui): adjust button spacing`).
* `docs`: Modificaciones en documentación (ej. `docs: update repo links`).
* `style`: Cambios de formato que no afectan la lógica.
* `refactor`: Mejora de código sin añadir funciones ni arreglar bugs.
* `test`: Adición o corrección de pruebas.
* `chore`: Mantenimiento y actualización de configuraciones.
### 5.1.3. Source Code Style Guide & Conventions.
### 5.1.4. Software Deployment Configuration.
## 5.2. Landing Page, Services & Applications Implementation.
### 5.2.1. Sprint 1
#### 5.2.1.1. Sprint Planning 1.
#### 5.2.1.2. Aspect Leaders and Collaborators.
### Aspect Leaders and Collaborators

* En esta sección se presenta la **Leadership-and-Collaboration Matrix (LACX)**. Esta matriz detalla los líderes (L) y colaboradores (C) para cada aspecto clave del Sprint, asegurando una comunicación clara y una distribución de responsabilidades eficiente para el proyecto **SmartLock**.

La organización de líderes y colaboradores está directamente relacionada con la selección de tareas (tasks) que se desarrollarán durante el Sprint.

| Team Member | GitHub Username | Arquitectura & DDD (L/C) | Desarrollo Backend & API (L/C) | Simulacion IoT & Hardware (L/C) | Frontend & UI/UX (L/C) | QA & Testing (L/C) |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| Ayllon Pauccar, Juan David | JuanDPAUC | C | C | C | C | L |
| Limache Coronel, Imanol Fabricio | ImaLi06 | C | C | L | C | C |
| Huaman Oscco Aldo Jesus | Jesusho22 | C | C | C | L | C |
| Palacios Tinoco Adrian Fernando | AdranP3107 | C | L | C | C | C |
| Peñaranda Caldas Gabriel Augusto | gapc2124 | L | C | C | C | C |
---

> **Leyenda:**  </br>
> **L:** Lider (Líder del aspecto)  
> **C:** Colaborador (Colaborador y desarrollo)

#### 5.2.1.3. Sprint Backlog 1.

* "Nuestro objetivo a sido consolidar el núcleo de seguridad y gestión de identidades del sistema SmartLock, de manera teorica hemos logrado la implementación de mecanismos de autenticación, aislamiento total de datos por cliente y blindaje contra ataques externos. Con esto, hemos transformado un diseño conceptual en una infraestructura técnica funcional que garantiza que solo las personas correctas tengan acceso a los recursos correctos, bajo un entorno de comunicación 100% cifrado y seguro. Esperamos que nuestros clientes tengan siempre la seguridad de que nuestro producto sera 100% confiable y eficiente"

|<img src="../Resources/Herramientas/Sprint.png" alt="Estructura de prioridad" width="850"/> |s

<https://upc-team-open-source.atlassian.net/?continue=https%3A%2F%2Fupc-team-open-source.atlassian.net%2Fwelcome%2Fsoftware%3FprojectId%3D10000&atlOrigin=eyJpIjoiNjJkNmViYTYyM2ZmNGMzMDlmYjRiMDQ0MTNkMGVkZDIiLCJwIjoiamlyYS1zb2Z0d2FyZSJ9>

##### **Sprint 1 - Formato**

| **Sprint #** | **Sprint 1** | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **User Story** | **Work-Item / Task** | | | | | |
| **Id** | **Título** | **Id** | **Título** | **Descripción** | **Est. (Hrs)** | **Asignado** | **Status** |
| SMAR-33 | Encriptación | T-33-1 | Hash de claves | Programar la función para que las contraseñas se guarden "encriptadas" en la base de datos usando la librería Bcrypt. | 4 | Adrian | To-Do |
| SMAR-33 | Encriptación | T-33-2 | Pruebas de Login | Verificar que al loguearse, el sistema compare correctamente la clave escrita con la encriptada en la DB. | 3 | Adrian | To-Do |
| SMAR-34 | Datos en tránsito | T-34-1 | Configuración HTTPS | Configurar el servidor (o el entorno local) para que la URL use el candadito de seguridad (SSL). | 4 | Gabriel | To-Do |
| SMAR-34 | Datos en tránsito | T-34-2 | Redirección Segura | Hacer que si alguien entra por "http", la web lo mande automáticamente a "https". | 2 | Gabriel | To-Do |
| SMAR-45 | Data Isolation | T-45-1 | Campo de Empresa | Agregar una columna "Empresa_Id" en todas las tablas para separar los datos de cada cliente. | 6 | Imanol | To-Do |
| SMAR-45 | Data Isolation | T-45-2 | Filtro de Consultas | Programar la lógica para que un usuario solo pueda ver los registros que coincidan con su "Empresa_Id". | 8 | Imanol | To-Do |
| SMAR-01 | Login estándar | T-01-1 | Maquetado de Login | Crear la página visual (HTML/CSS) con el formulario de correo y contraseña que sea responsive. | 5 | Aldo | To-Do |
| SMAR-01 | Login estándar | T-01-2 | Conexión Backend | Programar el endpoint que recibe los datos del formulario y valida si el usuario existe. | 6 | Aldo | To-Do |
| SMAR-03 | Creación usuarios | T-03-1 | Formulario Registro | Diseñar la interfaz para que el Admin pueda escribir los datos de nuevos empleados. | 5 | Gabriel | To-Do |
| SMAR-03 | Creación usuarios | T-03-2 | Guardado de Usuario | Crear la función que inserta al nuevo usuario en la base de datos validando que el correo no esté repetido. | 5 | Gabriel | To-Do |
| SMAR-04 | Asignación roles | T-04-1 | Tabla de Roles | Crear en la base de datos los niveles (Admin, Staff, Monitor) y asignarlos a los usuarios. | 4 | Juan | To-Do |
| SMAR-04 | Asignación roles | T-04-2 | Control de Accesos | Programar que ciertas páginas o botones solo se activen si el usuario tiene el rol adecuado. | 6 | Juan | To-Do |
| SMAR-23 | Reset de clave | T-23-1 | Envío de Correo | Integrar el servicio de AWS para que el sistema envíe un mail automático al pedir el reset. | 6 | Imanol | To-Do |
| SMAR-23 | Reset de clave | T-23-2 | Link Temporal | Crear una página donde el usuario escriba su nueva clave usando un enlace que expire en 1 hora. | 5 | Imanol | To-Do |
| SMAR-26 | Cierre de sesión | T-26-1 | Botón de Salir | Programar la acción de "Cerrar sesión" que borre los datos guardados en el navegador. | 2 | Imanol | To-Do |
| SMAR-26 | Cierre de sesión | T-26-2 | Limpieza de Token | Asegurar que el servidor ya no acepte el token anterior una vez que el usuario salió. | 4 | Imanol | To-Do |
| SMAR-44 | Anti-Brute Force | T-44-1 | Contador de Fallos | Programar un contador que identifique si una misma persona falla su clave más de 5 veces. | 5 | Adrian | To-Do |
| SMAR-44 | Anti-Brute Force | T-44-2 | Bloqueo por tiempo | Hacer que el sistema impida el acceso a esa cuenta por 15 minutos tras los fallos detectados. | 4 | Adrian | To-Do |
| SMAR-51 | Complejidad clave | T-51-1 | Reglas de Clave | Crear las validaciones para que la clave sea difícil (mínimo 8 letras, un número y un símbolo). | 3 | Juan | To-Do |
| SMAR-51 | Complejidad clave | T-51-2 | Mensajes de Error | Mostrar mensajes en rojo al usuario si su clave es muy débil mientras la está escribiendo. | 3 | Juan | To-Do |
| SMAR-81 | Manejo Errores | T-81-1 | Pantalla de Error | Crear una página o alerta amigable para cuando el servidor falle, sin mostrar código técnico. | 5 | Aldo | To-Do |
| SMAR-81 | Manejo Errores | T-81-2 | Auditoría Interna | Configurar que el sistema guarde un archivo (log) con los errores reales para que el programador los revise. | 4 | Aldo | To-Do |
| SMAR-82 | CORS Policy | T-82-1 | Permisos de Dominio | Configurar el sistema para que solo acepte peticiones que vengan de tu propia web oficial. | 3 | Gabriel | To-Do |
| SMAR-82 | CORS Policy | T-82-2 | Seguridad de Cabeceras | Definir qué acciones (leer, escribir, borrar) están permitidas desde el navegador. | 3 | Gabriel | To-Do |
| **TOTAL HORAS** | | | | | **106** | | |

#### 5.2.1.5. Execution Evidence for Sprint Review.
#### 5.2.1.6. Services Documentation Evidence for Sprint Review.
#### 5.2.1.7. Software Deployment Evidence for Sprint Review.
#### 5.2.1.8. Team Collaboration Insights during Sprint.
## 5.3. Validation Interviews.
### 5.3.1. Diseño de Entrevistas.
### 5.3.2. Registro de Entrevistas.
### 5.3.3. Evaluaciones según heurísticas.
## 5.4. Video About-the-Product.