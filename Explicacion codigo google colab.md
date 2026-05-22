## 🛠️ Guía Paso a Paso del Código de Preprocesamiento

Este script se encarga de estructurar, limpiar y estandarizar la base de datos química antes de realizar cualquier análisis gráfico o estadístico.

### 1. Importación de Librerías y Carga de Archivos
En esta sección se cargan las dependencias esenciales para la manipulación de datos (`pandas`, `numpy`) y visualización (`matplotlib`, `seaborn`). Al estar diseñado para entornos de Google Colab, implementa un módulo interactivo para subir el archivo `.csv` directamente desde el almacenamiento local.

```python
# CARGAR DATOS - Ejecutar siempre al inicio
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from google.colab import files
import io

# Interfaz interactiva para subir el archivo CSV
uploaded = files.upload()

# Lectura del archivo aplicando decodificación utf-8-sig para evitar caracteres extraños (\ufeff)
df = pd.read_csv(io.BytesIO(uploaded[list(uploaded.keys())[0]]), delimiter=';', encoding='utf-8-sig')

# Normalización de los nombres de las columnas eliminando espacios en blanco innecesarios
df.columns = df.columns.str.strip()



## 🔬 Análisis 1: Relación entre Peso Molecular y Punto de Ebullición (Fuerzas de London) 

Este módulo evalúa cuantitativamente cómo influye la masa molecular de los sustratos en sus propiedades macroscópicas térmicas, específicamente el Punto de Ebullición, basándose en los principios de las fuerzas intermoleculares de dispersión de London.

### 1. Filtrado de Datos y Definición de Rangos Fisicoquímicos
Para evitar que valores atípicos (*outliers*) o errores de registro distorsionen la tendencia real, se eliminan las filas con valores nulos en las variables de interés y se delimita el análisis a rangos realistas de síntesis orgánica:
* **Peso Molecular (PM):** 40 a 300 g/mol
* **Punto de Ebullición (PE):** 20 a 400 °C

```python
# Filtrar filas donde existan ambos valores y aplicar máscaras de rango químico
plot_df = df.dropna(subset=['PM_Sustrato', 'PE_Sustrato °C'])
plot_df = plot_df[(plot_df['PM_Sustrato'] >= 40) & (plot_df['PM_Sustrato'] <= 300)]
plot_df = plot_df[(plot_df['PE_Sustrato °C'] >= 20) & (plot_df['PE_Sustrato °C'] <= 400)]
