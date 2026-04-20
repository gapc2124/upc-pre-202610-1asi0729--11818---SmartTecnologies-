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
## 4.6. Domain-Driven Software Architecture

En esta sección se define la arquitectura de software de **SmartLock** utilizando los principios de Diseño Orientado al Dominio (Domain-Driven Design - DDD). Nuestro enfoque busca alinear la complejidad técnica del sistema con las necesidades reales del negocio (control de accesos "Asset-Light"). 

Para la representación de la arquitectura, utilizaremos el **Modelo C4**, el cual nos permite visualizar el sistema en diferentes niveles de abstracción (Contexto, Contenedores y Componentes), facilitando la comprensión tanto para *stakeholders* de negocio como para el equipo de desarrollo. El stack tecnológico base seleccionado incluye React con TypeScript para el Frontend, Python para el Backend, y despliegue en la infraestructura de AWS.

### 4.6.1. Design-Level Event Storming
### 4.6.2. Software Architecture Context Diagram

El diagrama de contexto (Nivel 1 del Modelo C4) ilustra a **SmartLock** como una caja negra en el centro de su ecosistema, mostrando las interacciones de alto nivel con los usuarios (Administradores, Staff y Asistentes) y los sistemas externos de los cuales depende para funcionar (proveedores de nube y mensajería).

**Descripción de las interacciones:**
1. **Administradores / Organizadores:** Interactúan con el sistema para configurar espacios, cargar listas de usuarios y descargar reportes.
2. **Staff de Seguridad:** Utilizan el sistema (vía móvil) exclusivamente para escanear y validar credenciales.
3. **Empleados / Asistentes:** Interactúan pasivamente al recibir su credencial digital y mostrarla en puerta.
4. **Sistemas Externos:** SmartLock delega el envío masivo de correos a un proveedor externo (AWS SES) y las notificaciones a un servicio de mensajería (Twilio API).

![Software Architecture Context Diagram](../Resources/Architecture/SmartLock_Context-Diagrama_de_Contexto__Nivel_1____SmartLock.png)

### 4.6.3. Software Architecture Container Diagrams

El **Diagrama de Contenedores (Nivel 2 del Modelo C4)** hace un "zoom" a la plataforma SmartLock para revelar su estructura técnica interna. En esta sección se detallan las aplicaciones web, aplicaciones móviles, bases de datos y APIs que conforman el sistema.

* **1. Web Application (Frontend):** Desarrollada en React con TypeScript. Es el panel de control tipo SPA donde los administradores configuran sus espacios y visualizan métricas.
* **2. Mobile Application (Scanner App):** App móvil rápida para el Staff de seguridad, diseñada para leer los QR dinámicos usando la cámara con latencia mínima.
* **3. Core Backend API:** Desarrollada en Python (FastAPI). Contiene toda la lógica de negocio, generación de códigos QR encriptados y validación de reglas de acceso.
* **4. Relational Database:** Base de datos PostgreSQL (AWS RDS) que almacena los perfiles, espacios y el registro inmutable de auditoría.

![Software Architecture Container Diagram](../Resources/Architecture/SmartLock_Containers-Diagrama_de_Contenedores__Nivel_2____SmartLock.png)

### 4.6.4. Software Architecture Components Diagrams

El **Diagrama de Componentes (Nivel 3 del Modelo C4)** hace un acercamiento al contenedor principal: el **Core Backend API**. Este diagrama expone la arquitectura interna organizada modularmente según los principios de DDD.

* **1. Auth & Security Controller:** Punto de entrada para la autenticación y emisión de tokens JWT.
* **2. Space & Event Manager:** Gestiona la creación de locaciones físicas y asignación de aforos.
* **3. Access Credential Service (Core Domain):** Recibe la lista de usuarios, genera códigos QR dinámicos con firma criptográfica y evalúa reglas de negocio en tiempo real.
* **4. Notification Publisher:** Componente asíncrono que delega el envío de correos y alertas a servicios externos.
* **5. Audit & Log Repository:** Registra cada intento de acceso en la base de datos garantizando un historial inmutable.

![Software Architecture Components Diagram](../Resources/Architecture/SmartLock_Components-Diagrama_de_Componentes__Nivel_3____Core_Backend_API__SmartLock_.png)

## 4.7. Software Object-Oriented Design

En esta sección se detalla el diseño orientado a objetos del sistema **SmartLock**, traduciendo los requerimientos de negocio y la arquitectura del dominio en estructuras de software concretas mediante el paradigma POO. Se definen las clases principales, sus atributos, métodos y las relaciones (herencia, agregación y composición) que interactúan dentro del *Core Backend API*.

### 4.7.1. Class Diagrams

El siguiente diagrama de clases ilustra el modelo de dominio central del sistema. Se ha aplicado el principio de herencia para gestionar los diferentes tipos de usuarios (`Admin`, `Staff` y `Attendee`) a partir de una clase base común `User`. Asimismo, se detalla la relación central del negocio: un `Space` emite múltiples `Credentials` (QR dinámicos), las cuales, al ser escaneadas por el `Staff`, generan instancias de `AccessLog`.

![Class Diagram](../Resources/Architecture/SmartLock_ClassDiagram-Diagrama_de_Clases___Core_Domain__SmartLock_.png)

## 4.8. Database Design

En esta sección se detalla el diseño relacional de la base de datos de **SmartLock**, implementada utilizando el motor **PostgreSQL** en AWS RDS. El diseño garantiza la integridad referencial, la normalización de los datos (hasta la tercera forma normal) y la optimización para consultas de alta concurrencia, aspectos críticos para un sistema de control en tiempo real.

### 4.8.1. Database Diagrams

A continuación, se presenta el Diagrama Entidad-Relación (ERD) físico del sistema central utilizando la notación *Crow's Foot*. Este modelo define las tablas principales (`users`, `spaces`, `credentials` y `access_logs`), los tipos de datos, y las llaves primarias (PK) y foráneas (FK) que establecen las relaciones estructurales.

![Database ERD Diagram](../Resources/Architecture/SmartLock_ERD-Diagrama_Entidad_Relación__ERD____SmartLock_Database.png)