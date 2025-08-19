# 📘 Clase: Introducción a las Arquitecturas de Software  

---

## 📘 Arquitectura de Software  

La **arquitectura de software** es la **estructura conceptual y organizativa** de un sistema, que define:  

1. **Los componentes principales del sistema** (módulos, servicios, bases de datos, interfaces).  
2. **Las relaciones e interacciones** entre esos componentes.  
3. **Los principios y reglas** que guían su diseño y evolución.  

Se la puede entender como una **capa intermedia** entre los **requisitos funcionales** (qué debe hacer el sistema) y la **implementación técnica** (cómo se programa).  

🔹 En otras palabras, la arquitectura responde a la pregunta:  
**“¿Cómo organizamos el sistema para que cumpla su propósito de forma eficiente, segura y escalable?”**  

---

### 🌍 Analogía con la Arquitectura de un Edificio  

Así como un arquitecto de construcción:  
- Decide cuántos pisos tendrá el edificio.  
- Dónde estarán los cimientos, paredes y puertas.  
- Qué materiales usar y cómo se conectan las instalaciones.  

👉 El **arquitecto de software** define:  
- Qué módulos existirán en el sistema.  
- Cómo se comunicarán (ej: APIs, servicios, bases de datos).  
- Qué tecnologías se utilizarán (frameworks, lenguajes, servidores).  
- Qué criterios de calidad se deben cumplir (seguridad, rendimiento, mantenimiento).  

---

### 🔹 Conceptos Fundamentales  

### 1. Módulos  
- Son las **unidades lógicas** en las que se divide el software.  
- Cada módulo cumple una función específica (ejemplo: módulo de facturación, módulo de usuarios, módulo de reportes).  
- Favorecen la **organización** y el **mantenimiento** del sistema.  

### 2. Servicios  
- Son **funcionalidades independientes** que pueden ser consumidas por otros módulos o sistemas.  
- Se suelen exponer a través de **APIs** (REST, SOAP, GraphQL).  
- Ejemplo: un servicio de autenticación de usuarios que puede ser usado por diferentes aplicaciones.  

### 3. Bases de Datos  
- Son los **repositorios estructurados de información**.  
- Permiten almacenar, consultar y mantener los datos del sistema.  
- Pueden ser relacionales (SQL) o no relacionales (NoSQL).  
- Ejemplo: MySQL, PostgreSQL, MongoDB.  

### 4. Interfaces  
- Son los **puntos de comunicación** entre módulos, servicios o usuarios.  
- Pueden ser:  
  - **Interfaces gráficas (GUI):** pantallas para el usuario.  
  - **Interfaces de programación (API):** reglas para que otros sistemas se conecten.  
- Ejemplo: una aplicación móvil que se conecta con el backend mediante una API REST.  


---

## 🚀 Beneficios de una Buena Arquitectura de Software  

Una buena arquitectura permite:  

### ✅ Escalabilidad  
- La capacidad de un sistema de **crecer sin perder rendimiento**.  
- Puede ser **vertical** (mejorando el hardware: más memoria, procesador más potente) o **horizontal** (añadiendo más servidores o instancias).  
- Ejemplo: una red social que empieza con 1.000 usuarios y puede adaptarse para millones sin reescribir todo el código.  

---

### ✅ Mantenibilidad  
- Facilidad para **actualizar, reparar o extender** el sistema.  
- Una arquitectura modular permite cambiar un componente sin afectar al resto.  
- Reduce el tiempo y costo de corregir errores o agregar nuevas funciones.  
- Ejemplo: en un sistema de ventas, se puede modificar el módulo de facturación sin tocar el módulo de clientes.  

---

### ✅ Seguridad  
- La arquitectura define **puntos críticos de protección** (acceso a datos, comunicaciones, autenticación).  
- Una buena organización separa responsabilidades, evitando que un fallo comprometa todo el sistema.  
- Incluye prácticas como cifrado, control de accesos y validación de datos.  
- Ejemplo: separar la base de datos en un servidor distinto del frontend para evitar ataques directos.  

---

### ✅ Eficiencia  
- Uso **óptimo de los recursos** (CPU, memoria, red, almacenamiento).  
- Una arquitectura eficiente evita redundancias, reduce tiempos de respuesta y mejora la experiencia de usuario.  
- Ejemplo: un servicio de streaming que ajusta la calidad del video según la velocidad de internet del usuario.  

---

### ✅ Comunicación Clara  
- La arquitectura funciona como un **mapa** del sistema.  
- Permite que diferentes perfiles (programadores, diseñadores, testers, gerentes) tengan una **visión común** de cómo está organizado.  
- Evita malentendidos y facilita la coordinación entre equipos.  
- Ejemplo: un diagrama de arquitectura ayuda a que un nuevo integrante entienda rápidamente cómo se estructura el sistema.  
 

---

