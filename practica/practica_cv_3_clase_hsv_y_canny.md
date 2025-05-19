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
## 🌈 Rango visual de tonos (Hue)

La siguiente imagen muestra cómo cambia el color al variar el valor de **Hue (H)** mientras la saturación y el valor permanecen al máximo (S=255, V=255):

![Mapa HSV](recursos/hsv_colormap.png)

### 📏 Valores típicos de Hue en OpenCV (0 a 179)

| Color       | Hue (aprox.) |
|-------------|--------------|
| Rojo        | 0 o 179      |
| Naranja     | 10 - 20      |
| Amarillo    | 20 - 30      |
| Verde       | 35 - 85      |
| Celeste     | 85 - 100     |
| Azul        | 100 - 130    |
| Violeta     | 130 - 160    |
| Rosa        | 160 - 170    |

> ⚠️ En OpenCV el Hue va de **0 a 179** (no 360), porque trabaja con imágenes de 8 bits.

---

## ✅ ¿Cómo usar estos rangos?

Si querés detectar un color, por ejemplo **verde**, podés definir:

```python
verde_bajo = np.array([40, 100, 100])
verde_alto = np.array([80, 255, 255])
```

Y así crear una **máscara** para detectar píxeles dentro de ese rango de tono, saturación y valor.

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
## 🌐 Recursos adicionales

- [Ejemplo interactivo de detección de colores en HSV](https://omes-va.com/deteccion-de-colores/)

---

## 🧠 Conclusión

El modelo HSV es una herramienta poderosa para analizar imágenes de forma más intuitiva y eficaz, especialmente cuando trabajamos con segmentación de colores en entornos reales. Aprender a usarlo correctamente es clave en cualquier proyecto de visión por computadora.


---

# 🧠 Mejora de Bordes con Canny

## 🔹 ¿Qué es el detector de bordes Canny?

El **algoritmo de Canny** es uno de los métodos más usados en visión por computadora para detectar **bordes** en imágenes. Un borde es una zona donde hay un cambio brusco de intensidad, como la separación entre dos objetos o un objeto y el fondo.

Detectar bordes es esencial para:
- Identificar formas y contornos.
- Reconocer objetos.
- Analizar estructuras en imágenes.

---

## ⚙️ ¿Cómo funciona Canny? (Etapas del algoritmo)

1. **Reducción de ruido (filtro Gaussiano):**
   - Se suaviza la imagen para evitar detectar bordes falsos.
   ```python
   suavizada = cv2.GaussianBlur(imagen, (5, 5), 0)
   ```

2. **Cálculo del gradiente:**
   - Se mide cómo cambia la intensidad en cada punto (con derivadas).

3. **Supresión de no-máximos:**
   - Se eliminan los puntos que no forman parte del borde más fuerte.

4. **Umbral por histéresis:**
   - Se definen dos umbrales:
     - `umbral_bajo`: ignora cambios leves.
     - `umbral_alto`: bordes fuertes y seguros.
   - Píxeles intermedios se aceptan solo si están conectados a bordes fuertes.

---

## 🔧 Aplicar Canny en OpenCV

```python
import cv2

canny = cv2.Canny(mascara, 100, 200)
cv2.imshow('Bordes Canny sobre mascara', canny)
```

- `100`: umbral inferior.
- `200`: umbral superior.
- Estos valores deben ajustarse dependiendo de la imagen.

---

## 📌 Recomendaciones prácticas

- Siempre aplicar un **filtro de suavizado** (como `GaussianBlur`) antes de usar Canny.
- Se puede aplicar Canny sobre:
  - Una imagen en **escala de grises**.
  - Una **máscara de color** generada con HSV.

Ejemplo completo:

```python
gris = cv2.cvtColor(imagen, cv2.COLOR_BGR2GRAY)
suave = cv2.GaussianBlur(gris, (5, 5), 0)
bordes = cv2.Canny(suave, 100, 200)
cv2.imshow('Bordes', bordes)
```

---

## 🧪 Actividad práctica

1. Usar una imagen con varios objetos.
2. Convertirla a escala de grises y suavizarla.
3. Aplicar Canny y ajustar los umbrales.
4. Mostrar la imagen original y los bordes.
5. Guardar el resultado como `bordes.jpg`.

---

## 💡 Preguntas para reflexionar

- ¿Qué diferencia hay entre aplicar Canny sobre la imagen en grises o sobre la máscara HSV?
- ¿Cómo afecta el desenfoque a la calidad de los bordes?
- ¿Qué pasa si los umbrales son demasiado bajos o demasiado altos?

---

## ✅ Conclusión

Canny es una herramienta poderosa para extraer los bordes más importantes de una imagen. Usado junto con HSV, permite detectar objetos específicos por color **y** forma, lo cual es clave para construir sistemas de visión robustos.


## 🌐 Recursos adicionales


- 📦 [Contando objetos aplicando detección de bordes con Canny en Python + OpenCV](https://omes-va.com/contando-objetos-aplicando-deteccion-de-bordes-con-canny-en-python-opencv/)

## 🔜 Próximo paso

Ahora que podemos aislar colores y detectar bordes con más precisión, vamos a **detectar contornos** y reconocer objetos combinando ambos enfoques.
