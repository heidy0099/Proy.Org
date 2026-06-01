# 📊 PROYECTO 3: DERIVADOS DE ÁCIDOS - ANÁLISIS DE REACCIONES QUÍMICAS

## 📌 Descripción General del Proyecto

Este proyecto comprende el estudio sistemático de **240 reacciones químicas** de derivados de ácidos, incluyendo:

| Grupo Funcional | Código | Cantidad |
|:----------------|:------:|---------:|
| Nitrilos | NIT | 40 |
| Haluros de acilo | HAC | 60 |
| Anhídridos | ANH | 20 |
| Ésteres | EST | 60 |
| Amidas | AMD | 60 |

El objetivo principal es analizar propiedades fisicoquímicas, caracterizar productos y reactivos, y visualizar patrones mediante herramientas computacionales.

---

## 👩‍🔬 Autoras del Proyecto

| Autora | Rol |
|:-------|:----|
| **Heidy Jissel Figueroa Martinez** | Análisis de datos y visualización |
| **Yuly Esperanza Garcia Gonzalez** | Recopilación y organización de datos |
| **Gisell Paola Contreras Lopez** | Documentación y control de calidad |

---

## 🎯 Objetivos del Proyecto

1. **Recopilar y organizar** 240 reacciones de derivados de ácidos en formato estructurado
2. **Registrar propiedades fisicoquímicas** de sustratos y productos
3. **Realizar análisis gráfico** utilizando librerías Python en Google Colab
4. **Evaluar correlaciones** entre variables clave (PM, PE, pKa, LD50)
5. **Clasificar riesgos** toxicológicos y ambientales por grupo funcional

---

## 📁 Estructura del Repositorio

---

## 📂 Descripción Detallada de Carpetas y Archivos

### 📄 **Archivos Raíz**

| Archivo | Versión | Propósito |
|:--------|:--------|:----------|
| **LEAME.md** | Final | Documentación principal en español del proyecto |
| **README.md** | Alternativa | Versión complementaria del README |
| **Observaciones.ipynb** | Notebook | Registro de observaciones y hallazgos durante el análisis |

### 📂 **CODIGOS/ - Scripts y Notebooks**

Esta carpeta contiene todas las versiones del código desarrollado durante el proyecto:

| Archivo | Versión | Descripción |
|:--------|:--------|:------------|
| **Borrador_codigo_graficos.ipynb** | Borrador | Primer intento de generación de gráficos con matplotlib/seaborn |
| **CÓDIGO** | Base | Script principal en formato plano |
| **Explicacion_codigo_Final.md** | Documentación | Explicación detallada del funcionamiento del código final |
| **PROYECTO_3_DERIVADOS_DE_ACIDO.ipynb** | ✅ Final | Notebook completo con análisis final y gráficos interactivos (Plotly) |

**Evolución del código:**
1. `Borrador_codigo_graficos.ipynb` → Pruebas iniciales con matplotlib
2. `CÓDIGO` → Versión base funcional
3. `PROYECTO_3_DERIVADOS_DE_ACIDO.ipynb` → ✅ Versión final con Plotly y dashboard interactivo

### 📂 **ESTRUCTURA/ - Documentación Metodológica**

| Archivo | Propósito |
|:--------|:----------|
| **ESTRUCTURA DEL PROYECTO.md** | Metodología completa, criterios de análisis, matriz de correlaciones y tipos de gráficos |

### 📂 **TABLA DE DATOS/ - Bases de Datos**

Esta carpeta contiene todas las versiones de la base de datos a lo largo del proyecto:

| Archivo | Versión | Estado | Descripción |
|:--------|:--------|:------|:------------|
| **Proyecto 3 Química Orgánica versión inicial.xlsx** | v1.0 | 📄 Histórico | Recopilación inicial de datos sin procesar |
| **Proyecto 3 Química Orgánica.csv** | v1.5 | 📄 Intermedio | Exportación CSV para pruebas en Python |
| **Proyecto DATOS PROCESADOS.xlsx** | v2.0 | 📄 Procesado | Datos con limpieza y estandarización |
| **Proyecto 3 Quimica Organica TRATAMIENTO FINAL.xlsx** | v3.0 | ✅ Final | Versión definitiva con 242 registros y 49 columnas |

---

## 📊 Matriz de Correlaciones y Análisis Gráficos

A continuación se presentan los **11 análisis gráficos** realizados, su propósito químico y el tipo de visualización utilizada:

### 📈 Análisis de Propiedades Fisicoquímicas

