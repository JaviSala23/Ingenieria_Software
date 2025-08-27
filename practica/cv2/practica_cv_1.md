
# 🛠️ Clase Práctica 1: Primeros pasos con OpenCV

## 🎯 Objetivo
Aprender a usar OpenCV para:
- Cargar imágenes.
- Visualizarlas en pantalla.
- Convertirlas a escala de grises.
- Realizar modificaciones básicas (dibujos, textos).
- Guardar el resultado.

---

## 🧰 Requisitos

Antes de comenzar, asegurate de tener instalados:

- **Python 3**
- **OpenCV**  
  Instalación:
  ```bash
  pip install opencv-python
  ```

---

## 📂 Estructura sugerida del proyecto

```
proyecto_cv/
├── paisaje.jpg       # Imagen de ejemplo
├── clase1.py         # Archivo con el código de esta clase
```

---

## 💻 Código explicado paso a paso

### 1. Importar OpenCV
```python
import cv2
```

### 2. Cargar una imagen
```python
imagen = cv2.imread('paisaje.jpg')
```

### 3. Mostrar la imagen en una ventana
```python
cv2.imshow('Imagen original', imagen)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### 4. Convertir la imagen a escala de grises
```python
gris = cv2.cvtColor(imagen, cv2.COLOR_BGR2GRAY)
cv2.imshow('Escala de grises', gris)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### 5. Dibujar sobre la imagen

```python
# Dibujar un rectángulo verde
cv2.rectangle(imagen, (50, 50), (200, 200), (0, 255, 0), 3)

# Dibujar un círculo rojo
cv2.circle(imagen, (300, 150), 40, (0, 0, 255), -1)  # relleno

# Dibujar una línea azul
cv2.line(imagen, (0, 0), (imagen.shape[1], imagen.shape[0]), (255, 0, 0), 2)

# Escribir texto
cv2.putText(imagen, 'Paisaje', (60, 45), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 0), 2)

cv2.imshow('Modificada', imagen)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

---

### 6. Guardar la imagen modificada
```python
cv2.imwrite('modificada.jpg', imagen)
```

---

## 🧪 Desafío propuesto

1. Cargar tu propia imagen (no paisaje.jpg).
2. Convertirla a escala de grises.
3. Dibujar al menos:
   - Un rectángulo
   - Un círculo
   - Una línea
   - Un texto personalizado
4. Guardar el resultado como `mi_modificada.jpg`.

---

## ✅ Conclusión

Ya aprendiste a usar OpenCV para trabajar con imágenes. En la próxima clase vamos a explorar cómo aplicar filtros y detectar bordes.
