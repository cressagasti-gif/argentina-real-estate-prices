<h1 align="center">Argentina Real Estate Prices</h1>
<p align="center">
  <b>Data Science · Pandas · NumPy · Matplotlib · scikit-learn</b><br>
  End-to-end price analysis and linear-regression baseline on Argentine property listings
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&labelColor=0D0D0D">
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&labelColor=0D0D0D">
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&labelColor=0D0D0D">
  <img src="https://img.shields.io/badge/Matplotlib-3F4F75?style=for-the-badge&labelColor=0D0D0D">
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&labelColor=0D0D0D">
</p>

---

## EN

**What key factors drive property sale prices in Argentina?**

An end-to-end data science exercise on a real Kaggle dataset of Argentine real
estate listings. The notebook takes raw scraped data through cleaning, feature
engineering, exploratory analysis and visualisation, and finishes with a linear
regression baseline — reporting its limitations honestly rather than overselling
the result.

### What it does

- **Loads** the Properati Argentina dataset directly from Kaggle via `kagglehub`
- **Cleans** the data: drops duplicates, handles outliers, and filters listings
  down to properties actually *for sale* and priced in *USD*
- **Engineers** a `price_per_m2` column (price ÷ covered surface)
- **Explores** with descriptive statistics (mean, median, standard deviation)
- **Visualises** average price by locality, price vs. surface area, and a
  side-by-side subplot comparing **CABA** (City of Buenos Aires) against
  **Gran Buenos Aires**
- **Models** a `LinearRegression` that predicts price from covered surface in
  CABA

### Results and honest limitations

The model reaches **R² ≈ 0.27**. That is a *weak* fit, and the notebook says so
plainly: covered surface alone explains only a fraction of the price variance in
this market. The write-up frames it as a coherent trend and a reasonable first
estimate, not a predictive model — and points at location and dispersion as the
dominant source of the remaining variance.

**This is the most important thing in the repo.** A weak baseline documented with
integrity is worth more than a high score with no explanation.

### How to run

```bash
pip install pandas numpy matplotlib scikit-learn kagglehub jupyter
jupyter notebook Proyecto_DATASET.ipynb
```

The first cell downloads the dataset from Kaggle automatically.

### Project structure

The notebook is organised in parts:

| Part | Contents |
|---|---|
| 1 | Dataset loading |
| 2 | NumPy & Pandas |
| 3 | Data cleaning |
| 4 | Feature engineering |
| 5 | Exploratory analysis & visualisation |
| 6 | Linear regression model |

### Dataset

[`alejandroczernikier/properati-argentina-dataset`](https://www.kaggle.com/datasets/alejandroczernikier/properati-argentina-dataset)
— credited to its original author; used here for educational purposes.

---

## ES

**¿Qué factores determinan el precio de venta de propiedades en Argentina?**

Ejercicio completo de ciencia de datos sobre un dataset real de publicaciones
inmobiliarias argentinas. El notebook lleva los datos crudos desde la limpieza
hasta el modelado, pasando por feature engineering, análisis exploratorio y
visualización, y termina con una regresión lineal como línea base — reportando
sus límites con honestidad en lugar de inflar el resultado.

### Qué hace

- **Carga** el dataset Properati Argentina directo de Kaggle con `kagglehub`
- **Limpia** los datos: elimina duplicados, maneja valores atípicos y filtra
  publicaciones que estén realmente *en venta* y valuadas en *dólares*
- **Crea** la columna `precio_m2` (precio ÷ superficie cubierta)
- **Explora** con estadística descriptiva (promedio, mediana, desvío estándar)
- **Visualiza** precio promedio por localidad, precio vs. superficie, y un
  subplot comparando **CABA** contra **Gran Buenos Aires**
- **Modela** una `LinearRegression` que predice precio a partir de la superficie
  cubierta en CABA

### Resultados y limitaciones honestas

El modelo llega a **R² ≈ 0.27**. Es un ajuste *débil*, y el notebook lo dice
claro: la superficie cubierta por sí sola explica solo una parte de la
varianza del precio. El análisis lo plantea como una tendencia coherente y una
primera estimación razonable, no un modelo predictivo — y señala a la ubicación
y a la dispersión del mercado como la fuente dominante de la varianza restante.

**Esto es lo más importante del repo.** Una línea base débil documentada con
integridad vale más que un score alto sin explicación.

### Cómo ejecutarlo

```bash
pip install pandas numpy matplotlib scikit-learn kagglehub jupyter
jupyter notebook Proyecto_DATASET.ipynb
```

La primera celda descarga el dataset de Kaggle automáticamente.

### Estructura del proyecto

| Parte | Contenido |
|---|---|
| 1 | Carga del dataset |
| 2 | NumPy y Pandas |
| 3 | Limpieza de datos |
| 4 | Feature engineering |
| 5 | Análisis exploratorio y visualización |
| 6 | Modelo de regresión lineal |

---

## Licencia

MIT — ver [LICENSE](LICENSE). El dataset es de su autor original y se usa con
fines educativos.
