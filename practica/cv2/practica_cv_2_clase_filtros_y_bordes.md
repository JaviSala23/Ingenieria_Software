
# 🛠️ Clase Práctica: Filtros y Detección de Bordes con OpenCV

## 🎯 Objetivo
Aprender a aplicar filtros básicos para suavizar imágenes y utilizar el algoritmo de Canny para detectar bordes.

---

## 📌 Contenidos

### 🔹 1. Suavizado de imágenes

#### 📍 ¿Por qué suavizar?
Los filtros suavizantes ayudan a reducir el ruido en una imagen, lo cual es útil antes de aplicar técnicas más complejas como detección de bordes o contornos.

#### 📌 Tipos de filtros:

##### a) Desenfoque promedio (Blur)
```python
import cv2

imagen = cv2.imread('paisaje.jpg')
blur = cv2.blur(imagen, (5, 5))

cv2.imshow('Desenfoque promedio', blur)
```

##### b) Desenfoque Gaussiano
```python
gauss = cv2.GaussianBlur(imagen, (5, 5), 0)

cv2.imshow('Desenfoque Gaussiano', gauss)
```

##### c) Filtro de Mediana
```python
mediana = cv2.medianBlur(imagen, 5)

cv2.imshow('Filtro de Mediana', mediana)
```

---

### 🔹 2. Conversión a escala de grises
```python
gris = cv2.cvtColor(imagen, cv2.COLOR_BGR2GRAY)
cv2.imshow('Escala de grises', gris)
```

---

### 🔹 3. Detección de bordes con Canny

```python
bordes = cv2.Canny(gris, 100, 200)

cv2.imshow('Bordes Canny', bordes)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

---

## 🧪 Actividad práctica

1. Cargar una imagen de tu elección.
2. Aplicar al menos dos filtros diferentes (promedio, gaussiano o mediana).
3. Convertir la imagen a escala de grises.
4. Aplicar detección de bordes con Canny.
5. Mostrar todas las imágenes intermedias.
6. Guardar el resultado final como `bordes_final.jpg`.

---

## ✅ Cierre

Con estos pasos ya podés preparar imágenes para ser analizadas más fácilmente. Detectar bordes es el primer paso para poder identificar objetos y contornos, tema que veremos en la próxima clase.
