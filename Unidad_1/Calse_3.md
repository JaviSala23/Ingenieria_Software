# 📘 Clase 3 – Software en Sistemas Complejos

---

## 🎯 Objetivos de la clase

- Comprender qué se entiende por sistema complejo y sistema sociotécnico.
- Analizar cómo se inserta el software en estos sistemas más amplios.
- Reflexionar sobre los desafíos técnicos, humanos y organizacionales involucrados.
- Introducir el concepto de propiedades emergentes.
- Dar ejemplos reales de sistemas críticos y su impacto.

---

## 🧠 ¿Qué es un sistema complejo?

Un **sistema complejo** es una colección de componentes interdependientes que interactúan para alcanzar un objetivo. Su comportamiento **no puede predecirse solamente a partir de las partes individuales**, ya que surgen propiedades nuevas al integrarlas. Estos sistemas pueden involucrar tecnología, personas, procesos, leyes y más.

---

### 🧩 Tipos de sistemas con software

#### 1. Sistemas técnicos basados en computadora

Estos sistemas están compuestos exclusivamente por **componentes tecnológicos**, es decir, hardware (dispositivos físicos) y software (programas que controlan esos dispositivos). **No contemplan la interacción directa con usuarios humanos** como parte esencial del sistema. Funcionan de forma autónoma una vez configurados, y su comportamiento se basa en lógica predefinida sin intervención humana durante su operación habitual.

📌 *Ejemplos:*  
- Un microondas que ejecuta un ciclo de cocción programado.  
- Un videojuego que corre en una consola.  
- Un sistema de control de temperatura en un horno eléctrico.

Estos sistemas pueden ser complejos en términos técnicos, pero **su entorno está más controlado y definido** en comparación con los sistemas sociotécnicos.

---

### 🧱 Capas de un sistema sociotécnico

Los sistemas sociotécnicos no se limitan al software. Son sistemas organizacionales completos en los que el software forma solo una parte. Están estructurados en múltiples **capas interrelacionadas**, cada una con su función específica y su impacto en el funcionamiento general del sistema.

#### 🖥️ 1. Equipo (Hardware)
Incluye todos los **dispositivos físicos** necesarios para que el sistema funcione:
- Servidores, computadoras, sensores, dispositivos móviles, routers, etc.
- Proveen la base material sobre la cual se ejecuta el software.
- Pueden ser locales o distribuidos geográficamente.

#### 🧠 2. Sistema Operativo
Es el software que **controla y gestiona los recursos del hardware**:
- Asigna memoria, administra procesos, controla dispositivos de entrada/salida.
- Crea una base estable para que otros programas puedan ejecutarse correctamente.
- Ejemplos: Windows, Linux, Android, macOS.

#### 🔗 3. Middleware
Software que actúa como **puente entre el sistema operativo y las aplicaciones**:
- Facilita la comunicación entre distintos componentes del sistema.
- Gestiona redes, base de datos, servicios distribuidos, colas de mensajes.
- Ejemplo: bases de datos, APIs, servidores web, sistemas de autenticación.

#### 💻 4. Aplicaciones
Programas con lógica específica que permiten al usuario cumplir tareas concretas:
- Pueden ser interfaces gráficas, aplicaciones móviles o herramientas especializadas.
- Directamente visibles y utilizadas por el usuario.
- Ejemplos: sistemas de ventas, historia clínica electrónica, plataformas de e-learning.

#### 🔄 5. Procesos de negocio
Son los **flujos de trabajo definidos por la organización**:
- Incluyen reglas, pasos, roles y responsabilidades.
- El software debe modelar y apoyar estos procesos, no reemplazarlos sin análisis.
- Ejemplo: flujo de admisión de pacientes en un hospital, procesos de facturación.

#### 🏛️ 6. Organización
Incluye la **estructura formal** de la institución u organización:
- Normas internas, políticas, jerarquías, división de responsabilidades.
- Afecta cómo se usa el sistema, qué cambios se pueden hacer, y qué resistencias pueden surgir.
- Un software exitoso debe adaptarse a esta capa, no imponerse a la fuerza.

