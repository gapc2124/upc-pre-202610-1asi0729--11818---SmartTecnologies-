# Capítulo II: Requirements Elicitation & Analysis

## 2.1 Competidores

### **Kisi (Control de Acceso en la Nube)** 
Es una solución global de gestión de accesos de nivel empresarial que centraliza el control de múltiples instalaciones en una única interfaz basada en la nube. Se especializa en modernizar infraestructuras existentes sin necesidad de reemplazarlas por completo.
<https://www.getkisi.com/enterprise>

##### **Características Principales**
* **Gestión de Identidad Avanzada:** Permite asignar privilegios detallados por usuario e integra sistemas de autenticación **SSO** y protocolos **SCIM** para sincronizar la base de datos de empleados automáticamente.
* **Seguridad y Auditoría:** Facilita el cumplimiento de normativas de seguridad física mediante la obtención de datos vía **API** y la generación de informes automáticos personalizados.
* **Seguridad Multicapa:** Ofrece opciones de autenticación de dos factores (**2FA**) y **WebAuthn** para elevar los estándares de protección.
* **Implementación Híbrida:** Su gran diferencial es la capacidad de conectarse a cerraduras y lectores ya instalados, lo que reduce los costos de implementación hasta en un **65%**.

##### **Estructura de Planes**

| Plan | Descripción / Enfoque | Ideal para |
| :--- | :--- | :--- |
| **Standard** | Control básico en la nube. | Oficinas pequeñas. |
| **CRM** | Integración con sistemas de gestión de clientes. | Negocios con membresías. |
| **Enterprise** | Auditorías estrictas e integraciones de IT avanzadas. | Grandes corporaciones. |

---
<https://pages.getkisi.com/hubfs/kisi-pricing-overview.pdf>
<br></br>

### **Acceso Total Perú (Soluciones Integrales de Automatización)**
**Perfil de la Empresa:** Empresa peruana en fase de expansión con más de 5 años de experiencia en el sector de seguridad inteligente. Su competitividad radica en la flexibilidad de hardware y una sólida trayectoria con instituciones públicas y privadas de alto perfil (MININTER, MINCETUR, UNI, entre otros).

##### **Líneas de Servicio y Planes**
* **Control de Acceso para Puertas:** Sistema versátil con soporte para múltiples métodos de validación: códigos, tarjetas, huellas biométricas, reconocimiento facial y **códigos QR**.
* **Gestión de Asistencia Biométrica:** Solución especializada para **Recursos Humanos** que permite el control detallado de asistencias, faltas y horas extras con gestión local o centralizada.
* **Control de Acceso Vehicular:** Automatización de entradas y salidas de vehículos enfocada en la eficiencia operativa y reducción de costos de personal.
* **Control Peatonal Centralizado:** Implementación de barreras físicas (**torniquetes o molinetes**) gestionadas por un software integrado e intuitivo para flujos masivos.

##### **Valor Agregado**

| Beneficio | Descripción |
| :--- | :--- |
| **Asesoría Personalizada** | Acompañamiento técnico previo para determinar la viabilidad según la infraestructura. |
| **Experiencia Local** | Conocimiento profundo del mercado peruano y cumplimiento de estándares para entidades estatales. |

---
<https://accesototalperu.com/control-de-acceso-puerta/>
<br></br>

### **Kronos por SEIDOR (Gestión de Fuerza Laboral y Tiempo)**
**Descripción General:** Solución de alto nivel distribuida por **SEIDOR**, diseñada para el control integral de la jornada laboral y la optimización de la productividad. Su enfoque principal es el cumplimiento normativo y la eficiencia operativa en empresas con grandes planillas y turnos complejos.

#### **Pilares Estratégicos**
* **Optimización de Costos Operativos:** Alinea el personal con la demanda del negocio. Controla el pago de **horas extras** y proyecta el gasto de horas-hombre en tiempo real mediante alertas automáticas.
* **Mitigación de Riesgos y Cumplimiento:** Automatiza la generación de horarios asegurando el cumplimiento de la **legislación laboral** y acuerdos sindicales. Valida que el personal cuente con certificaciones vigentes antes de asignar turnos.
* **Productividad y Rendimiento:** Gestiona descansos obligatorios para prevenir el agotamiento y facilita la creación de equipos basados en competencias específicas.
* **Experiencia del Empleado (Self-Service):** Interfaz intuitiva para dispositivos móviles (**iOS y Android**) que permite a los colaboradores gestionar su disponibilidad y preferencias de turnos.

#### **Resumen de Valor**

| Enfoque | Objetivo Principal |
| :--- | :--- |
| **Financiero** | Control de presupuestos y reducción de sobrecostos laborales. |
| **Legal** | Automatización del cumplimiento de normativas vigentes. |
| **Humano** | Autogestión y bienestar del colaborador mediante movilidad. |

---
<https://www.seidor.com/es-pe/kronos>
<br></br>


### 2.1.1 Análisis Competitivo

# Competitive Analysis Landscape

<div align="justify">

> **¿Por qué llevar a cabo el desarrollo de un software de gestión de accesos habiendo modelos internacionales que gestionan la seguridad a nivel empresarial?**
> 
> **Objetivo:** [El objetivo de nuestro equipo es que los clientes vean nuestro software como una aplicación viable para la gestión de accesos de sus eventos o empresas, pudiendo ver reportes de asistencias, tardanzas e identificación de usuarios. Asimismo, facilitar la visualización de reportes que permitan analizar estadísticamente a sus colaboradores.]

