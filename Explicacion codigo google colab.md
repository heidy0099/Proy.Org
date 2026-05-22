## 🛠️ Guía Paso a Paso del Código de Preprocesamiento

Este script se encarga de estructurar, limpiar y estandarizar la base de datos química antes de realizar cualquier análisis gráfico o estadístico.

### 1. Importación de Librerías y Carga de Archivos
En esta sección se cargan las dependencias esenciales para la manipulación de datos (`pandas`, `numpy`) y visualización 
(`matplotlib`, `seaborn`). Al estar diseñado para entornos de Google Colab, implementa 
un módulo interactivo para subir el archivo `.csv` directamente desde el almacenamiento local.

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

Este módulo evalúa cuantitativamente cómo influye la masa molecular de los sustratos en sus propiedades
macroscópicas térmicas (Punto de Ebullición), basándose en los principios de las fuerzas
intermoleculares de dispersión de London.

### 🧱 Paso 1: Filtrado y Control de Calidad de Datos

##df.dropna(...) elimina del análisis cualquier fila que no tenga registrado
el Peso Molecular o el Punto de Ebullición, evitando que el script falle por datos ausentes.
```python
plot_df = df.dropna(subset=['PM_Sustrato', 'PE_Sustrato °C'])
plot_df = plot_df[(plot_df['PM_Sustrato'] >= 40) & (plot_df['PM_Sustrato'] <= 300)]
plot_df = plot_df[(plot_df['PE_Sustrato °C'] >= 20) & (plot_df['PE_Sustrato °C'] <= 400)]

### 🧱 Paso 2:
np.polyfit(..., 1) calcula mediante el método de mínimos cuadrados la ecuación de la línea recta
($y = mx + b$) que mejor representa la tendencia de los datos. Extrae la pendiente
($m$, que indica cuántos grados Celsius aumenta el PE por cada g/mol de masa) y la ordenada al origen
($b$).
z = np.polyfit(plot_df['PM_Sustrato'], plot_df['PE_Sustrato °C'], 1)
p = np.poly1d(z)
x_line = np.linspace(plot_df['PM_Sustrato'].min(), plot_df['PM_Sustrato'].max(), 100)
