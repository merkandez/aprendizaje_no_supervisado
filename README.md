# 🍄 Taller de Aprendizaje Automático No Supervisado con el Dataset de Setas

Este repositorio contiene un taller práctico orientado al aprendizaje automático **no supervisado**, usando técnicas de **PCA** y **Clustering (KMeans)**, junto con una comparativa con un modelo supervisado (Random Forest).

Usaremos el **Mushroom Dataset**, un conjunto de datos muy conocido en el ámbito educativo que contiene información sobre diferentes tipos de hongos, incluyendo su clasificación como **comestibles o venenosos**.

---

## 📂 Dataset

Puedes obtener el dataset desde el siguiente enlace:

🔗 [Mushroom Dataset - UCI Repository](https://archive.ics.uci.edu/ml/datasets/Mushroom)

- **Instancia:** Cada fila representa un hongo.
- **Variables:** Todas son **categóricas** (forma, color, olor, etc.).
- **Variable objetivo (`class`)**: Binaria — `e` (edible/comestible) o `p` (poisonous/venenoso).

---

## 🧠 Objetivos del taller

- Cargar y explorar un dataset categórico complejo.
- Tratar valores nulos y eliminar columnas no informativas.
- Codificar variables categóricas usando **One-Hot Encoding**.
- Reducir dimensionalidad con **PCA (Análisis de Componentes Principales)**.
- Aplicar **K-Means Clustering** para detectar estructuras ocultas en los datos.
- Comparar el rendimiento del modelo no supervisado con un modelo supervisado (**Random Forest**).

---

## 🔧 Tecnologías utilizadas

- Python
- Pandas / NumPy
- Seaborn / Matplotlib
- Scikit-learn (`PCA`, `KMeans`, `RandomForestClassifier`)

---

## 🗂️ Contenido del notebook

### 1. 📥 Carga y exploración de datos
- Visualización general del dataset.
- Conteo de valores nulos y valores únicos por variable.
- Eliminación de columnas constantes o poco informativas.

### 2. 🧼 Preprocesamiento
- Imputación o eliminación de valores faltantes.
- Conversión de variables categóricas con **OneHotEncoder**.
- Separación entre `X` (features) e `y` (class).

### 3. 🧪 PCA (Análisis de Componentes Principales)
- Reducción de dimensionalidad a 2 componentes.
- Visualización de los datos en 2D.
- Evaluación visual de separabilidad.

### 4. 🌳 Clasificación supervisada (Random Forest)
- Entrenamiento de un modelo de clasificación.
- Evaluación con métricas de precisión.
- Estudio del impacto del número de componentes en el rendimiento del modelo.

### 5. 🔍 Clustering con K-Means
- Determinación del número óptimo de clusters (método del codo).
- Entrenamiento y visualización de clusters.
- Evaluación de la correspondencia entre clusters y clases reales (sin usar las etiquetas).


---

## 📊 Evaluación  

Se considerarán los siguientes criterios:  

Competencia:  Evaluar conjuntos de datos utilizando herramientas de análisis y de visualización de datos
  
✅ Uso y gestión de formato .csv  
✅ Limpieza y preprocesado de datos  
✅ Visualización de datos (seaborn, matplotlib, plotly)  
✅ Análisis exploratorio detallado (EDA)  
✅ Uso de técnicas de preprocesado (normalización, escalado, label encoder, one hot encoder)    
✅ Uso de técnicas avanzadas de limpieza de datos (eliminación de valores atípicos, imputación de valores faltantes)  
✅ Uso de técnicas de reducción de dimensionalidad (PCA, t-SNE)   
  

Competencia:  Aplicar algoritmos de aprendizaje automático según el problema, identificando y resolviendo problemas clásicos de inteligencia artificial:

✅ Seleccionar las variables que son útiles y las que no lo son  
✅ Reconocer un caso de aprendizaje no supervisado   
✅ Aplicar modelos de clustering  
✅ Reconocer si es un problema de regresión o de clasificación      
✅ Separación de datos en train/test  
✅ Uso modelos de ensemble (RandomForest, GradientBoosting, AdaBoost, XGBoost, LightGBM)  
  
Más detalles en: [roadmap-mad-ai-p4.coderf5.es](https://roadmap-mad-ai-p4.coderf5.es/)  






