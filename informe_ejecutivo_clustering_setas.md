# 🧠 Informe Ejecutivo – Proyecto VIII: Aprendizaje No Supervisado sobre el Dataset de Setas

**Fecha:** 28/05/2025  
**Autores:** Equipo de trabajo - Taller de IA y Machine Learning: Andreina Suescum y César Mercado.

---

## 📌 Objetivo del Proyecto

El objetivo principal de este proyecto ha sido aplicar técnicas de aprendizaje **no supervisado** sobre el famoso dataset de hongos del UCI Repository, con el fin de:

- Comprender la estructura de los datos sin necesidad de etiquetas.
- Reducir la dimensionalidad del dataset para su análisis y visualización.
- Identificar posibles agrupaciones naturales en los datos mediante clustering.
- Comparar los resultados no supervisados con un modelo supervisado de referencia.

---

## 🧾 Dataset utilizado

- **Fuente:** [Mushroom Dataset - UCI](https://archive.ics.uci.edu/ml/datasets/Mushroom)
- **Instancias:** 8124 muestras de hongos
- **Características:** 22 columnas categóricas (forma, color, olor, superficie, etc.)
- **Variable objetivo:** `class` → indica si un hongo es comestible (`e`) o venenoso (`p`)

---

## 🔍 Identificación del tipo de problema

La variable `class` contiene etiquetas categóricas (`e`, `p`) que indican si un hongo es comestible o venenoso.

> ✅ Se trata de un problema de **clasificación**, ya que el objetivo es predecir una **categoría**, no una cantidad continua.

Este tipo de problema requiere el uso de algoritmos de clasificación como Random Forest, y permite también evaluar la utilidad de técnicas no supervisadas como clustering.

---

## 🔄 Flujo de trabajo aplicado

1. **Carga y exploración inicial del dataset**

   - Lectura desde URL y asignación de nombres de columna manualmente.
   - Identificación de valores nulos y valores atípicos (`'?'`).

2. **Limpieza y preprocesamiento**

   - Imputación de valores faltantes (`'?'`) con la moda en `stalk-root`.
   - Eliminación de columnas sin variabilidad (`veil-type`).
   - Separación entre variables predictoras (`X`) y variable objetivo (`y`).
   - Codificación de variables categóricas mediante `OneHotEncoder`.

3. **Reducción de dimensionalidad con PCA**

   - Reducción del espacio de +90 dimensiones a 2 componentes principales para visualización.
   - Estudio del número óptimo de componentes a través de rendimiento en Random Forest.

4. **Clasificación supervisada (Random Forest)**

   - Alta precisión (~100%) con pocas componentes tras PCA.
   - Se demuestra que pocas variables concentraban gran parte de la información útil.

5. **Clustering no supervisado (KMeans)**
   - Determinación del número óptimo de clusters con el método del codo (`k=2`).
   - Evaluación visual de la separación de clases reales mediante `catplot`.
   - Visualización en espacio PCA coloreando por clusters.

---

## 📊 Resultados clave

- Con solo **10 componentes principales** (~10% de las variables codificadas), se alcanza **precisión máxima en clasificación supervisada**.
- El algoritmo **KMeans logra separar razonablemente bien las clases**, incluso sin conocer las etiquetas.
- La distribución de clases dentro de cada cluster es **muy clara en la mayoría de los casos**, con ligeras imprecisiones en pocos puntos.

---

## ✅ Conclusiones

- El dataset presenta una **estructura muy bien definida** que puede ser captada con técnicas no supervisadas.
- El uso combinado de **PCA + KMeans** resulta altamente eficaz para visualizar y agrupar datos categóricos de alta dimensión.
- **Random Forest** confirma con datos etiquetados que las decisiones tomadas por clustering no supervisado estaban alineadas con la realidad.
- Este enfoque es muy valioso cuando **no se dispone de etiquetas**, como ocurre en muchos problemas reales.

---

## 🧩 Competencias evaluadas

Según la rúbrica, se han trabajado las siguientes competencias clave:

- ✔️ Limpieza y análisis exploratorio de datos
- ✔️ Codificación de variables categóricas
- ✔️ Uso de PCA y KMeans para agrupación
- ✔️ Comparación entre aprendizaje supervisado y no supervisado
- ✔️ Identificación del tipo de problema (clasificación)
- ✔️ Uso de herramientas de visualización (`seaborn`, `matplotlib`)
- ✔️ Control de versiones y buenas prácticas con GitHub

---
