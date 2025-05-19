# 🎨 Clase: Introducción al Espacio de Color HSV y Mejora de Bordes con Canny

## 🎯 Objetivo

Comprender el uso del espacio de color **HSV** para segmentación por color y combinarlo con el algoritmo de **Canny** para mejorar la detección de objetos.

---

## 📘 ¿Qué es HSV?

HSV es un modelo de color que representa los colores en tres componentes intuitivos para los humanos:

- **H - Hue (Tono):** el tipo de color (rojo, azul, verde...).
- **S - Saturation (Saturación):** la intensidad o pureza del color.
- **V - Value (Valor / Brillo):** el nivel de luminosidad.

A diferencia del modelo RGB (Rojo, Verde, Azul), que mezcla colores directamente, HSV **separa el color del brillo y la intensidad**, lo cual es muy útil para análisis de imágenes.

---

## 🔍 Detalle de cada componente

### 🟥 H - Hue (Tono)
- Representa el color como un ángulo en la rueda de colores (0° a 360°).
- En OpenCV, se escala entre **0 y 179**.
- Ejemplos aproximados:
  - 0: Rojo
  - 30: Naranja
  - 60: Amarillo
  - 90: Verde claro
  - 120: Verde fuerte
  - 150: Azul
  - 179: Rojo nuevamente

### 🟨 S - Saturation (Saturación)
- Indica **qué tan puro o intenso** es el color.
- Valor bajo (≈ 0): grisáceo o desaturado.
- Valor alto (≈ 255): color fuerte, vivo.

### 🟩 V - Value (Brillo)
- Indica la **luminosidad** del color.
- Valor bajo: color oscuro o negro.
- Valor alto: color claro o brillante.

---

## 🤖 ¿Por qué usar HSV en lugar de RGB?

### ✅ Ventajas de HSV:
- **Mejor segmentación por color**: más resistente a cambios de luz.
- **Separación clara entre color y brillo**.
- Ideal para:
  - Detección de colores específicos.
  - Seguimiento de objetos con marcadores de color.
  - Procesamiento de imágenes en entornos no controlados.

### 👎 Problemas comunes con RGB:
- Los tres canales (R, G, B) se ven afectados simultáneamente por la iluminación.
- Es difícil determinar rangos precisos de colores.

---

## 🧪 Ejemplo práctico

```python
import cv2
import numpy as np

imagen = cv2.imread('colores.jpg')
hsv = cv2.cvtColor(imagen, cv2.COLOR_BGR2HSV)

# Rango para detectar color rojo (segmentación)
bajo_rojo = np.array([0, 100, 100])
alto_rojo = np.array([10, 255, 255])

mascara = cv2.inRange(hsv, bajo_rojo, alto_rojo)
resultado = cv2.bitwise_and(imagen, imagen, mask=mascara)

cv2.imshow('Color detectado', resultado)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

---

## 🧠 Conclusión

El modelo HSV es una herramienta poderosa para analizar imágenes de forma más intuitiva y eficaz, especialmente cuando trabajamos con segmentación de colores en entornos reales. Aprender a usarlo correctamente es clave en cualquier proyecto de visión por computadora.


---

## 🔹 Mejora de bordes con Canny (opcional pero recomendado)

### Aplicar Canny sobre la máscara o la imagen filtrada

```python
canny = cv2.Canny(mascara, 100, 200)
cv2.imshow('Bordes Canny sobre mascara', canny)
```

---

## 🧪 Actividad práctica

1. Usar una imagen con varios objetos de diferentes colores.
2. Detectar y aislar un color específico usando HSV.
3. Aplicar Canny a la imagen segmentada para obtener sus bordes.
4. Mostrar la imagen original, la máscara, el resultado filtrado y los bordes.
5. Guardar cada una como: `mascara.jpg`, `filtrado.jpg`, `bordes.jpg`.

---

## 🧠 Preguntas para reflexionar

- ¿Qué pasa si la iluminación cambia? ¿Sigue funcionando bien HSV?
- ¿Qué ventajas tiene HSV frente a RGB?
- ¿Qué parámetros de Canny conviene ajustar en tu imagen?

---

## 🔜 Próximo paso

Ahora que podemos aislar colores y detectar bordes con más precisión, vamos a **detectar contornos** y reconocer objetos combinando ambos enfoques.
