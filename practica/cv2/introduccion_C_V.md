
# 👁️ Introducción a la Visión por Computadora

## ¿Qué es la visión por computadora?

La visión por computadora es un campo dentro de la inteligencia artificial que busca permitir que las máquinas "vean" e interpreten el contenido de imágenes y videos, de forma similar al ojo humano.

Consiste en técnicas y algoritmos que analizan píxeles para identificar patrones, formas, colores, objetos y más. Su objetivo es extraer información útil a partir de imágenes o secuencias de video.

---

## 🌍 Aplicaciones reales

- **Reconocimiento facial:** desbloqueo de teléfonos, sistemas de vigilancia.
- **Lectura de matrículas:** peajes, controles policiales.
- **Diagnóstico médico:** análisis de radiografías, resonancias, etc.
- **Clasificación de objetos:** líneas de producción, control de calidad.
- **Agricultura de precisión:** detección de plagas y estado de cultivos.
- **Vehículos autónomos:** detección de peatones, semáforos, obstáculos.
- **Realidad aumentada:** filtros de Instagram, juegos como Pokémon GO.

---

## 🤖 Relación con la Inteligencia Artificial

La visión por computadora es una rama de la inteligencia artificial. En muchos casos, se combina con aprendizaje automático (machine learning) o redes neuronales profundas (deep learning) para lograr tareas como reconocimiento facial, clasificación de imágenes o detección de objetos.

---

## 🧠 Conceptos clave

- **Imagen digital:** es una matriz de píxeles. Cada píxel contiene información sobre el color en ese punto.
- **Resolución:** cantidad de píxeles que tiene una imagen (ejemplo: 1920x1080).
- **Canales de color:**
  - RGB: Rojo, Verde, Azul (común en color).
  - Escala de grises: un solo canal, solo intensidad.
- **Detección:** encontrar la ubicación de un objeto.
- **Reconocimiento:** saber qué es el objeto.
- **Segmentación:** separar partes de la imagen por categorías o regiones.

---

## 🧰 Herramientas más utilizadas

- **Lenguajes:** Python, C++, JavaScript.
- **Librerías populares en Python:**
  - `OpenCV`: para procesamiento de imágenes y video.
  - `PIL` / `Pillow`: para manipular imágenes.
  - `scikit-image`: análisis de imágenes.
  - `TensorFlow`, `PyTorch`: visión con redes neuronales.

---

## 🔁 Flujo básico de un sistema de visión

1. **Captura o carga** de la imagen o video.
2. **Procesamiento:** mejorar, limpiar o transformar la imagen (ej: cambiar color, enfocar, eliminar ruido).
3. **Análisis:** detección, segmentación, clasificación, medición.
4. **Resultado o acción:** mostrar en pantalla, tomar una decisión automática, activar una alarma, etc.

---

## 🧪 ¿Cómo se representa una imagen en código?

Una imagen en Python se puede representar como una matriz (array) de números usando NumPy:

- Imagen en escala de grises: matriz 2D de enteros (valores de 0 a 255).
- Imagen en color: matriz 3D (alto, ancho, 3 canales RGB).

Ejemplo:
```python
import numpy as np

# Imagen gris de 3x3 píxeles
img = np.array([
    [0, 128, 255],
    [64, 128, 192],
    [255, 255, 0]
])
```

---

## 💬 Reflexión

La visión por computadora ya está en todos lados: desde nuestras cámaras hasta autos inteligentes. Aprender a trabajar con imágenes es el primer paso para crear soluciones innovadoras en múltiples campos.

En la próxima clase vamos a comenzar a trabajar con `OpenCV`, una de las bibliotecas más potentes y utilizadas para procesar imágenes desde Python.