#### 🌍 7. Entorno social
Conjunto de **factores externos** que influyen en el sistema:
- Legislación, cultura, idioma, valores sociales, normas éticas y regulaciones gubernamentales.
- Afecta la manera en que el sistema debe ser diseñado y operado.
- Ejemplo: una app de salud debe cumplir con leyes de privacidad (como GDPR o Ley de Datos Personales en Argentina).

---

Estas capas no deben analizarse por separado: **interactúan constantemente** y cualquier cambio en una puede afectar a las demás. Por eso, el diseño y la implementación de un sistema sociotécnico requiere una **mirada sistémica e interdisciplinaria**.


---

### ⚙️ Capas de un sistema sociotécnico

Un sistema sociotécnico se compone de múltiples niveles interrelacionados que van desde el hardware físico hasta los factores sociales y organizativos que lo rodean. Estas capas trabajan en conjunto para que el sistema funcione de manera efectiva:

- **Equipo:** Dispositivos físicos (hardware) como computadoras, sensores, servidores y redes que soportan el sistema.
- **Sistema operativo:** Software base que administra los recursos del hardware y permite la ejecución de aplicaciones.
- **Middleware:** Capa intermedia que conecta componentes y servicios. Gestiona redes, bases de datos, autenticación y comunicación entre sistemas.
- **Aplicaciones:** Programas con funciones específicas que resuelven necesidades concretas de los usuarios (por ejemplo, facturación, control de stock, diagnóstico clínico).
- **Procesos de negocio:** Secuencia estructurada de tareas, reglas y flujos de trabajo que reflejan cómo opera una organización.
- **Organización:** Estructura formal e informal de la institución: normas internas, jerarquías, políticas y cultura institucional.
- **Entorno social:** Factores externos como leyes, regulaciones, costumbres, idioma, valores sociales y aspectos éticos que condicionan el diseño y uso del sistema.

Cada una de estas capas es clave para comprender el comportamiento global del sistema y su éxito o fracaso en el contexto real.

---

## 🧱 Propiedades emergentes

Las **propiedades emergentes** son características del sistema completo que **no pueden ser entendidas ni garantizadas observando únicamente sus componentes individuales**. Solo surgen cuando todos los elementos (software, hardware, procesos, personas) trabajan **en conjunto** dentro del contexto real del sistema.

Estas propiedades son críticas en sistemas sociotécnicos, especialmente en los sistemas complejos, distribuidos y de alta criticidad.

---

### 🔒 Fiabilidad (Reliability)
Capacidad del sistema para funcionar correctamente durante un periodo determinado, bajo condiciones específicas.  
Incluye:
- Ausencia de fallos.
- Estabilidad frente a uso prolongado o situaciones límite.
- Manejo de errores sin colapsar el sistema.

🧠 *Ejemplo:* Un sistema bancario que registra operaciones sin perder datos, incluso si hay cortes de red o errores del usuario.

---

### 🛡 Seguridad (Security)
Capacidad del sistema para resistir accesos no autorizados, fraudes o sabotajes.  
Incluye:
- Control de acceso y autenticación.
- Confidencialidad de datos.
- Integridad y protección contra amenazas externas.

🧠 *Ejemplo:* Un sistema de historia clínica debe proteger la privacidad de los pacientes y evitar manipulaciones de información.

---

### 🧭 Usabilidad (Usability)
Grado en el que el sistema es fácil de aprender, entender y usar correctamente.  
Incluye:
- Interfaz amigable.
- Claridad en los mensajes e instrucciones.
- Adaptación al perfil de usuario.

🧠 *Ejemplo:* Una app de turnos médicos que puede ser usada sin dificultad por adultos mayores o personas con poca experiencia digital.

---

### 🚀 Rendimiento (Performance)
Capacidad del sistema para responder de manera eficiente en términos de tiempo, velocidad y uso de recursos.  
Incluye:
- Tiempo de respuesta.
- Escalabilidad.
- Consumo de CPU, memoria y ancho de banda.

