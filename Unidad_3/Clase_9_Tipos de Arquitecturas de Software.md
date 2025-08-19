# 📘 Clase: Tipos de Arquitecturas de Software  

En el desarrollo de software existen diferentes **formas de organizar un sistema**, conocidas como **arquitecturas**.  
Cada una tiene características, ventajas y desventajas que la hacen más adecuada para ciertos proyectos.  

---

## 1. Arquitectura Monolítica  

### 🔹 ¿Cómo funciona?  
- Todo el sistema está dentro de una **única aplicación**.  
- La interfaz, la lógica de negocio y el acceso a datos se encuentran **mezclados** en un mismo bloque de código.  

### 🎯 ¿Para qué sirve?  
- Aplicaciones pequeñas o proyectos iniciales.  
- Casos en los que no se necesita gran escalabilidad.  

### ✅ Ventajas  
- Fácil de desarrollar al inicio.  
- Menor complejidad en la configuración.  

### ❌ Desventajas  
- Difícil de mantener a largo plazo.  
- Poca escalabilidad: si crece mucho, se vuelve lento y frágil.  

---

## 2. Arquitectura Cliente-Servidor  

### 🔹 ¿Cómo funciona?  
- El sistema se divide en dos partes:  
  - **Cliente:** la aplicación que usa el usuario (ejemplo: navegador web, app móvil).  
  - **Servidor:** procesa la información y responde a las peticiones del cliente.  

### 🎯 ¿Para qué sirve?  
- Aplicaciones de red como sistemas de correo electrónico, páginas web o bases de datos compartidas.  

### ✅ Ventajas  
- Separación clara entre quien pide (cliente) y quien responde (servidor).  
- Permite múltiples clientes conectados al mismo servidor.  

### ❌ Desventajas  
- Si el servidor falla, todos los clientes quedan sin servicio.  
- Puede sobrecargarse con muchos usuarios.  

---

## 3. Arquitectura en Capas (Three-Tier)  

### 🔹 ¿Cómo funciona?  
Se organiza el sistema en **tres capas principales**:  
1. **Presentación:** lo que ve el usuario (interfaces gráficas, web, móvil).  
2. **Lógica de negocio:** las reglas y procesos que dan sentido a la aplicación.  
3. **Datos:** bases de datos o sistemas de almacenamiento.  

### 🎯 ¿Para qué sirve?  
- Aplicaciones empresariales donde se necesita **orden, seguridad y crecimiento**.  

### ✅ Ventajas  
- Mejor mantenibilidad: se puede cambiar una capa sin afectar las otras.  
- Facilita la escalabilidad distribuyendo las capas en distintos servidores.  

### ❌ Desventajas  
- Mayor complejidad que un monolito simple.  
- Requiere coordinación entre capas.  

---

## 4. Arquitectura Orientada a Servicios (SOA)  

### 🔹 ¿Cómo funciona?  
- El sistema se organiza en **servicios independientes** que se comunican entre sí.  
- Cada servicio cumple una función concreta (ejemplo: autenticación, pagos, envíos).  

### 🎯 ¿Para qué sirve?  
- Empresas que necesitan **reutilizar servicios** en diferentes aplicaciones.  
- Grandes sistemas distribuidos.  

### ✅ Ventajas  
- Reutilización de servicios en distintos sistemas.  
- Flexibilidad para integrar aplicaciones heterogéneas.  

### ❌ Desventajas  
- Puede ser más lento por depender de comunicaciones entre servicios.  
- Requiere estándares claros y buena planificación.  

---

## 5. Arquitectura de Microservicios  

### 🔹 ¿Cómo funciona?  
- Similar a SOA, pero con **servicios más pequeños y especializados**.  
- Cada microservicio es independiente, puede desarrollarse en diferentes lenguajes y desplegarse en distintos servidores.  

### 🎯 ¿Para qué sirve?  
- Aplicaciones modernas que requieren **alta escalabilidad y despliegue rápido**.  
- Ejemplos: Netflix, Amazon, Spotify.  

### ✅ Ventajas  
- Escalabilidad: cada microservicio puede crecer de forma independiente.  
- Mayor resiliencia: si un servicio falla, el resto puede seguir funcionando.  

### ❌ Desventajas  
- Complejidad en la comunicación entre microservicios.  
- Requiere infraestructura más avanzada (Docker, Kubernetes, CI/CD).  

---

## 6. Arquitectura en la Nube  

### 🔹 ¿Cómo funciona?  
- El software no está en un solo servidor físico, sino que se ejecuta en **servidores distribuidos en la nube** (AWS, Azure, Google Cloud).  
- Modelos:  
  - **IaaS:** infraestructura como servicio.  
  - **PaaS:** plataforma como servicio.  
  - **SaaS:** software como servicio.  

### 🎯 ¿Para qué sirve?  
- Sistemas que necesitan alta disponibilidad y acceso desde cualquier parte del mundo.  
- Empresas que quieren reducir costos de infraestructura propia.  

### ✅ Ventajas  
- Escalabilidad prácticamente ilimitada.  
- Pago por uso (reduce costos iniciales).  
- Alta disponibilidad.  

### ❌ Desventajas  
- Dependencia del proveedor de nube.  
- Posibles riesgos de seguridad si no se configuran correctamente.  

---

## ✍️ Actividad en Clase  

1. Elijan **una arquitectura** (monolítica, cliente-servidor, en capas, SOA, microservicios o nube).  
2. Expliquen cómo funciona y para qué sirve en 5 minutos frente al curso.  
3. Den un ejemplo real de un software que use esa arquitectura.  