| Sección | Detalle | SmartLock <br><img src="/Resources/Chapter2/Companies/SmartLock.png" alt="SmartLock" width="100"/> | Kisi <br><img src="/Resources/Chapter2/Companies/Kisi.png" alt="kisi" width="100"/> | Acceso total Peru <br><img src="/Resources/Chapter2/Companies/Atp.png" alt="Acceso-total-peru" width="100"/> | Kronos por Seidor <br><img src="/Resources/Chapter2/Companies/Seidor.jpg" alt="Kronos" width="100"/> |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Perfil** | Overview | [Es un modelo de gestión de accesos "Asset-Light" que utiliza códigos QR dinámicos para eliminar la inversión en hardware, orientado a empresas y eventos que buscan una implementación inmediata, económica y escalable.] | [Es una solución de seguridad física basada en la nube que unifica el control de múltiples sedes globales en una sola interfaz, optimizando los costos de instalación al integrar infraestructura antigua con protocolos modernos de identidad (SSO/SCIM).] | [Se especializa en la integración de hardware y soporte técnico local, ofreciendo sistemas de barreras físicas y biometría para instituciones que requieren una fiscalización presencial estricta y cumplimiento de normativas nacionales.] | [Es una plataforma de Workforce Management estratégica enfocada en grandes corporaciones, cuyo objetivo es maximizar la rentabilidad del capital humano mediante la automatización de horarios complejos y el control de costos laborales.] |
| | Ventaja competitiva (¿Qué valor ofrece?) | [Optimiza la gestión de identidades mediante un modelo SaaS basado en códigos QR dinámicos, eliminando la dependencia de hardware costoso para ofrecer una solución ágil y de bajo costo en accesos corporativos y eventos temporales.] | [Se posiciona como una solución de control de accesos en la nube de nivel empresarial, cuyo objetivo es modernizar infraestructuras físicas antiguas integrándolas con sistemas de identidad avanzados como SSO y SCIM.] | [Se especializa en la integración de hardware y automatización local, enfocándose en la instalación de barreras físicas y sistemas biométricos para instituciones que requieren un control presencial robusto en el mercado peruano.] | [Ofrece una plataforma estratégica de Workforce Management, diseñada para grandes corporaciones que buscan maximizar la productividad y garantizar el cumplimiento legal mediante la gestión compleja de turnos y planillas.] |
| **Perfil de Marketing** | Mercado objetivo | [Se dirige a PYMES, startups y productoras de eventos que buscan una solución de acceso "ligera" y digital, priorizando la agilidad sobre la infraestructura física.] | [Su mercado son empresas tecnológicas y corporativos globales con múltiples sedes que necesitan centralizar la seguridad física en la nube e integrarla con su stack de IT (SSO/SCIM).] | [Enfocado en el sector público, industrial y educativo nacional, donde se requiere una fiscalización presencial estricta y soluciones de hardware robustas (torniquetes y biometría).] | [Orientada a grandes corporaciones con operaciones complejas (retail, manufactura, salud) que gestionan miles de empleados y requieren un control riguroso de normativas laborales.] |
| | Estrategias de marketing | [Basada en marketing digital, resaltando la facilidad de configuración, el ahorro en hardware y la flexibilidad del modelo por uso o suscripción.] | [Se posiciona mediante Inbound Marketing especializado en IT, ofreciendo contenido técnico sobre ciberseguridad física y eficiencia operativa para gerentes de tecnología y seguridad.] | [Utiliza una estrategia de ventas consultivas y licitaciones, apoyándose en su historial con el Estado y testimonios de grandes instituciones locales para generar confianza técnica.] | [Emplea un enfoque de ABM y eventos corporativos de alto nivel, posicionándose como un aliado estratégico para la transformación digital de Recursos Humanos.] |
| **Perfil de Producto** | Productos & Servicios | [Software de generación de QR dinámicos, panel de administración para gestión de planillas y módulos específicos para el control de asistencia en eventos masivos.] | [Controladores inteligentes de puertas, lectores compatibles con smartphones y una plataforma centralizada que integra autenticación de dos factores (2FA) con sistemas de oficina existentes.] | [Venta e instalación de terminales biométricos, molinetes y barreras vehiculares, acompañados de software de gestión local y servicios de mantenimiento preventivo.] | [Suite integral de Workforce Management que incluye módulos de planificación de horarios, control de fatiga, gestión de certificados y autoservicio para el empleado.] |
| | Precios & Costos | [Modelo de suscripción mensual escalable (SaaS) o pago por evento, eliminando los costos iniciales de instalación y mantenimiento de hardware especializado.] | [Estructura de precios por niveles (Standard, CRM, Enterprise) que combina una tarifa de software recurrente con el costo de adquisición de sus controladores propietarios.] | [Modelo de venta directa de activos (CAPEX) con un costo inicial alto por equipo e instalación, sumado a contratos opcionales de soporte técnico y licencias locales.] | [Inversión de nivel Enterprise que incluye costos significativos de consultoría, implementación personalizada y licencias anuales por volumen de empleados gestionados.] |
| | Canales de distribución | [Distribución 100% digital mediante plataforma Web para administración y App móvil nativa para que los usuarios finales validen sus accesos mediante QR.] | [Canal híbrido que utiliza plataforma Web para control global y aplicaciones móviles que emplean Bluetooth/NFC para la apertura de puertas físicas.] | [Distribución mediante ventas directas y consultoría presencial, utilizando interfaces de software locales (On-premise) o centralizadas para el monitoreo de hardware.] | [Ecosistema multi-dispositivo con interfaz Web robusta para la gestión administrativa y aplicaciones móviles (iOS/Android) enfocadas en la autogestión de turnos por el personal.] |
| **Análisis SWOT** | Fortalezas | [Su modelo "Asset-Light" basado en QR dinámicos elimina la inversión en hardware, permitiendo una implementación inmediata y costos operativos mínimos.] | [Excelente capacidad de integración híbrida, permitiendo gestionar infraestructuras antiguas desde una plataforma en la nube de nivel global.] | [Sólida presencia local y soporte técnico presencial, lo que les otorga una ventaja competitiva en licitaciones con el Estado y sector industrial.] | [Capacidad inigualable para gestionar cumplimiento legal y optimización de nómina en entornos corporativos con turnos altamente complejos.] |
| | Debilidades | [La dependencia total de la conectividad y batería del smartphone del usuario puede generar fricción en puntos de acceso de alta criticidad.] | [El costo de adquisición sigue siendo elevado debido a la necesidad de sus controladores propietarios para centralizar el mando.] | [Su modelo de negocio depende excesivamente de la venta e instalación de activos físicos (CAPEX), lo que dificulta una escalabilidad rápida.] | [Posee una curva de aprendizaje muy alta y procesos de implementación extremadamente largos y costosos para el cliente promedio.] |
| | Oportunidades | [Existe un mercado masivo en la digitalización de PYMES y eventos temporales que buscan seguridad profesional sin contratos de mantenimiento pesados.] | [El crecimiento del trabajo híbrido impulsa la demanda de soluciones que permitan gestionar oficinas desde cualquier parte del mundo.] | [Expansión hacia soluciones de ciudades inteligentes y automatización de edificios en el mercado inmobiliario peruano en auge.] | [La creciente regulación sobre el control de horas trabajadas y bienestar laboral obliga a las grandes empresas a adoptar sistemas tan robustos como este.] |
| | Amenazas | [La entrada de gigantes del software que integren funciones de acceso gratuitas en sus ecosistemas de oficina (como Microsoft o Google).] | [Startups con tecnologías puramente móviles (NFC/Bluetooth) que eliminan la necesidad de cualquier hardware intermedio.] | [El rechazo progresivo a los métodos de contacto físico (biometría de huella) frente a tecnologías de reconocimiento remoto o digital.] | [Herramientas de gestión de proyectos y comunicación que están añadiendo módulos de control de tiempo (Time Tracking) mucho más intuitivos.] |

