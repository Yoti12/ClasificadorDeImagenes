## Detector de Ropa en Tiempo Real (YOLOv8 + TensorFlow.js)

Una aplicación web progresiva que utiliza Inteligencia Artificial para detectar y clasificar prendas de ropa (**Suéter, Camiseta, Buso**)
en tiempo real utilizando la cámara web. El modelo corre totalmente en el navegador del cliente sin necesidad de servidores backend.

## 📸 Demostración

<img width="1918" height="954" alt="image" src="https://github.com/user-attachments/assets/0b8fbc94-ee28-4642-9182-dcaf73ad80a3" />


## Características

* **Detección en Tiempo Real:** Uso de la webcam para inferencia instantánea.
* **3 Clases Entrenadas:**
    * 🟥 Suéter
    * 🟩 Camiseta
    * 🟦 Buso
* **Visualización de Confianza:** Gráficas de barras dinámicas que muestran la probabilidad de cada clase en vivo.
* **Privacidad Total:** Todo el procesamiento ocurre en el navegador del usuario usando `TensorFlow.js`; ninguna imagen se envía a la nube.
* **Arquitectura:** Modelo YOLOv8n (Nano) entrenado en Google Colab y exportado a formato TFJS graph model.

## Tecnologías Utilizadas

* **Entrenamiento:** Python, Google Colab, Ultralytics YOLOv8.
* **Web:** HTML5, CSS3 (Bootstrap 5), JavaScript (Vanilla).
* **Librería de IA:** TensorFlow.js (@latest).

## Rendimiento del Modelo

El modelo fue entrenado durante **50 épocas** obteniendo métricas excelentes en el conjunto de validación.

| Métrica | Valor Alcanzado |
| :--- | :--- |
| **mAP50** | 0.995 (Perfecto) |
| **Precisión** | 1.0 |
| **Pérdida (Loss)** | Convergencia estable |

## Gráficas de Entrenamiento
* Graficas de Precisión
<img width="2400" height="1200" alt="Graficas de Precisión" src="https://github.com/user-attachments/assets/e8ce7356-dd74-45b0-8baa-779bacc16d45" />

* Matriz de confusión
  <img width="3000" height="2250" alt="Matriz de confusión" src="https://github.com/user-attachments/assets/746c7e9c-8f53-4f75-992a-bb96ef727008" />

* Validación de Imagenes
  <img width="3000" height="2250" alt="Validación de Imagenes" src="https://github.com/user-attachments/assets/56e0c999-1c3d-47f4-b6d4-c7deba99e6c3" />
  
## Instalación y Uso

Debido a políticas de seguridad de los navegadores, este proyecto **NO FUNCIONA ABRIENDO EL ARCHIVO DIRECTAMENTE** en el archivo `.html`. Necesitas un servidor local.

### Opción A: Visual Studio Code (Recomendado)
1.  Clona o descarga este repositorio.
2.  Abre la carpeta en **VS Code**.
3.  Instala la extensión **Live Server**.
4.  Haz clic derecho en `index.html` y selecciona **"Open with Live Server"**.

### Opción B: Python
Si tienes Python instalado, abre una terminal en la carpeta del proyecto y ejecuta:
```bash
python -m http.server

