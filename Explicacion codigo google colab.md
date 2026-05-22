Guia Paso a Paso del Codigo de Analisis Quimico
Explicacion General
Este script analiza datos quimicos de sustratos y productos, incluyendo propiedades como peso molecular, punto de ebullicion, pKa, toxicidad (LD50), y relaciones con grupos funcionales, tipos de reaccion, solventes y catalizadores.

Tabla de Contenidos
Importacion de Librerias y Carga de Datos

Analisis 1: PM vs PE (Fuerzas de Dispersion)
Analisis 2: Boxplot por Grupo Funcional
Analisis 3: pKa por Grupo Funcional
Analisis 4: Toxicidad LD50
Analisis 5: Distribucion de la Muestra
Analisis 6: PM Producto por Reaccion
Analisis 7: Criticidad de Solventes
Analisis 8: Clasificacion Ecologica
Analisis 9: Cambio de Acidez
Analisis 10: Catalizadores (Pareto)
Analisis 11C: Perfil de Toxicidad

Paso 1: Importacion de Librerias y Carga de Datos {#paso-1}
# CARGAR DATOS - Ejecutar siempre al inicio
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from google.colab import files
import io

# Interfaz interactiva para subir el archivo CSV
uploaded = files.upload()

# Lectura del archivo con separador punto y coma
df = pd.read_csv(io.BytesIO(uploaded[list(uploaded.keys())[0]]), 
                 delimiter=';', 
                 encoding='utf-8-sig')

# Limpiar nombres de columnas (eliminar espacios al inicio/final)
df.columns = df.columns.str.strip()

print(f"Archivo cargado: {len(df)} filas, {len(df.columns)} columnas")
print(f"Columnas disponibles: {list(df.columns)}")

Explicacion:

Importa las librerias necesarias para analisis de datos y graficos

Sube un archivo CSV desde el ordenador local

Lee el archivo con separador punto y coma (;)

Limpia los nombres de las columnas eliminando espacios en blanco

Para modificar:

Cambiar delimiter=';' a delimiter=',' si el archivo usa comas

Cambiar encoding='utf-8-sig' a encoding='latin-1' si hay problemas con caracteres