</div>

### **Kisi (Control de Acceso en la Nube)** 
Es una solución global de gestión de accesos de nivel empresarial que centraliza el control de múltiples instalaciones en una única interfaz basada en la nube. Se especializa en modernizar infraestructuras existentes sin necesidad de reemplazarlas por completo.
<https://www.getkisi.com/enterprise>

##### **Características Principales**
* **Gestión de Identidad Avanzada:** Permite asignar privilegios detallados por usuario e integra sistemas de autenticación **SSO** y protocolos **SCIM** para sincronizar la base de datos de empleados automáticamente.
* **Seguridad y Auditoría:** Facilita el cumplimiento de normativas de seguridad física mediante la obtención de datos vía **API** y la generación de informes automáticos personalizados.
* **Seguridad Multicapa:** Ofrece opciones de autenticación de dos factores (**2FA**) y **WebAuthn** para elevar los estándares de protección.
* **Implementación Híbrida:** Su gran diferencial es la capacidad de conectarse a cerraduras y lectores ya instalados, lo que reduce los costos de implementación hasta en un **65%**.

##### **Estructura de Planes**

| Plan | Descripción / Enfoque | Ideal para |
| :--- | :--- | :--- |
| **Standard** | Control básico en la nube. | Oficinas pequeñas. |
| **CRM** | Integración con sistemas de gestión de clientes. | Negocios con membresías. |
| **Enterprise** | Auditorías estrictas e integraciones de IT avanzadas. | Grandes corporaciones. |

---
<https://pages.getkisi.com/hubfs/kisi-pricing-overview.pdf>
<br></br>

### **Acceso Total Perú (Soluciones Integrales de Automatización)**
**Perfil de la Empresa:** Empresa peruana en fase de expansión con más de 5 años de experiencia en el sector de seguridad inteligente. Su competitividad radica en la flexibilidad de hardware y una sólida trayectoria con instituciones públicas y privadas de alto perfil (MININTER, MINCETUR, UNI, entre otros).

##### **Líneas de Servicio y Planes**
* **Control de Acceso para Puertas:** Sistema versátil con soporte para múltiples métodos de validación: códigos, tarjetas, huellas biométricas, reconocimiento facial y **códigos QR**.
* **Gestión de Asistencia Biométrica:** Solución especializada para **Recursos Humanos** que permite el control detallado de asistencias, faltas y horas extras con gestión local o centralizada.
* **Control de Acceso Vehicular:** Automatización de entradas y salidas de vehículos enfocada en la eficiencia operativa y reducción de costos de personal.
* **Control Peatonal Centralizado:** Implementación de barreras físicas (**torniquetes o molinetes**) gestionadas por un software integrado e intuitivo para flujos masivos.

##### **Valor Agregado**

| Beneficio | Descripción |
| :--- | :--- |
| **Asesoría Personalizada** | Acompañamiento técnico previo para determinar la viabilidad según la infraestructura. |
| **Experiencia Local** | Conocimiento profundo del mercado peruano y cumplimiento de estándares para entidades estatales. |

---
<https://accesototalperu.com/control-de-acceso-puerta/>
<br></br>

### **Kronos por SEIDOR (Gestión de Fuerza Laboral y Tiempo)**
**Descripción General:** Solución de alto nivel distribuida por **SEIDOR**, diseñada para el control integral de la jornada laboral y la optimización de la productividad. Su enfoque principal es el cumplimiento normativo y la eficiencia operativa en empresas con grandes planillas y turnos complejos.

#### **Pilares Estratégicos**
* **Optimización de Costos Operativos:** Alinea el personal con la demanda del negocio. Controla el pago de **horas extras** y proyecta el gasto de horas-hombre en tiempo real mediante alertas automáticas.
* **Mitigación de Riesgos y Cumplimiento:** Automatiza la generación de horarios asegurando el cumplimiento de la **legislación laboral** y acuerdos sindicales. Valida que el personal cuente con certificaciones vigentes antes de asignar turnos.
* **Productividad y Rendimiento:** Gestiona descansos obligatorios para prevenir el agotamiento y facilita la creación de equipos basados en competencias específicas.
* **Experiencia del Empleado (Self-Service):** Interfaz intuitiva para dispositivos móviles (**iOS y Android**) que permite a los colaboradores gestionar su disponibilidad y preferencias de turnos.

