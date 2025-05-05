# 📘 Clase 5 – Modelo en Cascada

---

## 🎯 Objetivos de la clase

- Comprender el funcionamiento del Modelo en Cascada.
- Analizar sus etapas, ventajas, limitaciones y aplicación.
- Evaluar situaciones donde este modelo puede ser apropiado.
- Relacionar con casos reales y prácticos de uso.

---

## 🏗 ¿Qué es el Modelo en Cascada?

El **Modelo en Cascada** es uno de los modelos de ciclo de vida del software más antiguos y estructurados.  
Fue formalizado en 1970 por Winston Royce y propone un desarrollo **secuencial y por fases** donde cada etapa debe completarse antes de pasar a la siguiente.

El nombre "cascada" hace referencia al flujo descendente, como una caída de agua, donde el progreso **fluye de una etapa a otra** sin retrocesos importantes.

---

## 🔄 Etapas del Modelo en Cascada 

### 1. 📋 Recolección y Análisis de Requisitos

Esta es una fase **crítica**, ya que define qué debe hacer el sistema.  
Implica:

- Entrevistas, reuniones y talleres con el cliente y usuarios finales.
- Revisión de procesos existentes y análisis de documentos del dominio.
- Identificación de restricciones legales, técnicas o de negocio.

El objetivo es obtener una **descripción precisa, clara y completa** de los requisitos funcionales (lo que el sistema debe hacer) y no funcionales (rendimiento, seguridad, usabilidad, etc.).

📄 *Resultado:* Documento formal de especificación de requisitos (SRS), que sirve de base para todo el proyecto.

---

### 2. 🧠 Diseño del Sistema

Con los requisitos definidos, se procede a planificar **cómo se va a construir** el sistema.

Se divide en dos niveles:

- **Diseño de alto nivel (arquitectónico):** define la estructura general del sistema, los módulos, sus interacciones, patrones arquitectónicos, tecnologías a utilizar.
- **Diseño de bajo nivel (detallado):** describe cada módulo internamente: algoritmos, estructuras de datos, interfaz con otros módulos.

Se toman decisiones sobre bases de datos, servicios, APIs, interfaces gráficas, flujos de navegación, etc.

📄 *Resultado:* Documento de diseño, diagramas (UML, flujo de datos, entidad-relación) y especificaciones técnicas.

---

### 3. 💻 Implementación (Codificación)

Aquí los desarrolladores convierten el diseño en **código ejecutable**.

- Se programan los módulos definidos, respetando los estándares y convenciones acordadas.
- Se realizan **pruebas unitarias** para verificar el funcionamiento correcto de cada componente.
- El trabajo puede estar dividido entre distintos programadores o equipos, según los módulos.

💡 El éxito de esta etapa depende fuertemente de la calidad del análisis y el diseño previos.

---

### 4. 🧪 Verificación (Pruebas)

Una vez implementados todos los módulos, se integran y se realiza una batería de **pruebas sistemáticas**:

- **Pruebas de integración:** para asegurar que los módulos interactúan correctamente.
- **Pruebas funcionales:** para validar que se cumplen los requisitos definidos.
- **Pruebas de rendimiento, seguridad, usabilidad**, según los criterios definidos en la fase de análisis.

En esta etapa también se documentan errores encontrados, se generan informes y se corrigen defectos antes de la entrega.

📄 *Resultado:* Informe de pruebas, plan de validación, versiones listas para producción.

---

### 5. 🚀 Instalación o Entrega

Finalizadas las pruebas, el producto se **entrega al cliente** y se instala en su entorno real de uso.

- Se realiza la **configuración final**, adaptación al entorno operativo.
- Se lleva a cabo la **capacitación a los usuarios**, entrega de manuales, guías de uso y soporte inicial.
- Se formaliza el cierre del proyecto (actas, entregables, aceptación por parte del cliente).

Es fundamental que esta etapa esté bien gestionada para evitar frustraciones o errores en el uso inicial.

---

### 6. 🔧 Mantenimiento

Una vez que el sistema está en producción, comienza su ciclo de **mantenimiento**, que puede extenderse por años.

Tipos de mantenimiento:
- **Correctivo:** se corrigen errores no detectados antes.
- **Adaptativo:** se ajusta el sistema a cambios del entorno (por ejemplo, nuevo hardware o normativas).
- **Perfectivo:** se mejora el sistema con nuevas funcionalidades o mejoras de rendimiento.
- **Preventivo:** se anticipan posibles problemas futuros.

El mantenimiento suele representar **más del 60% del costo total de un sistema de software** a lo largo de su vida útil.

---

Estas etapas, aunque presentadas en secuencia, pueden solaparse ligeramente en la práctica, pero en el Modelo en Cascada clásico, cada una debe **concluir formalmente** antes de iniciar la siguiente.


---

## ✅ Ventajas del Modelo en Cascada

- Sencillo de entender y aplicar.
- Fases bien definidas y documentadas.
- Ideal para proyectos **bien acotados y con requisitos estables**.
- Permite una planificación detallada desde el inicio.
- Facilita la gestión para equipos pequeños o tradicionales.

---

## ⚠️ Desventajas y críticas

- **Rígido**: difícil adaptarse a cambios de requisitos.
- **Poca retroalimentación temprana**: el cliente ve el producto funcional al final.
- **Riesgoso** en proyectos largos o con incertidumbre.
- **Costoso** corregir errores detectados en etapas tardías.
- No fomenta la participación continua del usuario.

---

## 🧭 ¿Cuándo conviene usar este modelo?

- Proyectos con requisitos **claros, estables y bien documentados**.
- Sistemas pequeños o medianos.
- Ambientes donde se exige mucha formalidad y documentación.
- Contratos cerrados o entornos gubernamentales.

---

## 💡 Ejemplo ilustrativo

Un sistema de gestión de turnos médicos en una clínica pequeña:
- Los requisitos no cambian con frecuencia.
- El cliente ya conoce qué funcionalidades desea.
- Se puede diseñar y desarrollar de manera lineal.

---

## 🔍 Reflexión

> ¿Qué pasaría si durante las pruebas el cliente se da cuenta de que un requisito fue mal interpretado?
> En el modelo en cascada, modificar el diseño o reescribir código en etapas tardías **es costoso y complejo**.  
> Por eso, este modelo **no es recomendable en proyectos donde se espera evolución o cambio constante**.

---

## ✍️ Actividad sugerida

**Analizar un sistema real (por ejemplo, un cajero automático, un sistema de reservas o una aplicación de escritorio).**  
Reflexionar en grupo:

- ¿Podría haberse desarrollado con el modelo en cascada?
- ¿Qué riesgos implicaría usarlo?
- ¿Qué aspectos del sistema podrían complicar su implementación si se siguen las fases estrictamente?

---
