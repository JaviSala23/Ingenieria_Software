# 📚 Clase: Modelo Incremental

## 🎯 Objetivos de la clase

- Comprender qué es el Modelo Incremental y cómo se aplica en el desarrollo de software.
- Conocer las ventajas y desventajas del modelo.
- Identificar en qué contextos es adecuado aplicarlo.
- Diferenciarlo de otros modelos de ciclo de vida como Cascada, Prototipos o Iterativo.

---

## 1. 🧠 ¿Qué es el Modelo Incremental?

El **Modelo Incremental** es una estrategia de desarrollo donde el sistema se construye de forma **progresiva**, mediante una serie de **incrementos funcionales**.

Cada incremento añade nuevas funcionalidades al sistema base ya existente. Combina elementos del modelo en cascada (por tener fases definidas) con elementos iterativos (por sus ciclos de mejora continua).

---

## 2. 🔁 Etapas de cada Incremento

Cada incremento en el modelo incremental es como un mini-proyecto completo que sigue una secuencia estructurada de fases. Cada fase aporta al desarrollo de una parte funcional del sistema, que será integrada con los incrementos anteriores.

### 1. **Recolección de requerimientos parciales**

En esta fase se identifican y documentan los **requisitos específicos** del incremento a desarrollar. A diferencia del modelo en cascada, no se capturan todos los requisitos al comienzo, sino **solo los necesarios para este ciclo**.

- Se realiza junto al cliente o usuario final.
- Permite enfocarse en funcionalidades más importantes o prioritarias.
- Se pueden aplicar técnicas como entrevistas, encuestas o historias de usuario.

> ✏️ *Ejemplo:* “En este incremento queremos permitir registrar nuevos libros y listarlos por título.”

---

### 2. **Análisis**

Se analiza cómo los nuevos requisitos se integran con lo ya desarrollado. Se definen:

- Casos de uso asociados.
- Impacto en los datos, procesos y arquitectura.
- Validaciones o reglas de negocio involucradas.

> 🔍 *Objetivo:* entender a fondo qué se necesita para convertir esos requerimientos en funcionalidad real.

---

### 3. **Diseño**

En esta etapa se define **cómo se implementará** el incremento:

- Diseño de interfaz de usuario (mockups o wireframes).
- Diseño de base de datos (nuevas tablas, relaciones).
- Diseño de clases, módulos o componentes.
- Diseño de APIs o servicios si se usan.

> 📐 *El diseño debe contemplar la integración con los incrementos anteriores y prever futuras expansiones.*

---

### 4. **Codificación**

Se desarrolla el código del incremento:

- Se implementan las nuevas funcionalidades según el diseño.
- Se reutiliza código anterior cuando es posible.
- Se aplican buenas prácticas de programación y control de versiones.

> 💡 *Puede desarrollarse en paralelo por varios programadores si el diseño es modular.*

---

### 5. **Pruebas**

Antes de entregar el nuevo incremento al cliente, se realiza:

- **Pruebas unitarias:** validan cada función/módulo individualmente.
- **Pruebas de integración:** aseguran que lo nuevo no rompa lo anterior.
- **Pruebas funcionales:** simulan escenarios reales.
- **(Opcional) Pruebas de usuario:** el cliente puede probar el nuevo módulo.

> 🧪 *El objetivo es garantizar calidad y estabilidad del sistema total.*

---

### 6. **Entrega**

Una vez validado, el incremento es **integrado al producto principal** y **entregado** al cliente o usuario final.

- Se actualiza la documentación.
- Se capacita al usuario si es necesario.
- Se recibe feedback que puede servir para el próximo incremento.

> 🚀 *Cada entrega aumenta el valor del sistema para el usuario final.*

---

> 📌 **Importante:** el proceso se repite con cada nuevo conjunto de requerimientos, y el sistema va creciendo de forma controlada, segura y funcional.


---

## 3. 🧩 Ejemplo ilustrativo

### Proyecto: Sistema de Gestión de Biblioteca Escolar

