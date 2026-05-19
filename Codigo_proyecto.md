 Repertorio de Código para Google Colab

Este bloque contiene todas las librerías fundamentales para el Análisis Exploratorio de Datos (EDA). Puedes copiar el bloque completo de la celda de abajo y pegarlo directamente en la primera celda de tu cuaderno de Google Colab.

Bloque de Importación de Librerías

```python
# ==============================================================================
# LIBRERÍAS ESENCIALES PARA ANÁLISIS DE DATOS
# ==============================================================================

# 1. Manipulación y Estructura de Datos
import pandas as pd
import numpy as np

# 2. Visualización Estática y Diagnóstico de Nulos
import seaborn as sns
import matplotlib.pyplot as plt
import missingno as msno

# 3. Visualización Interactiva
import plotly.express as px
import plotly.graph_objects as go

# Configuración de entorno para gráficos
%matplotlib inline
sns.set_theme(style="whitegrid")

print("¡Todas las librerías han sido cargadas con éxito!")

---

 Carga de Archivos desde el Ordenador Local

Este bloque de código es exclusivo para **Google Colab**. Permite abrir una ventana emergente en el navegador para seleccionar y subir cualquier archivo (como tus tablas de Excel `.xlsx` o archivos `.csv`) desde tu computadora directamente al entorno de ejecución.

 Bloque de Código para Colab

```python
# ==============================================================================
# CARGA DE ARCHIVOS LOCALES EN GOOGLE COLAB
# ==============================================================================

from google.colab import files

# Abre el asistente para subir archivos desde tu equipo
uploaded = files.upload()

# Confirma la carga exitosa mostrando el nombre y el tamaño del archivo
for fn in uploaded.keys():
    print(f'User uploaded file "{fn}" with length {len(uploaded[fn])} bytes')
