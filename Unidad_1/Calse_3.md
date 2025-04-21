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

#### 2. Sistemas sociotécnicos

Estos sistemas integran componentes técnicos (hardware y software) **junto con elementos humanos, organizativos y sociales**. No se pueden analizar ni diseñar correctamente si se ignoran los procesos, las personas que los usan o los marcos normativos en los que operan.

Incluyen:
- **Usuarios y operadores**: personas que interactúan con el sistema.
- **Reglas y procesos de negocio**: cómo debe usarse el sistema en un contexto real.
- **Aspectos sociales y culturales**: normas de uso, resistencia al cambio, hábitos de trabajo.
- **Evolución constante**: deben adaptarse a nuevas necesidades, regulaciones y tecnologías.

📌 *Ejemplos:*  
- Una plataforma bancaria en línea que maneja cuentas, préstamos, clientes y transacciones.  
- Un sistema de historia clínica digital, con médicos, enfermeros, y regulaciones de salud.  
- Un sistema global de predicción meteorológica que combina sensores, satélites, datos públicos, software especializado y decisiones gubernamentales.

Estos sistemas son **difíciles de predecir, mantener y validar**, porque sus componentes humanos y sociales son tan importantes como los técnicos.


---

## ⚙️ Capas de un sistema sociotécnico

1. **Equipo:** Dispositivos físicos (hardware).
2. **Sistema operativo:** Control del hardware.
3. **Middleware:** Gestión de datos, redes.
4. **Aplicaciones:** Programas con lógica específica.
5. **Procesos de negocio:** Flujo de tareas de una organización.
6. **Organización:** Normas, reglas internas.
7. **Entorno social:** Leyes, cultura, aspectos humanos y éticos.

---

## 🧱 Propiedades emergentes

Son aquellas que **no existen en los componentes por separado**. Solo surgen al integrarlos:

- Fiabilidad
- Seguridad
- Usabilidad
- Rendimiento
- Capacidad de recuperación【66:19†IS__Libro_Sommerville_9(2).pdf】

> Ejemplo: una bicicleta se convierte en un medio de transporte solo cuando todos sus componentes funcionan juntos. Lo mismo pasa con un sistema de software hospitalario.

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

1. **Interdisciplinariedad:** Se debe trabajar con expertos en distintos campos.
2. **Tolerancia a errores:** Los sistemas deben prever fallos humanos y técnicos.
3. **Adaptabilidad:** El entorno cambia y el sistema debe evolucionar.
4. **Validación holística:** No basta con probar el código; se debe probar todo el sistema en conjunto.
5. **Factores organizacionales:** Cambios en procesos, resistencias internas o políticas pueden afectar el éxito.

---

## 🚨 Sistemas heredados

- Son sistemas sociotécnicos antiguos pero fundamentales.
- Muy costosos de reemplazar.
- Su mantenimiento es complejo por la obsolescencia y dependencia mutua entre sus componentes.

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


