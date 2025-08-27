# 📷 Clase: Apertura de Cámara Web con OpenCV (Local o por URL)

## 🎯 Objetivo

Aprender a capturar video en tiempo real utilizando OpenCV desde:

1. La cámara web local del dispositivo.
2. Una cámara IP o stream en vivo a través de una URL.

Esta clase no aplica ningún filtro ni procesamiento. Se enfoca en **abrir, visualizar y cerrar** correctamente el stream de video.

---

## 🧰 Requisitos

- Python 3
- OpenCV (`pip install opencv-python`)
- Una cámara conectada o una URL de stream válida

---

## 🧠 ¿Qué es `cv2.VideoCapture`?

`VideoCapture` es una clase de OpenCV que permite acceder a una **fuente de video**, ya sea:

- Una cámara conectada localmente (como una webcam).
- Un archivo de video (`.mp4`, `.avi`, etc.).
- Una dirección IP (streaming de red o cámara IP).

---

## 🔹 Apertura de cámara local (Webcam)

```python
import cv2

# Abrir cámara
camara = cv2.VideoCapture(0)

# Verificar que la cámara se abrió correctamente
if not camara.isOpened():
    print("No se pudo abrir la cámara.")
    exit()

print("Presioná 'q' para salir.")

while True:
    ret, frame = camara.read()
    if not ret:
        print("No se pudo leer el frame.")
        break

    # Mostrar el frame en una ventana única
    cv2.imshow('Camara en vivo', frame)

    # Esperar 1 milisegundo y chequear si se presiona 'q'
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

# Liberar recursos
camara.release()
cv2.destroyAllWindows()
```

### ✅ Explicación:
- `cv2.VideoCapture(0)`: abre la primera cámara conectada.
- `.read()`: captura cada fotograma (frame).
- `imshow()`: muestra el frame en una ventana.
- `waitKey(1)`: actualiza la ventana cada milisegundo y espera si se presionó una tecla (`q` para salir).
- `.release()`: libera la cámara.
- `destroyAllWindows()`: cierra todas las ventanas abiertas por OpenCV.

---

## 🔹 Apertura de cámara IP o por URL

```python
url = 'http://mi-camara-ip/video'
camara = cv2.VideoCapture(url)
```

- Este método es útil para:
  - Cámaras IP conectadas a una red.
  - Video en vivo transmitido desde un celular (por ejemplo, con apps como IP Webcam en Android).
  - Transmisión desde otro dispositivo por WiFi.

> ⚠️ La calidad y estabilidad del stream depende del ancho de banda y el tipo de protocolo de la cámara. En muchos casos se usan URL con MJPEG, RTSP, o HTTP.

---

## 🧪 Actividad práctica

1. Abrir la webcam local y mostrar el video en una ventana.
2. Cerrar la cámara correctamente al presionar `q`.
3. (Opcional) Probar una app de cámara IP en el celular y acceder desde la PC con la URL que te muestra.
4. Mostrar un contador de frames en consola mientras se transmite.

---

## 🧠 Conceptos clave

- **Stream de video**: secuencia de imágenes (frames) que llegan en tiempo real.
- **Frame**: imagen individual del stream.
- **FPS (Frames por segundo)**: cuántos frames se procesan por segundo.
- **Latencia**: retardo entre la captura y la visualización.

---

## 🛑 Buenas prácticas

- Siempre verificar que `.isOpened()` sea `True` antes de leer frames.
- Usar `.release()` para liberar la cámara cuando no se usa más.
- Manejar excepciones si la URL no responde o si la cámara está ocupada.

---

## 🔚 Próxima clase

Vamos a capturar **fotogramas específicos (como si fuera una foto)** y luego aplicar filtros, reconocimiento y segmentación sobre esos frames.