| # | Variable X | Variable Y | Propósito del Análisis | Tipo de Gráfico |
|:-:|:-----------|:-----------|:-----------------------|:----------------|
| 1 | **PM_Sustrato** | **PE_Sustrato** | **Evaluar las Fuerzas de Dispersión de London:** Demuestra cómo al aumentar la masa molar y el tamaño de la cadena de carbonos, se incrementa la polarizabilidad de la molécula, requiriendo mayor energía térmica (temperatura) para pasar al estado gaseoso. | 📈 Gráfico de Dispersión (X vs Y) |
| 2 | **Grupo Funcional** | **PE_Sustrato** | **Comparar Fuerzas Intermoleculares por Familia:** Permite analizar por qué compuestos con pesos similares tienen ebulliciones tan distintas. Demuestra que las amidas hierven a mayor temperatura que los nitrilos porque forman redes de **puentes de hidrógeno**, mientras que los nitrilos solo experimentan fuerzas dipolo-dipolo. | 📦 Gráfico de Cajas (Boxplot) |
| 3 | **Grupo Funcional** | **pKa_Sustrato** | **Analizar la Reactividad y Estabilidad por Resonancia:** Evalúa la acidez relativa de los sustratos. Valores altos de pKa en amidas demuestran que el par de electrones del nitrógeno está deslocalizado por el grupo carbonilo (C=O), explicando por qué son los derivados de ácido más estables y menos reactivos. | 📊 Gráfico de Barras |
| 4 | **Grupo Funcional** | **LD50_Sustrato** | **Evaluación de Riesgo Ambiental y Toxicidad:** Clasifica el perfil de peligro biológico de las familias químicas en el laboratorio. Permite discutir los riesgos de manejo (como la potencial liberación metabólica de iones cianuro CN⁻ en ciertos nitrilos) frente a la estabilidad de las amidas. | 📊 Gráfico de Barras |


---

### 🔬 Análisis de Reactividad, Síntesis y Procesos

| # | Variable X | Variable Y | Propósito del Análisis | Tipo de Gráfico |
|:-:|:-----------|:-----------|:-----------------------|:----------------|
| 6 | **Tipo_Reaccion** | **PM_Producto** o **PE_Producto** | **Efecto del Mecanismo en las Propiedades del Producto:** Permite evaluar si ciertos tipos de reacción (como una Reducción con LiAlH₄ frente a una Hidrólisis) tienden a generar sistemáticamente productos más ligeros o volátiles, mapeando la eficiencia promedio de las transformaciones sintéticas. | 📊 Gráfico de Barras (Promedios/Medianas) |
| 7 | **Nombre_Reaccion** | **Nombre_Solvente 1** | **Análisis de Toxicidad, Criticidad y Sostenibilidad de Solventes:** Evalúa qué tipos de reacciones químicas conllevan un mayor riesgo ambiental y operativo en función del puntaje de criticidad de sus medios de reacción. | 📊 Gráfico de Barras Agrupadas |
| 8 | **Tipo_Reaccion** | **Tipo_Solvente** | **Clasificación Ecológica y de Seguridad por Tipo de Proceso:** Evalúa si ciertos mecanismos (sustituciones, adiciones, etc.) dependen críticamente de solventes según su naturaleza (ej. polares próticos, polares apróticos, apolares). Permite analizar el impacto ambiental global de cada categoría de reacción y planificar la sustitución sistemática hacia medios de reacción más limpios o reutilizables. | 📊 Gráfico de Barras Apiladas o Gráfico de Mosaico |
| 9 | **pKa_Sustrato** | **pKa_Producto** | **Evaluación del Cambio de Acidez en la Reacción:** Muestra el salto de pH y reactividad antes y después del proceso químico. Por ejemplo, cómo un nitrilo o amida se transforma en una amina o ácido carboxílico, alterando el carácter ácido-base del sistema. | 📈 Gráfico de Dispersión o Gráfico de Líneas Correlativas |
| 10 | **Nombre_Catalizador 1** | **Cantidad_Veces_Utilizado** | **Análisis de Recurrencia y Optimización del Medio:** Identifica cuáles agentes catalíticos específicos son los más empleados a lo largo del proyecto para acelerar las transformaciones químicas. Este conteo de frecuencia es clave para priorizar estudios de costos, evaluar la viabilidad de recuperación/reciclaje del catalizador y optimizar las condiciones estándar del proceso. | 📊 Gráfico de Barras Simples (Ordenado de mayor a menor) o Gráfico de Pareto |
| 11 | **LD50_Reactivos** | **LD50_Productos** | **Variación del Perfil de Toxicidad y Seguridad del Proceso:** Evalúa el cambio en la dosis letal media de los grupos funcionales (LD50) antes y después de la reacción. Su propósito es determinar si el proceso incrementa el riesgo químico o si, por el contrario, se avanza hacia productos más seguros y biocompatibles, lo cual es crítico para el diseño de protocolos de seguridad industrial, manejo de residuos y regulaciones ambientales. | 📊 Gráfico de Barras (Comparativo o de Diferencias) |