#### **Resumen de Valor**

| Enfoque | Objetivo Principal |
| :--- | :--- |
| **Financiero** | Control de presupuestos y reducción de sobrecostos laborales. |
| **Legal** | Automatización del cumplimiento de normativas vigentes. |
| **Humano** | Autogestión y bienestar del colaborador mediante movilidad. |

---
<https://www.seidor.com/es-pe/kronos>
<br></br>

### 2.1.2. Estrategias y tácticas frente a competidores.

### **Kisi (Control de Acceso en la Nube)** 
Es una solución global de gestión de accesos de nivel empresarial que centraliza el control de múltiples instalaciones en una única interfaz basada en la nube. Se especializa en modernizar infraestructuras existentes sin necesidad de reemplazarlas por completo.
<https://www.getkisi.com/enterprise>

##### **Características Principales**
* **Gestión de Identidad Avanzada:** Permite asignar privilegios detallados por usuario e integra sistemas de autenticación **SSO** y protocolos **SCIM** para sincronizar la base de datos de empleados automáticamente.
* **Seguridad y Auditoría:** Facilita el cumplimiento de normativas de seguridad física mediante la obtención de datos vía **API** y la generación de informes automáticos personalizados.
* **Seguridad Multicapa:** Ofrece opciones de autenticación de dos factores (**2FA**) y **WebAuthn** para elevar los estándares de protección.
* **Implementación Híbrida:** Su gran diferencial es la capacidad de conectarse a cerraduras y lectores ya instalados, lo que reduce los costos de implementación hasta en un **65%**.

##### **Estructura de Planes**

| Plan | Descripción / Enfoque | Ideal para |
| :--- | :--- | :--- |
| **Standard** | Control básico en la nube. | Oficinas pequeñas. |
| **CRM** | Integración con sistemas de gestión de clientes. | Negocios con membresías. |
| **Enterprise** | Auditorías estrictas e integraciones de IT avanzadas. | Grandes corporaciones. |

---
<https://pages.getkisi.com/hubfs/kisi-pricing-overview.pdf>
<br></br>

### **Acceso Total Perú (Soluciones Integrales de Automatización)**
**Perfil de la Empresa:** Empresa peruana en fase de expansión con más de 5 años de experiencia en el sector de seguridad inteligente. Su competitividad radica en la flexibilidad de hardware y una sólida trayectoria con instituciones públicas y privadas de alto perfil (MININTER, MINCETUR, UNI, entre otros).

##### **Líneas de Servicio y Planes**
* **Control de Acceso para Puertas:** Sistema versátil con soporte para múltiples métodos de validación: códigos, tarjetas, huellas biométricas, reconocimiento facial y **códigos QR**.
* **Gestión de Asistencia Biométrica:** Solución especializada para **Recursos Humanos** que permite el control detallado de asistencias, faltas y horas extras con gestión local o centralizada.
* **Control de Acceso Vehicular:** Automatización de entradas y salidas de vehículos enfocada en la eficiencia operativa y reducción de costos de personal.
* **Control Peatonal Centralizado:** Implementación de barreras físicas (**torniquetes o molinetes**) gestionadas por un software integrado e intuitivo para flujos masivos.

##### **Valor Agregado**

| Beneficio | Descripción |
| :--- | :--- |
| **Asesoría Personalizada** | Acompañamiento técnico previo para determinar la viabilidad según la infraestructura. |
| **Experiencia Local** | Conocimiento profundo del mercado peruano y cumplimiento de estándares para entidades estatales. |

---
<https://accesototalperu.com/control-de-acceso-puerta/>
<br></br>

### **Kronos por SEIDOR (Gestión de Fuerza Laboral y Tiempo)**
**Descripción General:** Solución de alto nivel distribuida por **SEIDOR**, diseñada para el control integral de la jornada laboral y la optimización de la productividad. Su enfoque principal es el cumplimiento normativo y la eficiencia operativa en empresas con grandes planillas y turnos complejos.

#### **Pilares Estratégicos**
* **Optimización de Costos Operativos:** Alinea el personal con la demanda del negocio. Controla el pago de **horas extras** y proyecta el gasto de horas-hombre en tiempo real mediante alertas automáticas.
* **Mitigación de Riesgos y Cumplimiento:** Automatiza la generación de horarios asegurando el cumplimiento de la **legislación laboral** y acuerdos sindicales. Valida que el personal cuente con certificaciones vigentes antes de asignar turnos.
* **Productividad y Rendimiento:** Gestiona descansos obligatorios para prevenir el agotamiento y facilita la creación de equipos basados en competencias específicas.
* **Experiencia del Empleado (Self-Service):** Interfaz intuitiva para dispositivos móviles (**iOS y Android**) que permite a los colaboradores gestionar su disponibilidad y preferencias de turnos.

#### **Resumen de Valor**

| Enfoque | Objetivo Principal |
| :--- | :--- |
| **Financiero** | Control de presupuestos y reducción de sobrecostos laborales. |
| **Legal** | Automatización del cumplimiento de normativas vigentes. |
| **Humano** | Autogestión y bienestar del colaborador mediante movilidad. |

---
<https://www.seidor.com/es-pe/kronos>
<br></br>

## 2.2 Entrevistas

### 2.2.1 Diseño de entrevistas

Para validar la propuesta de valor de **SmartLock**, se diseñaron entrevistas dirigidas a dos segmentos clave: **empresarios (dueños o administradores de negocios)** y **organizadores de eventos**, quienes enfrentan problemáticas relacionadas con el control de accesos y la seguridad en sus espacios.

El objetivo de estas entrevistas es comprender sus necesidades, problemas actuales, comportamientos y nivel de interés en una solución digital de control de accesos.

---

#### Segmento 1: Empresarios (dueños o administradores)

> **Objetivo:** Entender cómo gestionan actualmente el acceso a sus instalaciones, identificar problemas de seguridad y evaluar su disposición hacia soluciones digitales.

