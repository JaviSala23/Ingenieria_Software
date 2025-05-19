# 🎨 Clase: Introducción al Espacio de Color HSV y Mejora de Bordes con Canny

## 🎯 Objetivo

Comprender el uso del espacio de color **HSV** para segmentación por color y combinarlo con el algoritmo de **Canny** para mejorar la detección de objetos.

---

## 📘 ¿Qué es HSV?

HSV es un modelo de color alternativo al RGB:

- **H (Hue / Tono):** el color en sí (0 a 179 en OpenCV).
- **S (Saturation / Saturación):** qué tan puro o intenso es el color.
- **V (Value / Valor):** qué tan brillante u oscuro es el color.

### 🔎 ¿Por qué usar HSV?

- Es más robusto para segmentar colores que RGB.
- Permite separar el color del brillo y la iluminación.

---

## 🧰 Librerías necesarias

```python
import cv2
import numpy as np
```

---

## 🧪 Paso a paso: Detección de un color específico (por ejemplo, rojo)

### 1. Cargar imagen y convertir a HSV

```python
imagen = cv2.imread('objetos.jpg')
hsv = cv2.cvtColor(imagen, cv2.COLOR_BGR2HSV)
```

### 2. Definir el rango de color (rojo en este ejemplo)

```python
bajo_rojo = np.array([0, 100, 100])
alto_rojo = np.array([10, 255, 255])
```

> ⚠️ En el caso del rojo, a veces se usa también un segundo rango: `[160, 100, 100]` a `[179, 255, 255]` porque el rojo cruza el límite circular de matiz.

### 3. Crear una máscara con los píxeles dentro del rango

```python
mascara = cv2.inRange(hsv, bajo_rojo, alto_rojo)
```

### 4. Aplicar la máscara a la imagen original

```python
resultado = cv2.bitwise_and(imagen, imagen, mask=mascara)
cv2.imshow('Solo rojo', resultado)
```

---

## 📷 Visualizar el proceso completo

```python
cv2.imshow('Original', imagen)
cv2.imshow('Mascara', mascara)
cv2.imshow('Color detectado', resultado)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

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
