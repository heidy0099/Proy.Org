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