**Cuestionario de validación:**

1.  ¿Cómo gestionas actualmente el acceso de personas a tu negocio o instalaciones?
2.  ¿Qué tipo de problemas has tenido relacionados con el control de accesos?
3.  ¿Utilizas algún sistema digital o todo es manual? ¿Por qué?
4.  ¿Qué tan importante es para ti saber quién entra y sale en tiempo real?
5.  ¿Has tenido alguna situación de acceso no autorizado? ¿Cómo la manejaste?
6.  ¿Qué tan complicado es actualmente revocar el acceso a exempleados o terceros?
7.  ¿Qué herramientas utilizas para llevar un registro de accesos?
8.  ¿Cuánto tiempo inviertes en gestionar o supervisar estos accesos?
9.  ¿Qué características considerarías esenciales en un sistema de control de accesos?
10. ¿Estarías dispuesto a pagar por una solución que automatice este proceso? ¿Por qué?
11. ¿Qué nivel de confianza te generaría un sistema basado en la nube?
12. ¿Qué tan importante es para ti recibir alertas automáticas ante accesos sospechosos?
13. ¿Qué tan fácil debería ser implementar una solución como esta en tu negocio?
14. ¿Prefieres una solución sin hardware inicial (solo software)? ¿Por qué?
15. ¿Qué te haría decidirte por usar una plataforma como SmartLock?

---

#### Segmento 2: Organizadores de eventos

> **Objetivo:** Explorar cómo gestionan accesos en eventos, identificar dificultades operativas y validar oportunidades de mejora mediante tecnología.

**Cuestionario de validación:**

1.  ¿Cómo gestionas el ingreso de personas en los eventos que organizas?
2.  ¿Qué problemas has enfrentado al controlar accesos en eventos?
3.  ¿Cómo verificas la identidad o autorización de los asistentes?
4.  ¿Qué tan frecuente es que ocurran errores o accesos no autorizados?
5.  ¿Utilizas herramientas digitales para el control de ingreso? ¿Cuáles?
6.  ¿Qué tan importante es para ti tener un registro de asistencia en tiempo real?
7.  ¿Cómo manejas cambios de último momento en listas de invitados?
8.  ¿Qué tan complicado es coordinar el acceso con tu equipo de trabajo?
9.  ¿Has tenido problemas con sobreaforo o control de capacidad?
10. ¿Qué funcionalidades te gustaría tener en un sistema de control de accesos para eventos?
11. ¿Qué tan útil sería recibir alertas en tiempo real durante un evento?
12. ¿Estarías dispuesto a usar una plataforma web para gestionar accesos? ¿Por qué?
13. ¿Qué tan importante es la rapidez en el proceso de ingreso de asistentes?
14. ¿Qué te preocupa más: seguridad, rapidez o experiencia del usuario?
15. ¿Qué mejoras implementarías en tu proceso actual de control de accesos?

### 2.2.2 Registro de entrevistas

En esta sección se consolidan las entrevistas realizadas para la validación de la propuesta de valor. Cada sesión ha sido documentada para asegurar la trazabilidad de los hallazgos.