## 3. Relación con Escalabilidad, Seguridad y Mantenimiento  

La calidad de una arquitectura de software se refleja principalmente en su capacidad para **crecer, protegerse y mantenerse en el tiempo**.  

---

### 🔹 Escalabilidad  
- Es la capacidad de un sistema para **soportar un aumento en la carga de trabajo** (más usuarios, más datos, más procesos) sin perder rendimiento.  
- Puede lograrse de dos formas:  
  - **Escalabilidad vertical:** mejorar los recursos del mismo servidor (más memoria, CPU más potente).  
  - **Escalabilidad horizontal:** distribuir la carga en varios servidores o instancias.  
- 📌 **Ejemplo:** una tienda online que funciona con 100 usuarios simultáneos y puede adaptarse para atender a 10.000 en fechas como el Black Friday sin caerse.  

---

### 🔹 Seguridad  
- La arquitectura debe incorporar **mecanismos de protección** desde el diseño, no como un agregado posterior.  
- Incluye prácticas como:  
  - Autenticación y autorización de usuarios.  
  - Cifrado de contraseñas y comunicaciones.  
  - Separación de capas para que un fallo en una parte no comprometa todo el sistema.  
- 📌 **Ejemplo:** una aplicación bancaria que mantiene la base de datos en un servidor independiente y encriptado, mientras el frontend solo muestra la información necesaria al usuario.  

---

### 🔹 Mantenimiento  
- Se refiere a la facilidad para **actualizar, corregir errores y agregar nuevas funciones** sin que el sistema se vuelva frágil o inestable.  
- Una arquitectura bien organizada (modular o en capas) permite modificar una parte del sistema sin afectar el resto.  
- 📌 **Ejemplo:** en un sistema hospitalario, actualizar el módulo de turnos sin alterar el módulo de historias clínicas.  

---

## 4. Ejemplos Visuales  

### ❌ Mala arquitectura (Monolito caótico)  
- Todo el código está escrito en un único archivo o en pocos archivos sin separación de responsabilidades.  
- La lógica de negocio, la interfaz gráfica y el acceso a la base de datos están **mezclados entre sí**.  
- Consecuencias:  
  - Muy difícil de **mantener**: un cambio pequeño puede generar errores en otras partes.  
  - Poco **escalable**: no soporta bien el crecimiento en usuarios o funcionalidades.  
  - Baja **seguridad**: si un atacante accede a una parte, probablemente acceda a todo.  
- 📌 **Ejemplo real:** una aplicación antigua donde el mismo archivo PHP o JavaScript contiene las pantallas, las consultas a la base de datos y la lógica de negocio.  

---

### ✅ Buena arquitectura (Organizada en capas)  
- El sistema está dividido en **capas bien definidas**:  
  1. **Capa de presentación (interfaz):** lo que el usuario ve (ejemplo: app móvil, sitio web).  
  2. **Capa de lógica de negocio:** donde se procesan las reglas y funciones principales (ejemplo: cálculos, validaciones).  
  3. **Capa de datos:** donde se almacenan y gestionan las bases de datos.  
- Ventajas:  
  - Facilita el **mantenimiento**, ya que se puede modificar una capa sin afectar a las otras.  
  - Permite mayor **seguridad**, aislando datos sensibles en su propia capa.  
  - Mejora la **escalabilidad**, porque cada capa puede crecer o distribuirse en distintos servidores.  
- 📌 **Ejemplo real:** una tienda online donde:  
  - El frontend muestra los productos y el carrito (presentación).  
  - El backend procesa los pedidos, aplica descuentos y calcula envíos (lógica de negocio).  
  - La base de datos guarda usuarios, productos y transacciones (datos).

---


## 📝 Tarea de Investigación  

👉 De forma individual, cada estudiante deberá **investigar la arquitectura real de un software conocido**.  
- Puede ser **Netflix, WhatsApp, Instagram, Amazon, Mercado Libre, Spotify**, etc.  
- Preguntas orientadoras:  
  1. ¿Qué tipo de arquitectura utiliza (monolito, cliente-servidor, microservicios, en la nube, etc.)?  
  2. ¿Qué ventajas obtiene al usar esa arquitectura?  
  3. ¿Qué desafíos o problemas debe resolver con esa arquitectura?  
  4. ¿Qué tecnologías o herramientas principales emplea (bases de datos, servidores, APIs, frameworks)?  

📌 **Formato de entrega:**  
- Un informe breve (1 o 2 páginas) con texto y, si es posible, un esquema o diagrama de la arquitectura investigada.  
- Puede entregarse en formato digital (Word, PDF o diapositiva).  
---

📌 **Conclusión:**  
La arquitectura de software es **la base** sobre la que se construye cualquier aplicación.  
Una buena arquitectura no solo resuelve problemas actuales, sino que prepara al sistema para el futuro.  
