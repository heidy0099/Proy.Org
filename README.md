#  Reacciones de Derivados de Ácidos

Descripción
Estudio de 240 reacciones químicas de derivados de ácidos: nitrilos, haluros de acilo, anhídridos, ésteres y amidas. En donde se incluye el  análisis de propiedades fisicoquímicas, caracteristicas especificas de productos y reactivos y visualización de datos con Python.

 Autoras
- Heidy Jissel Figueroa Martinez
- Yuly Esperanza Garcia Gonzalez
- Gisell Paola Contreras Lopez

Objetivos
- Recopilar y organizar 240 reacciones de derivados de ácidos
- Registrar propiedades fisicoquímicas de sustratos y productos
- Realizar análisis gráfico con librerías Python en Google Colab

Grupos Funcionales
| ID | Grupo Funcional | Cantidad |
|----|----------------|----------|
| NIT | Nitrilos | 40 |
| HAC | Haluros de acilo | 60 |
| ANH | Anhídridos | 20 |
| EST | Ésteres | 60 |
| AMD | Amidas | 60 |

Columnas de la Tabla
- ID de reacción
- Grupo funcional
- Función química
- Nombre y Fórmula del sustrato
- Peso molecular (sustrato y producto)
- Punto de ebullición e incertidumbre (sustrato y producto)
- Densidad e incertidumbre (sustrato y producto)
- pKa e incertidumbre (sustrato y producto)
- LD50 en mamíferos (sustrato y producto)
- Reactivo, catalizador, solvente, medio
- Producto
- Tipo y nombre de la reacción

Herramientas
- Microsoft Excel / Google Sheets
- Python (pandas, matplotlib, seaborn)
- Google Colab / Jupyter Notebook
- CAS-SciFinder (fuente de datos numéricos)
- GitHub (control de versiones)


---

### Matriz de Correlación de Variables y Criterios Gráficos

| Variable X vs Variable Y | Propósito del Análisis (¿Para qué se evalúa?) | Tipo de Gráfico a Usar |
| :--- | :--- | :--- |
| **PM_Sustrato** <br>vs<br> **PE_Sustrato** | **Evaluar las Fuerzas de Dispersión de London:** Demuestra cómo al aumentar la masa molar y el tamaño de la cadena de carbonos, se incrementa la polarizabilidad de la molécula, requiriendo mayor energía térmica (temperatura) para pasar al estado gaseoso. | **Gráfico de Dispersión (X vs Y)** |
| **Grupo Funcional** <br>vs<br> **PE_Sustrato** | **Comparar Fuerzas Intermoleculares por Familia:** Permite analizar por qué compuestos con pesos similares tienen ebulliciones tan distintas. Demuestra que las amidas hierven a mayor temperatura que los nitrilos porque forman redes de **puentes de hidrógeno**, mientras que los nitrilos solo experimentan fuerzas dipolo-dipolo. | **Gráfico de Cajas (Boxplot)** |
| **Grupo Funcional** <br>vs<br> **pKa_Sustrato** | **Analizar la Reactividad y Estabilidad por Resonancia:** Evalúa la acidez relativa de los sustratos. Valores altos de pKa en amidas demuestran que el par de electrones del nitrógeno está deslocalizado por el grupo carbonilo ($C=O$), explicando por qué son los derivados de ácido más estables y menos reactivos. | **Gráfico de Cajas (Boxplot)** |
| **Grupo Funcional** <br>vs<br> **LD50_Sustrato** | **Evaluación de Riesgo Ambiental y Toxicidad:** Clasifica el perfil de peligro biológico de las familias químicas en el laboratorio. Permite discutir los riesgos de manejo (como la potencial liberación metabólica de iones cianuro $\text{CN}^-$ en ciertos nitrilos) frente a la estabilidad de las amidas. | **Gráfico de Cajas (Boxplot)** |
| **Grupo Funcional** <br>vs<br> **ID / Conteo** | **Análisis de Distribución de la Muestra:** Sirve para caracterizar la base de datos de tu proyecto. Muestra visualmente la cantidad de muestras y la representatividad (porcentaje de participación) de cada familia química dentro del estudio. | **Gráfico de Barras o Torta** |

### Matriz Avanzada: Análisis de Reactividad, Síntesis y Procesos

| Variable X vs Variable Y | Propósito del Análisis (¿Para qué se evalúa?) | Tipo de Gráfico a Usar |
| :--- | :--- | :--- |
| **Tipo_Reaccion** <br>vs<br> **PM_Producto** o **PE_Producto** | **Efecto del Mecanismo en las Propiedades del Producto:** Permite evaluar si ciertos tipos de reacción (como una Reducción con $LiAlH_4$ frente a una Hidrólisis) tienden a generar sistemáticamente productos más ligeros o volátiles, mapeando la eficiencia de las transformaciones sintéticas. | **Gráfico de Cajas (Boxplot)** |
| **Nombre_Reaccion** <br>vs<br> **Nombre_Solvente 1** | **Análisis de Compatibilidad y Sostenibilidad de Solventes:** Evalúa qué solventes (ej. Éter dietílico, Benceno, Agua) se usan más según cada reacción. En ingeniería ambiental, esto sirve para discutir la sustitución de solventes tóxicos o aromáticos por alternativas más verdes. | **Gráfico de Barras Agrupadas** |
| **pKa_Sustrato** <br>vs<br> **pKa_Producto** | **Evaluación del Cambio de Acidez en la Reacción:** Muestra el salto de pH y reactividad antes y después del proceso químico. Por ejemplo, cómo un nitrilo o amida (con pKa específicos) se transforma en una amina o ácido carboxílico, alterando el carácter ácido-base del sistema. | **Gráfico de Dispersión (X vs Y)** o **Gráfico de Líneas Correlativas** |
| **Nombre_Catalizador 1** <br>vs<br> **ID / Conteo de Reacciones** | **Evaluación de Eficiencia Catalítica del Proceso:** Identifica cuáles catalizadores o condiciones de medio son los más recurrentes en el proyecto para acelerar los mecanismos de sustitución o adición nucleofílica, permitiendo discutir los costos y la viabilidad del proceso. | **Gráfico de Barras** o **Gráfico de Torta** |

Estructura del Repositorio
Proy.Org/

├── README.md

├── tabla_reacciones.xlsx

├── tabla_explicacion_analisis_grafico.xlsx

└── Codigo_analisis_grafico.ipynb