🧠 *Ejemplo:* Una plataforma de e-commerce que sigue funcionando correctamente durante eventos de alto tráfico como el Black Friday.

---

### ♻️ Capacidad de recuperación (Recoverability)
Capacidad del sistema para **recuperarse** ante fallos, errores o situaciones imprevistas.  
Incluye:
- Mecanismos de respaldo y restauración.
- Redundancia de componentes.
- Reintentos automáticos o modos de operación degradados.

🧠 *Ejemplo:* Un sistema de control industrial que continúa funcionando en “modo seguro” ante la pérdida de un sensor.

---

### 💡 Reflexión

> Estas propiedades no están “programadas” directamente como funciones, sino que **emergen de la interacción entre partes**. Son esenciales para la confianza, estabilidad y éxito de cualquier sistema complejo.

Diseñar con estas propiedades en mente requiere una mirada integral y colaborativa desde la **ingeniería de software**, **experiencia de usuario**, **infraestructura**, **seguridad** y **gestión del proyecto**.

---

## 🧪 Ejemplo 1: Sistema meteorológico

Un sistema de predicción del clima incluye:
- Estaciones con sensores.
- Programas de modelado climático.
- Bases de datos globales.
- Operadores y meteorólogos.
- Gobiernos y usuarios que toman decisiones con base en sus reportes.

👉 No es solo software: es un **sistema sociotécnico internacional**.

---

## 🧪 Ejemplo 2: Sistema crítico - Bomba de insulina

- Mide el nivel de glucosa.
- Calcula y administra automáticamente la insulina.
- Puede tener consecuencias fatales si falla.

Este tipo de sistemas:
- Son **críticos para la seguridad**.
- Requieren **alta confiabilidad**.
- Deben probarse rigurosamente.

---

## 🔍 Implicancias para la Ingeniería de Software

Diseñar software para sistemas complejos y sociotécnicos implica enfrentar una serie de desafíos que van mucho más allá de escribir buen código. A continuación se detallan algunas de las implicancias clave que la Ingeniería de Software debe considerar:

---

### 1. **Interdisciplinariedad**

El desarrollo de sistemas complejos requiere la colaboración de profesionales de múltiples áreas:  
- Ingenieros de software y sistemas.  
- Expertos en el dominio (médicos, contadores, docentes, etc.).  
- Diseñadores UX, analistas funcionales, especialistas legales o en seguridad.  

🧠 *Ejemplo:* Para crear un sistema de historia clínica digital es indispensable entender las prácticas médicas, los flujos de atención y la legislación sanitaria.

---

### 2. **Tolerancia a errores**

Dado que **ningún sistema es perfecto**, deben diseñarse con mecanismos de prevención, detección y recuperación ante fallos, tanto técnicos como humanos.  
- Validaciones de entrada.  
- Confirmaciones y deshacer acciones.  
- Logs, backups y monitoreo en tiempo real.  

🧠 *Ejemplo:* Un sistema bancario debe poder manejar desde errores de tipeo hasta caídas de red sin comprometer la integridad de los datos.

---

### 3. **Adaptabilidad**

Los entornos reales están en constante cambio:  
- Nuevas normativas legales.  
- Cambios en los procesos de negocio.  
- Avances tecnológicos.  
- Cambios en los perfiles de usuarios.

El software debe diseñarse de forma **modular y flexible** para facilitar su evolución sin requerir una reescritura completa.

🧠 *Ejemplo:* Un sistema de facturación debe adaptarse rápidamente a nuevos impuestos o cambios en la legislación tributaria.

---

### 4. **Validación holística**

No alcanza con validar que el código funcione; es necesario verificar que el **sistema completo** (incluyendo usuarios, hardware, redes y procesos) cumpla con los objetivos.  
- Pruebas de integración.  
- Simulación de uso en escenarios reales.  
- Evaluaciones de experiencia de usuario (UX).  
- Revisión con expertos del dominio.