La idea es desarrollar un sistema completo que permita a una institución educativa gestionar su biblioteca. En lugar de construir todo de una sola vez, aplicamos el **modelo incremental** para ir entregando partes funcionales de forma progresiva.

A continuación, se detalla cómo se puede dividir el desarrollo por incrementos:

| Incremento | Funcionalidad Agregada                                                                 |
|------------|-----------------------------------------------------------------------------------------|
| **1**      | **Autenticación y gestión de usuarios:** Login seguro, creación de cuentas, roles (admin/bibliotecario). |
| **2**      | **Gestión de libros:** Alta, baja y modificación de libros. Búsqueda por título, autor o categoría. |
| **3**      | **Préstamos y devoluciones:** Registrar préstamos, fechas de devolución, historial por usuario. |
| **4**      | **Reservas y sanciones:** Permitir reservar libros y registrar sanciones por retrasos. |
| **5**      | **Reportes y estadísticas:** Reportes por libro, usuario o fechas. Estadísticas de uso y ranking de libros más prestados. |
| **6**      | **Módulo web de consulta pública:** Portal donde alumnos consultan disponibilidad sin login, acceden a novedades o recomiendan libros. |

---

### 🔍 ¿Cómo se construye?

- **Después del incremento 1**, ya se puede acceder al sistema y crear cuentas.
- **Después del incremento 2**, el bibliotecario puede cargar libros y mantener actualizada la base.
- **Después del incremento 3**, ya es posible operar préstamos y devoluciones reales.
- **Con cada nuevo incremento, el sistema crece y mejora sin necesidad de rehacer lo anterior.**

---

Cada incremento se puede desarrollar, probar y entregar de forma independiente.

---
## 4. ✅ Ventajas del Modelo Incremental

El modelo incremental ofrece una serie de beneficios especialmente útiles en proyectos reales, donde los requisitos pueden cambiar o donde se necesita mostrar resultados tempranos:

- 🎯 **Entrega temprana de funcionalidades clave**  
  Cada incremento genera una versión funcional del sistema, lo que permite a los usuarios comenzar a utilizar el producto desde etapas tempranas.

- 🔁 **Facilita el feedback constante del cliente**  
  Los usuarios pueden probar el sistema en cada entrega, lo que permite hacer correcciones o mejoras antes de continuar con el siguiente incremento.

- 🔧 **Admite cambios en los requerimientos**  
  Al no requerir todos los requisitos desde el inicio, se pueden ajustar funcionalidades en base a la experiencia real del usuario y necesidades cambiantes.

- 🛡️ **Reduce el riesgo técnico y de gestión**  
  Al dividir el proyecto en partes más pequeñas y manejables, es más fácil controlar el avance, detectar errores temprano y anticipar problemas.

- 📊 **Mejor visibilidad y control del progreso**  
  Permite medir el avance real del proyecto con entregas concretas, facilitando la planificación, el control de calidad y la gestión del tiempo.

- 🧱 **Fomenta una arquitectura modular**  
  Obliga a pensar el sistema como una serie de componentes o módulos reutilizables e independientes, lo que mejora el mantenimiento futuro.

---

## 5. ⚠️ Desventajas del Modelo Incremental

Si bien es una metodología muy útil, también tiene limitaciones que deben considerarse:

- 🧠 **Requiere planificación precisa de los incrementos**  
  Se necesita una buena estrategia para decidir qué funcionalidades se desarrollan primero, y cómo se irán integrando con las siguientes.

- 🌀 **Puede generar duplicación de código o esfuerzo**  
  Si no se diseña una arquitectura común desde el inicio, los incrementos pueden terminar resolviendo lo mismo de distintas maneras.

- 🐢 **Posible pérdida de eficiencia global**  
  La integración repetida de módulos puede generar sobrecostos o problemas de rendimiento si no se hace con cuidado.

- 📉 **Dificultad para estimar el esfuerzo total**  
  Es más complejo prever el esfuerzo y el tiempo necesario para el sistema completo si se avanza por partes.

