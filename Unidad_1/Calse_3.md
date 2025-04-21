# 📘 Clase 3 – Software en Sistemas Complejos

## 🧠 ¿Qué es un sistema complejo?

Un sistema complejo es un conjunto de elementos interrelacionados que interactúan de formas no lineales, impredecibles y a menudo emergentes. Estos sistemas pueden ser físicos, sociales, biológicos o computacionales. En el ámbito del software, nos enfocamos en **sistemas sociotécnicos**: aquellos que combinan aspectos tecnológicos (hardware/software) con procesos sociales (usuarios, organizaciones, normas).

### 🎯 Ejemplos de sistemas complejos:
- Sistemas de gestión hospitalaria.
- Control de tráfico aéreo.
- Plataformas bancarias globales.
- Redes sociales a gran escala.
- Sistemas embebidos críticos (como una bomba de insulina).

---

## 🧩 Componentes de un sistema sociotécnico

1. **Hardware**: Dispositivos físicos como servidores, sensores, computadoras personales.
2. **Software**: Programas que realizan tareas específicas.
3. **Procesos**: Conjunto de reglas y procedimientos que definen el comportamiento del sistema.
4. **Usuarios**: Personas que interactúan directa o indirectamente con el sistema.
5. **Entorno operativo**: El contexto donde se implementa el sistema (leyes, regulaciones, clima, etc.).
6. **Datos**: Información que circula entre componentes y se utiliza como base para la toma de decisiones.

---

## ⚙️ Características de los sistemas de software en entornos complejos

- **Interdependencia**: Cambios en un componente pueden afectar a otros.
- **Emergencia**: El comportamiento del sistema completo no puede predecirse simplemente conociendo sus partes.
- **Evolución continua**: Deben adaptarse a requisitos, tecnologías y contextos cambiantes.
- **Distribución**: Componentes distribuidos físicamente en distintas ubicaciones.
- **Heterogeneidad**: Combinación de múltiples tecnologías, dispositivos, lenguajes y plataformas.
- **Alta criticidad**: Fallas pueden causar consecuencias graves o irreversibles.

---

## 🧪 Ejemplo: Sistema de bomba de insulina

Este sistema embebido monitorea el nivel de glucosa en sangre y administra insulina de forma automática. Combina:
- Sensores que recogen datos biomédicos.
- Software embebido que decide la dosis adecuada.
- Hardware que activa la bomba.
- Interfaz para médicos y pacientes.
- Registro y monitoreo remoto.

Se considera **crítico para la seguridad**, por lo que su diseño exige alta confiabilidad, pruebas exhaustivas y mecanismos de recuperación ante fallas.

---

## 🧠 Implicancias para el desarrollo de software

1. **No basta con programar bien**: Es necesario comprender el sistema completo.
2. **Requiere trabajo interdisciplinario**: Participan médicos, ingenieros, operadores, usuarios finales.
3. **Alta dependencia del entorno**: Cambios regulatorios, actualización de dispositivos o red pueden afectar el funcionamiento.
4. **Pruebas realistas**: Deben replicar el entorno real de uso y prever fallas.

---

## 📌 Conclusión

Desarrollar software para sistemas complejos implica mucho más que escribir código. Involucra comprender cómo interactúa ese software con personas, procesos y dispositivos en escenarios reales. La ingeniería de software debe ofrecer métodos para modelar, validar, desplegar y mantener sistemas que son altamente interdependientes y críticos.

En la próxima clase comenzaremos a **modelar estos sistemas** y a practicar con ejemplos inspirados en los casos del libro de Sommerville.