| Nombre del Entrevistado | Segmento | Enlace de la Entrevista (Drive) |
| :--- | :--- | :--- |
| Almendra Lucía Lavi Cuyubamba | Organizador de eventos | [Enlace al drive](https://drive.google.com/drive/folders/1Uhej5HwTiy1H02ks4PsJ1ypoxCMtlsuX?usp=sharing) |
| Evelyn Jannet Caldas Párraga | Organizador de Eventos | [Enlace al video](https://drive.google.com/drive/folders/1JFUE4UwyJyrbLREk2UrAOmn6ZuhBJyHT?usp=sharing) |
| Josue Nolasco | Organizador de eventos | [Enlace al video](https://drive.google.com/drive/folders/1Z8a_31JU139vRjelw6E6odRUEEG1zb4N?usp=sharing) |
| Anthony Nolasco | Empresario | [Enlace al video](https://drive.google.com/drive/folders/1BYn2a5jxz758K4LYA9w57gxhZQiKlB_P?usp=sharing) |
| Monica Moreno Olivera | Empresario | [Enlace al video](https://drive.google.com/drive/folders/1xa4zk88iqrlRpYc5PhleA7pgUyJ_iNaL?usp=sharing) |
| Hugo Ricardo Rojas | Empresario | [Enlace al video](https://drive.google.com/drive/folders/1wupFFeJ_Gso7lkt-E98uMOC2pvaAPjVk?usp=sharing) |

### 2.2.3 Análisis de entrevistas

A continuación, se presenta un análisis detallado de cada una de las sesiones de validación. En este apartado se describen los comportamientos detectados, los puntos de dolor específicos y la recepción de la propuesta de valor de SmartLock por parte de cada entrevistado.

#### Segmento: Organizadores de Eventos

**1. Almendra Lucía Lavi Cuyubamba**
de 21 años, es estudiante de la carrera de Marketing y organizadora de eventos coorporativos en la empresa llamada Okawa. Almendra Suele organizar sus eventos llevando un conteo de registros en formularios tipo google forms, donde las personas que asistirán al evento se registran. Sin embargo no tiene una manera de asegurarse que la persona registrada es alguien que tiene permiso de ingreso a las oficinas coorporativas. También tiene el problema de que muchas personas se aglomeran cerca a la hora de inicio de la conferencia provocando cierto desorden. Le gustaría que se activen servicios de IA una vez las personas ingresen al area. Le gustaría que mejore la experiencia de usuario. Le parece innovadora la idea de SmartLock y estaría dispuesta a usarlo si los beneficios en seguridad y ahorro de tiempo supera el precio del software. Prefeririá que tenganmos tanto app web como app movil. Lo más interesante de todo para ella es ver el aforo en tiempo real

**2. Evelyn Jannet Caldas Párraga**
tiene 48 años, graduada como administradora de empresas es secretaria y organizadora de eventos familiares en el colegio Norteamericano Abraham Lincoln. Evelyn gestiona el acceso a eventos institucionales dirigidos exclusivamente a socios y sus familias, utilizando actualmente plataformas como Joinnus para el registro digital y la venta de tickets. Aunque cuenta con procesos definidos, identifica un problema importante en la logística con proveedores: los cambios de último minuto en el personal externo generan demoras operativas, ya que debe asignar personal específicamente para verificaciones manuales. Para la seguridad interna de la empresa, recalca que el control es vital para proteger documentación sensible y activos contables. Evelyn muestra una clara preferencia por una solución basada 100% en software y la nube (SaaS), rechazando la implementación de hardware o servidores físicos por los costos de mantenimiento y espacio que implican. Lo que más le atrae de SmartLock es la capacidad de recibir alertas automáticas de acceso denegado y la generación de reportes estadísticos e indicadores de asistencia, lo cual considera clave para reducir horas-hombre y mejorar la eficiencia en la toma de decisiones.

**3. Josue Nolasco**
[Escribe aquí el párrafo amplio]

---

#### Segmento: Empresarios (Dueños/Administradores)

**4. Anthony Nolasco**
[Escribe aquí el párrafo amplio]

**5. Monica Moreno Olivera**
[Escribe aquí el párrafo amplio]

**6. Hugo Ricardo Rojas Párraga**
tiene 35, es ingeniero ambiental y gerente de su empresa llamada Gestam Consulting donde se realizan gestiones ambientales a empresas que contraten sus servicios. Hugo ha experimentado problemas con el manejo del acceso a sus oficinas, ya que todo el control lo hace en hojas físicas a mano lo que provoca cierto retraso. Ha tenido malas experiencias donde exempleados ingresan a las instalaciones como lo hacían antes y no desea que eso vuelva a ocurrir. También le gustaría implementar smartlock pagando una membresía económica pero sin adquirir ningún tipo de hardware físico más que los dispositivos móviles. Hugo considera que sería sencillo implementar SmartLock en sus oficinas. Hugo también considera que lo más importante para él son los reportes de asistencia periodicos.

---

#### Síntesis de hallazgos (Insights principales)
* **Insight 1:** [Resumen de una verdad descubierta].
* **Insight 2:** [Resumen de otra verdad].

## 2.3 Needfinding

### 2.3. User Personas

En esta sección se presentan las fichas de **User Persona** desarrolladas para los dos segmentos clave de **SmartLock**. La creación de estos arquetipos no es arbitraria; surge directamente del análisis de las entrevistas realizadas y del estudio de la competencia (Kisi, Acceso Total y Kronos). 

De las entrevistas, identificamos que la principal fricción es la **dependencia de registros manuales y hardware costoso**, lo que nos llevó a priorizar la agilidad y la movilidad en nuestros perfiles. Del análisis competitivo, detectamos un vacío en soluciones **"Asset-Light"** para PYMES y eventos, lo que define las metas de nuestros personajes: eficiencia sin inversión pesada en infraestructura.

Para la elaboración de estos artefactos, se utilizó la herramienta **UXPressia**, asegurando que cada ficha incluya dimensiones demográficas, psicográficas, metas, frustraciones y el entorno tecnológico del usuario.

---

#### 2.3.1. Segmento 1: Gerentes de Operaciones y TI

##### **Carlos Ortega - "El Protector Eficiente"**

Carlos representa nuestro segmento B2B corporativo. Es el tomador de decisiones que busca transformar la seguridad de su edificio en un activo estratégico basado en datos y no solo en llaves físicas.

![User Persona - Carlos Ortega](/Resources/Chapter2/docs/Carlos%20Ortega.png)

**Resumen del Perfil:**
* **Relación con el problema:** Sufre por la falta de trazabilidad en los accesos de su edificio de oficinas. Su mayor temor es una brecha de seguridad que no pueda auditar.
* **Características Clave:** * **Metas:** Centralizar el control de múltiples sedes y automatizar reportes de asistencia para RRHH.
    * **Frustraciones:** El costo de reposición de tarjetas/llaves y la lentitud de los procesos manuales.
    * **Tecnología:** Usuario avanzado de herramientas SaaS y monitoreo móvil constante.

---

#### 2.3.2. Segmento 2: Organizadores de Eventos y Espacios de Alto Tráfico

##### **Valeria Rios - "La Productora Perfeccionista"**

Valeria representa el segmento dinámico de SmartLock. Su necesidad no es la permanencia, sino la velocidad y la seguridad temporal masiva durante picos de tráfico.

![User Persona - Valeria Rios](/Resources/Chapter2/docs/Valeria%20Rios.png)

**Resumen del Perfil:**
* **Relación con el problema:** El caos en el ingreso es su mayor enemigo. Necesita un sistema que sea fácil de desplegar (sin hardware pesado) y que garantice que nadie use entradas falsificadas.
* **Características Clave:**
    * **Metas:** Fluidez total en el ingreso masivo y control de aforo en tiempo real por seguridad.
    * **Frustraciones:** Listas de invitados desactualizadas y el fraude con capturas de pantalla de códigos QR estáticos.
    * **Tecnología:** Mobile-first extremo; depende de su smartphone y la nube para coordinar a su staff en terreno.


### 2.3.2. User Task Matrix.
En esta sección se presenta el **User Task Matrix**, una herramienta que permite mapear las actividades críticas que nuestros arquetipos realizan para alcanzar sus objetivos de seguridad y gestión. Este artefacto es el resultado directo de la síntesis entre las entrevistas a profundidad y el análisis de la competencia, permitiéndonos identificar qué procesos son rutinarios y cuáles son vitales para el éxito de la operación.

Para este análisis, consideramos a nuestros dos segmentos objetivo representados por:
* **Carlos Ortega:** Gerente de Operaciones (Segmento Corporativo/Oficinas).
* **Valeria Rios:** Organizadora de Eventos (Segmento de Espacios de Alto Tráfico).

A continuación, se detallan las tareas identificadas, evaluando su **Frecuencia (F)** y su **Importancia (I)** en una escala de Bajo, Medio y Alto.

| Tareas (Tasks) | Carlos: Frecuencia | Carlos: Importancia | Valeria: Frecuencia | Valeria: Importancia |
| :--- | :---: | :---: | :---: | :---: |
| Registro de entrada y salida del personal/asistentes | Alta | Alta | Alta | Alta |
| Verificación de identidad en puntos de control | Alta | Alta | Alta | Alta |
| Gestión y entrega de credenciales físicas (llaves, carnets) | Media | Media | Baja | Media |
| Supervisión de la capacidad máxima de los recintos (aforo) | Baja | Media | Alta | Alta |
| Gestión de permisos para visitas o contratistas externos | Media | Alta | Alta | Alta |
| Elaboración de informes de permanencia y puntualidad | Alta | Alta | Baja | Media |
| Eliminación de credenciales de personal que ya no labora | Media | Alta | Baja | Media |
| Respuesta ante intentos de ingreso no autorizados | Baja | Alta | Media | Alta |

### **Explicación del Cuadro**

Al analizar la matriz, se observan coincidencias estratégicas y diferencias operativas marcadas por la naturaleza de cada segmento:

* **Tareas Críticas (Coincidencias):** El **Registro de entrada/salida** y la **Verificación de identidad** son las tareas con mayor frecuencia e importancia para ambos. Esto valida que el núcleo de *SmartLock* debe ser la rapidez y la seguridad en estos puntos de fricción.
* **Diferencias en Frecuencia:** Para Carlos, la **Elaboración de informes** es una tarea de alta frecuencia debido a la necesidad de control administrativo constante (asistencia), mientras que para Valeria es una tarea de baja frecuencia que solo ocurre al cierre del evento. Por otro lado, la **Supervisión de aforo** es crítica y frecuente para Valeria por razones de seguridad civil, mientras que para Carlos es una tarea secundaria.
* **Puntos de Dolor Identificados:** La **Eliminación de credenciales** tiene una importancia Alta para Carlos (evitar que un exempleado ingrese), pero su frecuencia es Media. En el caso de Valeria, la **Gestión de permisos temporales** es constante debido a la naturaleza volátil del staff de eventos, lo que representa una carga operativa mayor que la de una oficina tradicional.

### 2.3.3. User Journey Mapping

En esta sección se presentan los **User Journey Maps (As-Is)** correspondientes a los dos arquetipos de usuarios principales definidos previamente: Carlos Ortega (Gerente de Operaciones) y Valeria Rios (Organizadora de Eventos). 

El objetivo de estos diagramas es ilustrar el *end-to-end journey* de la situación actual que enfrentan ambos perfiles al intentar gestionar la seguridad y el control de accesos **sin contar con una solución tecnológica centralizada como SmartLock**. Se evidencia el proceso tradicional, desde el descubrimiento de la necesidad operativa, pasando por la gestión manual mediante el uso de llaves físicas o listas impresas, hasta las tareas de auditoría post-ingreso. 

A través de estos mapas, se identifican claramente los puntos de fricción (pain points), las frustraciones y las caídas en la experiencia del usuario, justificando así la necesidad de desarrollar nuestra propuesta de valor digital. Cada mapa está directamente vinculado a su ficha de *User Persona* desarrollada en la plataforma UXPressia.

#### A. User Journey Map: Carlos Ortega (Segmento Corporativo)
Este mapa detalla la experiencia diaria de Carlos, quien actualmente depende de un sistema obsoleto basado en llaves físicas, registros manuales en cuadernos de portería y reportes poco fiables. Se ilustra la frustración frente a la pérdida de llaves y la falta de visibilidad en tiempo real sobre el flujo de sus empleados.

![Customer Journey Map - Carlos Ortega](/Resources/Chapter2/docs/Customer%20Carlos.png)

#### B. User Journey Map: Valeria Rios (Segmento de Eventos)
Este mapa ilustra el proceso acelerado y estresante de Valeria durante la organización y ejecución de un evento. Se muestra su recorrido "As-Is", donde la gestión de invitados se realiza mediante listas de Excel impresas, generando lentitud en la validación de identidades, largas colas en la puerta y vulnerabilidad ante falsificaciones.

![Customer Journey Map - Valeria Rios](/Resources/Chapter2/docs/Customer%20Valeria.png)

### 2.3.4. Empathy Mapping.

En esta sección, el equipo resume el proceso de elaboración y presenta las capturas de los Empathy Maps realizados en la plataforma UXPressia para cada uno de nuestros User Personas. 

El proceso de elaboración inició con una fase de preparación estratégica, colocando al centro a nuestro User Persona correspondiente. A continuación, procedimos a colocar en cada sección de la herramienta las observaciones debatidas por los miembros del equipo, buscando responder de forma analítica a las siguientes preguntas clave: ¿Con quién estamos empatizando?, ¿Qué necesita hacer?, ¿Qué está diciendo?, ¿Qué está viendo?, ¿Qué está haciendo?, ¿Qué está escuchando? y ¿Cómo se siente y qué piensa? 

Finalmente, logramos identificar los **Pains** (frustraciones y miedos) y **Gains** (beneficios y alegrías) de cada perfil en base a las preguntas fundamentales del modelo: ¿Qué le preocupa?, ¿Qué puede ayudar a resolver sus problemas?, y sobre todo, ¿Qué puede convencerlo de que SmartLock es la alternativa correcta en el mercado?

#### A. Empathy Map: Carlos Ortega (Segmento Corporativo B2B)
El siguiente mapa de empatía ilustra el entorno corporativo de Carlos, resaltando su constante presión por mantener los costos operativos bajos y su frustración ante la pérdida recurrente de llaves físicas o tarjetas de acceso en sus instalaciones.

![Empathy Map - Carlos Ortega](/Resources/Chapter2/docs/Carlos%20Empathy%20map.png)

#### B. Empathy Map: Valeria Rios (Segmento de Eventos)
En este mapa empatizamos con el entorno de alta presión de Valeria. Se destacan sus preocupaciones principales relacionadas con las largas colas en los eventos, la vulnerabilidad ante entradas falsificadas y su necesidad urgente de una solución ágil que no requiera instalación de hardware.

![Empathy Map - Valeria Rios](/Resources/Chapter2/docs/Valeria%20Empathy%20map.png)
### 2.3.5. As-is Scenario Mapping.

En esta sección, se desarrollan los **As-is Scenario Maps** para nuestros dos arquetipos de usuario: Carlos Ortega y Valeria Rios. A diferencia del Journey Map, que evalúa el ciclo de vida completo del cliente, esta herramienta nos permite desglosar paso a paso las acciones, pensamientos y emociones de los usuarios frente a un **escenario crítico y específico** dentro de su contexto operativo actual (antes de la implementación de SmartLock).

El mapeo de estos escenarios detalla las fases cronológicas de la situación, lo que el usuario "hace", "piensa" y "siente", permitiendo a nuestro equipo identificar las deficiencias técnicas, los altos costos de resolución y los cuellos de botella que justifican el desarrollo de nuestra plataforma digital.

#### A. As-is Scenario Map: Carlos Ortega (Segmento Corporativo)
**Escenario evaluado:** Gestión de un incidente de seguridad por pérdida de llave o tarjeta maestra.
En este mapa se ilustra el proceso tradicional y reactivo que debe seguir Carlos cuando un empleado reporta la pérdida de su credencial de acceso o cuando un ex-empleado no la devuelve. Se evidencia la ineficiencia de depender de un cerrajero, el alto costo económico del reemplazo de cerraduras físicas y el estrés generado por el tiempo en que las instalaciones quedan vulnerables.

![As-is Scenario Map - Carlos Ortega](/Resources/Chapter2/docs/Carlos-As-is-Scenario.png)

#### B. As-is Scenario Map: Valeria Rios (Segmento de Eventos)
**Escenario evaluado:** Control de acceso y validación de aforo durante la "hora pico" de un evento masivo.
Este escenario detalla el momento más crítico para Valeria: la apertura de puertas de un evento utilizando listas de Excel impresas y validación manual. Se destacan las acciones de su personal de seguridad (staff), la frustración ante la lentitud del proceso, la presión por las largas colas de asistentes y la imposibilidad de tener un conteo real del aforo en tiempo real para reportar a Defensa Civil.

![As-is Scenario Map - Valeria Rios](../docs/Valeria-As-is-Scenario.png)
## 2.4. Big Picture Event Storming

En esta sección, el equipo introduce y resume el proceso colaborativo realizado para entender el dominio del negocio de **SmartLock**. Durante la sesión, nos enfocamos en identificar los eventos significativos, procesos clave y las relaciones entre ellos, permitiéndonos mapear el flujo completo desde que un usuario solicita un acceso hasta que la cerradura se activa mediante el código QR dinámico.

Esta primera aproximación visual de alto nivel nos permitió explorar el landscape del negocio, exponiendo potenciales problemas de sincronización y validación, así como oportunidades para optimizar la experiencia del usuario final al eliminar la dependencia de hardware físico tradicional.

![Big Picture Event Storming](/Resources/Chapter2/eventStormin/bigpicture.jpeg)

**Explicación de las etapas:**
* **Identificación de Eventos de Dominio:** Plasmamos en color naranja todos los sucesos relevantes (ej. QR generado, Acceso validado).
* **Ordenamiento Cronológico:** Organizamos los eventos en una línea de tiempo para asegurar la coherencia del proceso.
* **Identificación de Hotspots:** Marcamos puntos críticos o dudas técnicas que requieren mayor análisis.
* **Definición de Actores y Sistemas:** Vinculamos los eventos con los usuarios (clientes/visitantes) y sistemas externos (servicios de nube y dispositivos IoT).

## 2.5. Ubiquitous Language
## Authentication context

- Subscription: Platform tenant subscription
- System User: Admin/Operator/Auditor who accesses the web platform
- Authentication: Verifying user identity (login + 2FA)
- Role: Permission level (Super Admin, Admin, Operator, Auditor)
- 2FA: Two-factor authentication
- Quota: Usage limits (users, subscription limits)
- Billing Cycle: Recurring payment period
- Quota Warning: Alert when reaching usage limits
- User Lock: Account lockout after failed attempts

---

## Organization context

- Location: Physical site/office where doors are installed
- Door: Physical entry point with access control
- Access Mode: How door grants access (card, biometric, PIN, etc.)
- Door Status: Current state of door (open, closed, locked)
- Maintenance: Updates/repairs to doors

---

## Organization context

- Access User: Person who passes through physical doors
- Access Policy: Set of rules defining who can access
- Schedule: Time windows for access (workdays, hours)
- Holiday Schedule: Special dates with different access rules
- Policy Assignment: Linking policy to doors/users
- Access Attempt: Any attempt to enter through a door
- Access Grant: Successful access
- Access Denial: Failed access attempt

---

## Security context

- Security Alert: Notification of suspicious/unsafe activity
- Access Denial Reason: Why access was denied (invalid credentials, out of schedule, policy violation)
- Repeated Failed Attempts: Multiple failed access attempts
- Unauthorized Access: Access by unauthorized person
- Suspicious Behavior: Activity that violates normal patterns
- Emergency Override: Bypass all security to unlock doors
- Alert Acknowledgment: Operator confirms alert
- Alert Resolution: Alert issue resolved

---

## Subscription context

- Subscription Plan: Paid tier (Principiante, Eventos, Corporativo)
- Subscription Upgrade/Downgrade: Plan level changes
- Payment Failure: Failed billing transaction
- Billing Renewal: Automatic recurring payment
- History Archive: Storing old access logs
- Deactivation: Disabling user/location access