🧠 *Ejemplo:* En un sistema de transporte público, no solo debe funcionar el software de validación de tarjetas, sino que debe integrarse correctamente con torniquetes, sensores, y horarios.

---

### 5. **Factores organizacionales**

La implantación de un sistema puede verse afectada por:  
- Resistencias al cambio.  
- Falta de capacitación.  
- Políticas internas contradictorias.  
- Rechazo por parte de usuarios clave.

La ingeniería de software debe considerar el **componente humano** y cultural del entorno organizacional, incluyendo tareas de comunicación, formación y gestión del cambio.

🧠 *Ejemplo:* Un sistema de control de asistencia puede fallar si los empleados no comprenden su uso o si la gerencia no establece normas claras sobre su implementación.

---

> En resumen, la Ingeniería de Software moderna no puede limitarse a la técnica: debe asumir un **enfoque sistémico, colaborativo y estratégico** para crear soluciones sostenibles en entornos reales.


---

## 🚨 Sistemas heredados

Los **sistemas heredados** (también llamados *legacy systems*) son sistemas sociotécnicos que han estado en funcionamiento durante muchos años, y aunque suelen estar **tecnológicamente desactualizados**, siguen siendo **esenciales para la operación diaria de una organización**.

---

### 🧱 Características principales

- **Antigüedad:** Fueron desarrollados con tecnologías, lenguajes y arquitecturas que hoy pueden estar obsoletos.
- **Críticos:** Son indispensables para el funcionamiento de procesos clave (producción, facturación, control, etc.).
- **Estabilidad:** Suelen haber sido probados durante años, lo que los hace confiables en cuanto a comportamiento.
- **Dependencia interna:** Otros sistemas, bases de datos y usuarios dependen de ellos.
- **Poca documentación:** Muchas veces el conocimiento se pierde con el tiempo y depende de pocos especialistas.

---

### 💰 Costos y desafíos

- **Reemplazarlos es caro y riesgoso**, ya que pueden estar integrados profundamente en la organización.
- Su **mantenimiento es complejo** por:
  - Escasez de programadores con conocimientos en lenguajes antiguos (como COBOL).
  - Falta de pruebas automatizadas o documentación.
  - Hardware especializado que ya no se fabrica.
- Pueden convertirse en **cuellos de botella** para la modernización digital.

---

### 🧠 Ejemplos comunes

- Sistemas de control industrial en fábricas.
- Software de gestión bancaria desarrollado en los años 80.
- Sistemas tributarios del estado con décadas de evolución.
- Software de inventario escrito en lenguajes como FoxPro o Delphi.

---

### 🔄 ¿Qué hacer con ellos?

Las organizaciones suelen optar por una de estas estrategias:

1. **Reemplazo total:** Riesgoso y costoso, pero elimina la dependencia.
2. **Reescritura parcial:** Se reimplementan componentes clave gradualmente.
3. **Encapsulamiento:** Se crea una “capa moderna” que interactúa con el sistema antiguo mediante interfaces.
4. **Emulación:** Se conservan los sistemas pero se ejecutan en entornos virtuales modernos.

---

> 📌 La Ingeniería de Software debe entender estos sistemas no solo como código viejo, sino como **infraestructura crítica** cargada de conocimiento organizacional, histórico y funcional que debe preservarse o migrarse con sumo cuidado.

---

## 📌 Conclusión

El software no vive en el vacío. Forma parte de sistemas complejos donde interactúa con personas, procesos y tecnologías. Comprender el **contexto** es tan importante como escribir buen código. La Ingeniería de Software moderna requiere una mirada amplia, crítica y multidisciplinaria.

---

## 🧠 Actividad sugerida

🔎 **Investigar y presentar** (individual o en grupo):  
> Elegí un sistema sociotécnico (banco, hospital, red de transporte, app de delivery, etc.)  
> Describí:
> - Componentes técnicos y humanos.
> - Riesgos de fallo y propiedades emergentes.
> - ¿Qué pasaría si falla el software?

---


