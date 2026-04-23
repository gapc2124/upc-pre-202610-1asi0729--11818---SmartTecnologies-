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