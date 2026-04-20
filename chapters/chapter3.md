# Capítulo III: Requirements Specification

## 3.1. User Stories.

---

## Historias de Usuario Funcionales (30)

| ID | Título | Descripción | Criterios de Aceptación (Gherkin) | Relacionado con |
| :--- | :--- | :--- | :--- | :--- |
| **HU-01** | Inicio de sesión estándar | Acceso al panel administrativo. | **Dado** que el administrador está en el login, **Cuando** ingresa correo y clave correctos, **Entonces** accede al panel de control. | **EPIC-01** |
| **HU-02** | Autenticación 2FA | Verificación de identidad reforzada. | **Dado** que el personal ingresó clave válida, **Cuando** el sistema procesa el primer paso, **Entonces** solicita código 2FA y valida que no haya expirado. | **EPIC-01** |
| **HU-03** | Creación de usuarios | Registro de empleados/miembros. | **Dado** que el admin de RRHH está en el módulo, **Cuando** ingresa datos requeridos y correo único, **Entonces** el sistema registra al usuario. | **EPIC-02** |
| **HU-04** | Asignación de roles | Gestión de niveles de permiso. | **Dado** que se edita un usuario, **Cuando** se selecciona un rol (Staff/Limpieza), **Entonces** se asignan permisos automáticos del rol. | **EPIC-02** |
| **HU-05** | Acceso días laborales | Restricción por calendario. | **Dado** que el usuario tiene acceso L-V, **Cuando** intenta acceder un sábado, **Entonces** el sistema deniega y registra el evento. | **EPIC-03** |
| **HU-06** | Acceso franjas horarias | Restricción por horas. | **Dado** que el acceso es de 9AM a 6PM, **Cuando** intenta acceder 6:05PM, **Entonces** deniega la entrada y genera registro fallido. | **EPIC-03** |
| **HU-07** | Accesos temporales | Permisos con caducidad. | **Dado** que el permiso vence a las 5:00PM, **Cuando** el reloj marca las 5:01PM, **Entonces** el permiso se revoca automáticamente. | **EPIC-03** |
| **HU-08** | Dashboard Real-Time | Visualización de eventos. | **Dado** que el dashboard está abierto, **Cuando** ocurre un evento en cualquier puerta, **Entonces** aparece en la lista sin recargar la página. | **EPIC-04** |
| **HU-09** | Simulación exitosa | Prueba de flujo sin hardware. | **Dado** que se usa la web sin cerraduras, **Cuando** se simula acceso en puerta permitida, **Entonces** registra evento exitoso en dashboard. | **EPIC-05** |
| **HU-10** | Simulación denegada | Prueba de reglas de negocio. | **Dado** que se usa el simulador, **Cuando** se simula acceso en horario no permitido, **Entonces** genera registro rojo y dispara alertas. | **EPIC-05** |
| **HU-11** | Alerta intentos fallidos | Detección de intrusos. | **Dado** que el sistema está activo, **Cuando** hay >3 fallos en 5 min, **Entonces** genera alerta visual de seguridad. | **EPIC-04** |
| **HU-12** | Alerta fuera de horario | Notificación preventiva. | **Dado** que el monitoreo corre, **Cuando** hay intento de apertura fuera de franja, **Entonces** genera notificación destacada en panel. | **EPIC-04** |
| **HU-13** | Historial detallado | Auditoría de movimientos. | **Dado** que se ingresa a "Historial", **Cuando** carga la vista, **Entonces** muestra lista paginada con usuario, fecha, hora, puerta y estado. | **EPIC-06** |
| **HU-14** | Filtros de historial | Búsqueda avanzada de eventos. | **Dado** que hay miles de registros, **Cuando** se filtra por estado y fecha, **Entonces** la tabla muestra solo los criterios coincidentes. | **EPIC-06** |
| **HU-15** | Límites Plan Básico | Bloqueo por suscripción. | **Dado** que se alcanzó el límite de usuarios, **Cuando** se intenta crear uno nuevo, **Entonces** muestra modal para mejorar al Plan Profesional. | **EPIC-07** |
| **HU-16** | Upgrade Profesional | Escalabilidad de cuenta. | **Dado** que se completa el pago del Plan Profesional, **Cuando** se confirma, **Entonces** elimina límites y desbloquea control avanzado. | **EPIC-07** |
| **HU-17** | Gestión multi-sede | Centralización operativa. | **Dado** que se tiene Plan Empresarial, **Cuando** se accede al panel, **Entonces** permite crear y cambiar entre Sedes independientes. | **EPIC-07** |
| **HU-18** | Reportes avanzados | Análisis de flujo. | **Dado** que se tiene Plan Empresarial, **Cuando** se pide reporte de horas pico, **Entonces** exporta PDF/Excel con gráficas. | **EPIC-06** |
| **HU-19** | Desactivación rápida | Revocación instantánea. | **Dado** que se visualiza lista de empleados, **Cuando** se pulsa "Desactivar", **Entonces** el acceso se revoca en tiempo real en toda la red. | **EPIC-02** |
| **HU-20** | Gestión de Puertas | CRUD de infraestructura. | **Dado** que se configura el espacio, **Cuando** se entra a "Puertas", **Entonces** permite crear, editar y eliminar puntos de acceso. | **EPIC-03** |
| **HU-21** | Acceso por puerta | Permisos granulares. | **Dado** que se edita el rol "Limpieza", **Cuando** se marcan puertas específicas, **Entonces** deniega acceso en el resto de puertas. | **EPIC-03** |
| **HU-22** | Alerta uso indebido | Prevención de espionaje. | **Dado** que hay zonas restringidas, **Cuando** hay intento sin autorización, **Entonces** etiqueta como "Uso indebido" y emite alerta. | **EPIC-04** |
| **HU-23** | Reset de contraseña | Autogestión de cuenta. | **Dado** que el usuario olvidó su clave, **Cuando** la solicita, **Entonces** recibe enlace tokenizado válido por 15 minutos. | **EPIC-01** |
| **HU-24** | Exportación de datos | Descarga de reportes. | **Dado** que se aplicaron filtros en historial, **Cuando** se pulsa "Exportar", **Entonces** descarga CSV con los registros filtrados. | **EPIC-06** |
| **HU-25** | Cierre de alertas | Gestión de incidencias. | **Dado** que hay alerta activa, **Cuando** se pulsa "Resolver", **Entonces** desaparece de la vista y se archiva como resuelta. | **EPIC-04** |
| **HU-26** | Cierre de sesión | Seguridad de terminal. | **Dado** que el usuario está logueado, **Cuando** pulsa "Cerrar sesión", **Entonces** destruye el token y redirige al login. | **EPIC-01** |
| **HU-27** | Invitación masiva | Onboarding eficiente. | **Dado** que se carga lista de correos, **Cuando** se envía, **Entonces** cada empleado recibe link único para crear su clave. | **EPIC-02** |
| **HU-28** | Edición de perfil | Actualización de datos. | **Dado** que el usuario está autenticado, **Cuando** edita su perfil, **Entonces** permite cambiar foto/teléfono pero bloquea cambio de rol. | **EPIC-01** |
| **HU-29** | Alerta desconexión | Monitoreo de hardware. | **Dado** que se monitorea hardware, **Cuando** una puerta pierde red, **Entonces** el ícono en dashboard cambia a "Offline" o rojo. | **EPIC-04** |
| **HU-30** | Notificación crítica | Alerta vía email. | **Dado** que hay notificaciones activas, **Cuando** ocurre emergencia (madrugada), **Entonces** envía email automático al dueño. | **EPIC-04** |

