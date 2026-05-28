
---

## 📂 Descripción Detallada de Carpetas y Archivos

### 1. 📄 **README.md**
- **Contenido:** Documentación principal del proyecto
- **Propósito:** Guía completa para entender, navegar y ejecutar el proyecto
- **Incluye:** Objetivos, estructura, instrucciones de uso y análisis esperados

### 2. 📊 **tabla_reacciones.xlsx**
- **Contenido:** Base de datos principal con 242 registros y 49 columnas
- **Columnas principales:**
  - `ID` - Identificador único de reacción
  - `Grupo Funcional` - Clasificación química (NIT, HAC, ANH, EST, AMD)
  - `Función química` - Rol del compuesto en la reacción
  - `Nombre_Sustrato` / `Formula_Sustrato` - Identificación del reactivo
  - `Peso molecular` - Masa molar (sustrato y producto)
  - `Punto de ebullición` - Temperatura de cambio de fase
  - `Densidad` - Masa por unidad de volumen
  - `pKa` - Constante de acidez
  - `LD50` - Toxicidad aguda en mamíferos
  - `Reactivo`, `Catalizador`, `Solvente`, `Medio`
  - `Producto` - Compuesto resultante
  - `Tipo de reacción` / `Nombre de la reacción`

### 3. 📋 **tabla_explicacion_analisis_grafico.xlsx**
- **Contenido:** Matriz de análisis con 11 correlaciones clave
- **Columnas:**
  - Variable X vs Variable Y
  - Propósito del análisis (contexto químico)
  - Tipo de gráfico recomendado
- **Análisis incluidos:**
  1. PM vs PE → Fuerzas de London
  2. Grupo Funcional vs PE → Fuerzas intermoleculares
  3. Grupo Funcional vs pKa → Reactividad por resonancia
  4. Grupo Funcional vs LD50 → Riesgo ambiental
  5. Grupo Funcional vs Conteo → Distribución muestral
  6. Tipo_Reaccion vs PM_Producto → Eficiencia sintética
  7. Nombre_Reaccion vs Solvente → Sostenibilidad
  8. Tipo_Reaccion vs Tipo_Solvente → Clasificación ecológica
  9. pKa_Sustrato vs pKa_Producto → Cambio de acidez
  10. Catalizador vs Frecuencia → Optimización de procesos
  11. LD50_Reactivos vs LD50_Productos → Perfil de toxicidad

### 4. 📓 **Codigo_analisis_grafico.ipynb**
- **Contenido:** Notebook de Python para análisis interactivo
- **Librerías utilizadas:**
  - `pandas` - Manipulación de datos
  - `numpy` - Cálculos numéricos
  - `plotly` - Gráficos interactivos
  - `matplotlib` / `seaborn` - Visualización estática
- **Funcionalidades:**
  - Carga automática de CSV
  - Generación de gráficos interactivos
  - Dashboard completo de análisis
  - Resumen ejecutivo automático

### 5. 📂 **CODIGOS/**
- **Contenido:** Scripts adicionales y versiones alternativas
- **Propósito:** Almacenar código complementario y experimentos

### 6. 📂 **ESTRUCTURA/**
- **Contenido:** Documentos de planificación y metodología
- **Propósito:** Registrar criterios de análisis y organización del proyecto

---
## 📊 Resultados Esperados

- ✅ **Matriz de correlaciones** entre propiedades fisicoquímicas
- ✅ **Clasificación de toxicidad** por grupo funcional
- ✅ **Optimización de condiciones** de reacción
- ✅ **Dashboard interactivo** para exploración de datos
- ✅ **Recomendaciones** para manejo seguro de reactivos

---

## 🔍 Interpretación de Variables Clave

| Variable | Significado Químico | Rango Típico |
|:---------|:--------------------|:-------------|
| **Peso Molecular (PM)** | Masa molar del compuesto | 50-500 g/mol |
| **Punto de Ebullición (PE)** | Temperatura de cambio de fase | 0-300°C |
| **pKa** | Constante de acidez | -2 a 50 |
| **LD50** | Toxicidad aguda | 1-5000 mg/kg |
| **Densidad** | Masa por unidad de volumen | 0.5-2.5 g/mL |

---

## 📈 Ejemplo de Interpretación

| Variable | Valor Bajo | Valor Alto | Implicación |
|:---------|:-----------|:-----------|:-------------|
| **PM** | < 100 g/mol | > 300 g/mol | Compuestos más volátiles | Compuestos más pesados |
| **PE** | < 50°C | > 200°C | Líquido volátil | Sólido estable |
| **pKa** | < 0 | > 20 | Ácido fuerte | Base fuerte |
| **LD50** | < 50 mg/kg | > 2000 mg/kg | ⚠️ Altamente tóxico | ✅ Baja toxicidad |
| **Densidad** | < 1 g/mL | > 1 g/mL | Flota en agua | Hunde en agua |


### Paso 1: Clonar o Descargar el Repositorio
```bash
git clone https://github.com/heidy0099/Proy.Org.git
