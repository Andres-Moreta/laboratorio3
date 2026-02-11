## 📖 Descripción del Proyecto

Este proyecto aplica técnicas de **Machine Learning No Supervisado** para identificar patrones de comportamiento en usuarios de dispositivos móviles. El objetivo principal es segmentar a los usuarios en grupos diferenciados (clusters) basándose en métricas como tiempo de pantalla, uso de datos y consumo de batería.

Se compararon dos algoritmos principales: **K-Means** y **DBSCAN**, utilizando técnicas de reducción de dimensionalidad (**PCA** y **t-SNE**) para mejorar la precisión y la visualización.

## 📂 El Dataset

El conjunto de datos (`user_behavior_dataset.csv`) contiene información sobre el uso de dispositivos móviles.
* **Instancias:** 700 usuarios.
* **Variables Clave:**
    * `App Usage Time` (min/día)
    * `Screen On Time` (horas/día)
    * `Battery Drain` (mAh/día)
    * `Data Usage` (MB/día)
    * `Age`, `Gender`, `Device Model`, `OS`.

## ⚙️ Metodología

El flujo de trabajo seguido en el notebook (`semana3_Modelos_NoSupervisados_Taller.ipynb`) incluye:

1.  **Limpieza de Datos:** Eliminación de identificadores y codificación de variables categóricas.

2.  **Modelado:**
    * **K-Means:** Se utilizó el *Método del Codo* y el *Coeficiente de Silueta* para determinar el número óptimo de clusters ($k=5$).
    * **DBSCAN:** Clustering basado en densidad para detectar ruido y agrupaciones no esféricas.
3.  **Visualización:** Uso de **t-SNE** para proyectar los clusters en 2D y validar visualmente la separación de los grupos.

## 📊 Resultados y Perfiles Detectados

A través del análisis, se identificaron 3 perfiles de comportamiento principales (agrupados en 5 clusters técnicos):

| Perfil | Tipo de Usuario | Características Promedio |
| :--- | :--- | :--- |
| **Básico** | Light User | ~2.3 hrs pantalla/día, bajo consumo de datos y batería. Usa el móvil para lo esencial. |
| **Moderado** | Average User | ~6.0 hrs pantalla/día, ~1GB datos/día. Usuario estándar de redes y multimedia. |
| **Intensivo** | Power User | **>10 hrs pantalla/día**, ~2GB datos/día. "Gamers" o usuarios con alta dependencia del dispositivo. |
