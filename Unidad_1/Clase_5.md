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
- Se documentan todas las necesidades del sistema.
- Implica reuniones con el cliente, usuarios y análisis de dominio.
- Se produce un documento de especificación de requisitos.

### 2. 🧠 Diseño del Sistema
- Se define la arquitectura general del sistema.
- Se decide cómo se dividirá en módulos, cómo interactúan, qué tecnologías se usarán.
- Se documenta el diseño lógico y físico.

### 3. 💻 Implementación (Codificación)
- Los desarrolladores escriben el código fuente basado en el diseño.
- Se realizan pruebas unitarias a medida que se desarrolla.

### 4. 🧪 Verificación (Pruebas)
- Se integran todos los módulos y se realizan pruebas del sistema.
- Se busca asegurar que cumple con los requisitos funcionales y no funcionales.

### 5. 🚀 Instalación o Entrega
- Se despliega el sistema en el entorno real de producción.
- Se capacita a los usuarios y se brinda documentación final.

### 6. 🔧 Mantenimiento
- Se corrigen errores descubiertos en producción.
- Se realizan mejoras o adaptaciones según nuevas necesidades del usuario o entorno.

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
