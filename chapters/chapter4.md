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
### 4.8.1. Database Diagrams.