---

## Historias de Usuario No Funcionales (30)

| ID | Título | Descripción | Criterios de Aceptación (Gherkin) | Relacionado con |
| :--- | :--- | :--- | :--- | :--- |
| **HNF-01** | Latencia Dashboard | Actualización inmediata. | **Dado** que ocurre validación en puerta, **Cuando** la DB registra el evento, **Entonces** actualiza el dashboard en < 1 segundo. | **EPIC-08** |
| **HNF-02** | Rendimiento carga | Carga de plataforma. | **Dado** que se ingresa a la URL, **Cuando** el navegador pide recursos, **Entonces** la página es interactiva en un máximo de 2 segundos. | **EPIC-08** |
| **HNF-03** | Encriptación | Hashing de seguridad. | **Dado** que se crea/cambia clave, **Cuando** se guarda en DB, **Entonces** debe usarse bcrypt y nunca texto plano. | **EPIC-09** |
| **HNF-04** | Datos en tránsito | Cifrado de red. | **Dado** que la web habla con la API, **Cuando** viajan datos sensibles, **Entonces** debe usarse HTTPS con TLS 1.2+. | **EPIC-09** |
| **HNF-05** | Disponibilidad | Continuidad operativa. | **Dado** que el sistema está en producción, **Cuando** se mide el uptime mensual, **Entonces** debe ser >= 99.9%. | **EPIC-08** |
| **HNF-06** | Diseño Responsivo | Adaptabilidad móvil. | **Dado** que se usa un móvil (320px), **Cuando** accede al panel, **Entonces** la interfaz adapta elementos sin pérdida de función. | **EPIC-10** |
| **HNF-07** | Inmutabilidad logs | Integridad de auditoría. | **Dado** que un evento se escribió en DB, **Cuando** un admin intenta borrarlo, **Entonces** la API debe rechazar el UPDATE/DELETE. | **EPIC-06** |
| **HNF-08** | Escalabilidad | Capacidad de carga. | **Dado** que es hora pico (9AM), **Cuando** hay 500 peticiones simultáneas, **Entonces** el servidor responde en < 500ms sin caídas. | **EPIC-08** |
| **HNF-09** | Timeout sesión | Protección por olvido. | **Dado** que la sesión quedó abierta, **Cuando** pasan 15 min sin actividad, **Entonces** destruye sesión y redirige al login. | **EPIC-09** |
| **HNF-10** | Compatibilidad | Multi-navegador. | **Dado** que se usa Chrome/Safari/Firefox, **Cuando** se abre la plataforma, **Entonces** debe renderizar sin fallos visuales ni de consola. | **EPIC-10** |
| **HNF-11** | Tolerancia fallos | Aislamiento de errores. | **Dado** que el simulador tiene un crash, **Cuando** el usuario navega el resto, **Entonces** dashboard e historial siguen operando. | **EPIC-08** |
| **HNF-12** | Velocidad 2FA/Email | Entrega de correos. | **Dado** que se pide 2FA, **Cuando** se dispara solicitud, **Entonces** el correo llega en < 5 segundos a la bandeja del usuario. | **EPIC-08** |
| **HNF-13** | Accesibilidad | Normas WCAG. | **Dado** que se evalúan colores, **Cuando** se mide el contraste, **Entonces** debe cumplir nivel AA de WCAG 2.1. | **EPIC-10** |
| **HNF-14** | Anti-Brute Force | Bloqueo de ataques. | **Dado** que hay ataque de clave, **Cuando** hay 5 fallos en mismo correo, **Entonces** bloquea IP/Cuenta por 30 minutos. | **EPIC-09** |
| **HNF-15** | Data Isolation | Multi-tenancy real. | **Dado** que es un SaaS multi-empresa, **Cuando** un admin consulta, **Entonces** el esquema garantiza que no vea datos de otros clientes. | **EPIC-09** |
| **HNF-16** | Backups diarios | Respaldo de datos. | **Dado** que la info es crítica, **Cuando** es la ventana de mantenimiento, **Entonces** genera backup automático en nube segregada. | **EPIC-09** |
| **HNF-17** | Log de auditoría | Trazabilidad admin. | **Dado** que un admin cambia configuración, **Cuando** se ejecuta, **Entonces** registra quién, cuándo y qué cambió en log oculto. | **EPIC-06** |
| **HNF-18** | Mensajes de error | UX de fallos. | **Dado** que hay fallo de base de datos, **Cuando** la API falla, **Entonces** el frontend muestra mensaje amigable sin detalles técnicos. | **EPIC-10** |
| **HNF-19** | Rate Limiting | Protección de API. | **Dado** que un bot ataca la API, **Cuando** hay >100 req/min desde una IP, **Entonces** el Gateway bloquea con error 429. | **EPIC-09** |
| **HNF-20** | Velocidad Export | Procesamiento masivo. | **Dado** que se exportan 10,000 registros, **Cuando** se procesa, **Entonces** entrega el archivo en < 10 segundos. | **EPIC-08** |
| **HNF-21** | Complejidad clave | Validación de fortaleza. | **Dado** que se configura clave, **Cuando** es débil (1234), **Entonces** rechaza y exige 8 carac., número y símbolo. | **EPIC-09** |
| **HNF-22** | Soporte i18n | Internacionalización. | **Dado** que se desarrolla el código, **Cuando** se implementan textos, **Entonces** se envuelven en i18n para futuras traducciones. | **EPIC-11** |
| **HNF-23** | RTO | Recuperación desastres. | **Dado** que hay desastre total, **Cuando** se activa el DRP, **Entonces** el sistema opera en región secundaria en máximo 4 horas. | **EPIC-08** |
| **HNF-24** | Archivado datos | Cold Storage. | **Dado** que hay millones de registros, **Cuando** un log cumple 2 años, **Entonces** se mueve automáticamente a almacenamiento en frío. | **EPIC-06** |
| **HNF-25** | Consumo batería | Optimización móvil. | **Dado** que el dashboard corre 8h en tablet, **Cuando** se mide consumo, **Entonces** no debe causar drenaje excesivo ni calor. | **EPIC-08** |
| **HNF-26** | Seguridad OWASP | Sanitización de inputs. | **Dado** que hay ataque XSS/SQLi, **Cuando** se envían datos, **Entonces** el backend sanitiza y usa consultas parametrizadas. | **EPIC-09** |
| **HNF-27** | Sincronía NTP | Precisión temporal. | **Dado** que el log tiene valor legal, **Cuando** se registra evento, **Entonces** el servidor usa NTP para sincronía global exacta. | **EPIC-09** |
| **HNF-28** | Regla 3 clics | Arquitectura intuitiva. | **Dado** que se busca una función, **Cuando** se navega desde dashboard, **Entonces** se debe completar en máximo 3 clics. | **EPIC-10** |
| **HNF-29** | Design System | Consistencia UI. | **Dado** que hay nuevas pantallas, **Cuando** el usuario navega, **Entonces** los colores/espaciados deben ser uniformes. | **EPIC-10** |
| **HNF-30** | Health Checks | Monitoreo de salud. | **Dado** que falla un microservicio, **Cuando** el monitor consulta /health, **Entonces** detecta y notifica antes del reporte del cliente. | **EPIC-08** |