---

## 📊 Tipos de Gráficos Utilizados y su Propósito

| Tipo de Gráfico | Cuándo se usa | Ejemplo en el proyecto |
|:----------------|:--------------|:----------------------|
| **Gráfico de Dispersión (Scatter)** | Para mostrar correlación entre dos variables numéricas | PM vs PE |
| **Boxplot (Diagrama de Cajas)** | Para comparar distribuciones entre categorías | Grupo Funcional vs PE |
| **Gráfico de Barras** | Para comparar valores entre categorías | Grupo Funcional vs pKa |
| **Gráfico de Barras Agrupadas** | Para comparar múltiples variables por categoría | Nombre_Reacción vs Solvente |
| **Gráfico de Barras Apiladas** | Para mostrar composición relativa | Tipo_Reacción vs Tipo_Solvente |
| **Gráfico de Pareto** | Para identificar causas más frecuentes | Catalizador vs Frecuencia |
| **Gráfico de Torta (Pie Chart)** | Para mostrar proporciones de un todo | Distribución de grupos funcionales |
| **Gráfico de Líneas** | Para mostrar tendencias o cambios | pKa_Sustrato vs pKa_Producto |
| **Heatmap (Mapa de Calor)** | Para visualizar matrices de correlación | Correlación entre variables numéricas |
| **Histograma** | Para mostrar distribución de una variable | Distribución de Temperatura |
| **Violin Plot** | Para mostrar distribución y densidad | Temperatura por Función Química |

---

## 🔍 Interpretación de Variables Clave

| Variable | Significado Químico | Rango Típico | Interpretación |
|:---------|:--------------------|:-------------|:---------------|
| **Peso Molecular (PM)** | Masa molar del compuesto | 50-500 g/mol | Mayor PM = mayor punto de ebullición |
| **Punto de Ebullición (PE)** | Temperatura de cambio de fase | 0-300°C | Mayor PE = fuerzas intermoleculares más fuertes |
| **pKa** | Constante de acidez | -2 a 50 | Menor pKa = ácido más fuerte |
| **LD50** | Toxicidad aguda (dosis letal media) | 1-5000 mg/kg | Menor LD50 = más tóxico |
| **Densidad** | Masa por unidad de volumen | 0.5-2.5 g/mL | >1 g/mL = más denso que el agua |

### 📊 Rangos de Interpretación de LD50 (Toxicidad)

| LD50 (mg/kg) | Clasificación | Manejo Recomendado |
|:-------------|:--------------|:-------------------|
| < 5 | ⚠️ **Súper tóxico** | Campana de extracción, traje de protección |
| 5 - 50 | ⚠️ **Altamente tóxico** | Guantes, gafas, campana |
| 50 - 500 | ⚠️ **Moderadamente tóxico** | Precaución estándar |
| 500 - 5000 | ✅ **Ligeramente tóxico** | Manejo normal con cuidado |
| > 5000 | ✅ **Prácticamente no tóxico** | Manejo estándar |

---

## 📁 ¿PARA QUÉ SIRVE LA CARPETA DEL DICCIONARIO?

### 🎯 PROPÓSITO PRINCIPAL:
La carpeta del **diccionario** actúa como una **"guía de referencia rápida"** para entender las columnas del dataset sin tener que revisar el archivo original cada vez.

---

### 📋 ¿QUÉ CONTIENE ESTA CARPETA?

| Archivo | Propósito | Cuándo usarlo |
|---------|-----------|---------------|
| `diccionario_columnas.md` | Explicación de CADA columna | Al inicio del proyecto |
| `diccionario_abreviaturas.md` | Significado de siglas (PM, PE, pKa, etc.) | Cuando aparecen abreviaturas |
| `mapeo_columnas.json` | Relación nombre técnico ↔ nombre amigable | Para generar gráficos automáticos |
| `unidades_medida.txt` | Unidades de cada variable | Para etiquetar ejes correctamente |
| `tipos_de_datos.csv` | Qué columnas son numéricas/categóricas | Para elegir análisis apropiados |

---

### 🔧 ¿PARA QUÉ SIRVE CADA ARCHIVO?

#### 1. **diccionario_columnas.md**
```markdown
| Columna | Significado | Tipo | Unidad |
|---------|-------------|------|--------|
| PMS     | Peso Molecular | Numérico | g/mol |
| PES     | Punto Ebullición | Numérico | °C |
| pKa S   | Constante acidez | Numérico | pH |
| GF      | Grupo funcional | Categórico | - |