- 🧩 **No es ideal para proyectos muy pequeños o de una sola entrega**  
  Si el proyecto es simple y no requiere iteraciones ni feedback, este modelo puede resultar innecesariamente complejo.



## 6. 📌 Comparación con otros modelos

| Modelo      | Entrega parcial | Flexibilidad | Complejidad |
|-------------|------------------|--------------|-------------|
| Cascada     | ❌               | Baja         | Media       |
| Prototipos  | ✅               | Alta         | Baja        |
| Incremental | ✅               | Media/Alta   | Media       |
| Iterativo   | ✅               | Alta         | Alta        |

---



## 7. 🧪 Actividad práctica individual: App de Control de Hábitos (Modelo Incremental)

### 🎯 Objetivo:
Aplicar el modelo incremental planificando paso a paso una aplicación para controlar hábitos diarios. No es necesario programar, pero sí **diseñar, organizar y planificar** como lo haría un analista de software.

---

### 📝 Instrucciones

Vas a trabajar de forma **individual** en el diseño de una aplicación llamada **“Hábitos365”**, que permite al usuario llevar un registro diario de sus hábitos saludables.

Debés realizar lo siguiente:

---

### 🔹 Paso 1: Definí los incrementos

Dividí el desarrollo del sistema en **tres incrementos funcionales**. Completá esta tabla con las funcionalidades que se agregarán en cada uno:

| Incremento | Funcionalidades nuevas que se agregarán                               |
|------------|------------------------------------------------------------------------|
| 1          | (Ejemplo: Crear hábitos, marcar como cumplido hoy, ver hábitos activos) |
| 2          | (Ejemplo: Estadísticas semanales, editar o eliminar hábitos)          |
| 3          | (Ejemplo: Notificaciones, sincronizar con Google Calendar, modo oscuro) |

> ✏️ *Pensá qué funcionalidades básicas necesita el sistema al inicio y cuáles podés agregar en versiones futuras.*

---

### 🔹 Paso 2: Diagrama de Casos de Uso

Dibujá un **diagrama de casos de uso UML** del sistema completo (los tres incrementos juntos), incluyendo:

- Actor: Usuario
- Casos de uso para registrar, visualizar, editar hábitos, estadísticas, alertas, etc.
- Relaciones entre casos de uso (include/extend si corresponde)

> Podés hacerlo a mano o en herramientas como draw.io / diagrams.net

---

### 🔹 Paso 3: Diseño del primer incremento

Describí lo siguiente:

1. ¿Qué podrá hacer el usuario en la primera versión?
2. ¿Qué campos debe tener cada hábito? (Ej: nombre, frecuencia, ícono, etc.)
3. Dibujá un **boceto simple** (a mano o digital) de cómo se verá la pantalla principal.

> 🎯 *En este primer incremento, el sistema debe ser funcional aunque sea básico.*

---

### 🔹 Paso 4 (opcional): Maqueta funcional

Si sabés usar alguna herramienta visual (HTML, Kivy, Figma, Tkinter, etc.), creá una **maqueta o simulación del primer incremento**.

- No es obligatorio, pero suma puntos.
- Si no sabés programar, podés usar Canva, PowerPoint o Figma para simular pantallas.

---

### 🧠 Reflexión final

Respondé estas preguntas brevemente:

- ¿Qué ventajas encontraste al trabajar por incrementos?
- ¿Tuviste que reorganizar ideas durante el diseño?
- ¿Qué aprendiste sobre planificación de sistemas?

---

### 📌 Entregable

Subí un documento PDF (o carpeta comprimida) con:

- Tabla de incrementos completa
- Diagrama de casos de uso
- Diseño del incremento 1 (descripción y boceto)
- (Opcional) Captura o link a la maqueta
- Reflexión escrita

---


---

> 💬 **Reflexión final:** ¿Qué diferencias ves entre el modelo incremental y tu forma de desarrollar proyectos habitualmente?