---

## Definición de Epics (Módulos Generales)

| Epic ID | Nombre de la Epic | Descripción |
| :--- | :--- | :--- |
| **EPIC-01** | **Gestión de Identidad y Cuenta** | Todo lo relacionado con autenticación, seguridad de perfil y acceso inicial al sistema. |
| **EPIC-02** | **Administración de Personal (RRHH)** | Gestión del ciclo de vida del usuario: creación, asignación de roles, desactivación e invitaciones. |
| **EPIC-03** | **Configuración de Infraestructura y Reglas** | Definición de puertas físicas y las reglas de negocio (horarios, días, accesos temporales). |
| **EPIC-04** | **Centro de Monitoreo y Alertas** | El "corazón" operativo: dashboard en tiempo real, gestión de alertas e indicadores de estado. |
| **EPIC-05** | **Entorno de Simulación (Virtual Lock)** | Módulo para clientes sin hardware que permite probar la lógica de acceso digitalmente. |
| **EPIC-06** | **Auditoría, Reportes e Integridad** | Registro histórico, exportación de datos, analítica avanzada y protección de la inmutabilidad de logs. |
| **EPIC-07** | **Ecosistema Comercial y Suscripciones** | Manejo de tiers (Básico, Pro, Enterprise), límites de cuenta y gestión multi-sede. |
| **EPIC-08** | **Rendimiento, Disponibilidad y Escalabilidad** | Calidad del sistema en términos de velocidad, estabilidad frente a carga y recuperación ante fallos. |
| **EPIC-09** | **Capa de Seguridad y Ciberdefensa** | Normas técnicas de encriptación, protocolos de red, protección contra ataques y privacidad de datos. |
| **EPIC-10** | **Experiencia de Usuario (UX/UI)** | Consistencia visual, accesibilidad, diseño responsivo y usabilidad general. |
| **EPIC-11** | **Escalabilidad Global e i18n** | Preparación técnica del software para mercados internacionales y multi-idioma. |

## 3.2. Impact Mapping

## 3.3. Product Backlog
