# 📘 Proyecto Integrador — Visión por Computador y EDA

Este repositorio contiene el análisis exploratorio de datos (**EDA**) aplicado a un dataset de imágenes multiformato para tareas de **clasificación, detección y segmentación**, desarrollado como parte del proyecto integrador de la Maestría en Inteligencia Artificial.

---

## 📂 Estructura del dataset
- **Clasificación**: imágenes organizadas en carpetas por clase (`OK_tipo1`, `NG_tipo2`, etc.).  
- **Detección (YOLO)**: imágenes con anotaciones `.txt` (coordenadas normalizadas).  
- **Segmentación**: imágenes `.jpg` y máscaras asociadas `.png`.  
- Resolución estándar: **640x640 píxeles**.  

---

## 🔎 Análisis Exploratorio (EDA)

### 1. Clasificación
- Se detectó un **desbalance de clases** (más ejemplos en *OK* que en *NG*).  
- Variables analizadas: `file_size`, `brightness`, `mean_r/g/b`, `blur_var`.  
- **Alta correlación** entre canales RGB y brillo → redundancia de variables.  
- **Desenfoque (`blur_var`)**: variable clave para distinguir defectos.  

### 2. Segmentación
- Dataset con **80 imágenes y sus máscaras**.  
- Homogeneidad en colorimetría (valores medios 165–177).  
- Se identificaron **imágenes con alto desenfoque** (>45), posibles problemas de captura.  
- Las máscaras permiten entrenar modelos supervisados (U-Net, Mask R-CNN).  

### 3. Visualizaciones
- Histogramas de distribución de clases.  
- Gráficos de conteo y ejemplos de imágenes.  
- Heatmap de correlaciones entre variables.  

---

## 💡 Insights principales
1. El dataset está **bien estructurado pero desbalanceado**.  
2. Es necesario aplicar **data augmentation** en clases NG.  
3. Requiere **normalización de iluminación y brillo**.  
4. El **desenfoque** es un predictor importante de defectos.  
5. Las **máscaras añaden valor** para segmentación supervisada.  

---
<img width="1047" height="562" alt="image" src="https://github.com/user-attachments/assets/409c8f93-5046-4b0f-b4f9-f7c3341b0e8d" />


## ✅ Conclusiones
- El dataset es adecuado como base experimental, pero necesita **ajustes previos al modelado**.  
- Se recomienda:
  - Balanceo de clases.  
  - Reducción de colinealidad (ej. PCA).  
  - Normalización de iluminación.  
  - Augmentations en brillo, contraste y nitidez.  

El EDA realizado constituye una etapa crítica que orienta el pipeline de visión por computador hacia modelos más robustos y generalizables.  

---

## 👥 Autores
- **David Alejandro Narváez Mejia** — Maestría en IA  
- **Francisco Javier Estupiñan Andrade** — Maestría en IA  
