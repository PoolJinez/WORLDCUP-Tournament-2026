# FIFA World Cup — Data Scraping & 2026 Prediction

Este proyecto tiene como objetivo **extraer datos históricos de los Mundiales de Fútbol (FIFA World Cup)** usando Web Scraping desde Wikipedia, construir un **dataset limpio de resultados pasados** y posteriormente utilizar esa información para **predecir posibles resultados del Mundial 2026**.

Este repositorio incluye:
- Código de scraping (`webscraping_data.ipynb`)
- Código de predicción basado en machine learning (`prediction_2026_worldcup.ipynb`)
- Datasets generados con el scraping (CSV)

---

## 1. Objetivo del Proyecto

1. **Recolectar datos históricos** de todos los mundiales desde 1930 hasta 2018.  
2. **Limpiar, estructurar y guardar** esos datos en archivos CSV.  
3. **Entrenar modelos de machine learning** para analizar patrones de resultados.  
4. **Predecir los resultados del Mundial 2026** usando características históricas.

---

## 2. Contenidos del Repositorio
/
├── prediction_2026_worldcup.ipynb # Modelo predictivo para el Mundial 2026 
├── clean_csv_files-format_fixtures.ipynb # Limpieza y formateo de archivos csv  
├── data/
│ ├── clean_fifa_worldcup_historical_data.csv
│ ├── fifa_worldcup_fixture_2026.csv
│ ├── fifa_worldcup_historical_data.csv
│ ├── fifa_worldcup_missing_data.csv
│ └── format_fixture_data.csv
├── scrapping/
│ ├── Web_Scrapping_bs4.ipynb
│ └── Web_Scrapping_selenium.ipynb
└── README.md

## 3. Web Scraping

La carpeta 'scrapping' contiene:

**`Web_Scrapping_bs4.ipynb`**:

- Extrae resultados de cada partido por mundial  
- Omite los años que no se jugaron (1942 y 1946)  
- Guía paso a paso cómo usar `requests`, `BeautifulSoup` y `pandas`  
- Genera datasets limpios para análisis posteriores  

Tecnologías usadas:
- `requests`
- `BeautifulSoup4`
- `pandas`
- `lxml`

**`Web_Scrapping_selenium.ipynb`**:

- Extrae resultados de cada partido de los Mundiales, incluyendo años faltantes.  
- Omite los años que no se jugaron (1942 y 1946).  
- Automatiza la navegación en Wikipedia con Selenium y selecciona elementos con XPath.  
- Guarda los datos en un CSV listo para análisis posteriores.  

Tecnologías usadas:
- `selenium`
- `pandas`
- `time`
- `chromedriver` / `Chrome WebDriver` 

## 4. Limpieza de Dataset y Formateo

En el archivo **`clean_csv_files-format_fixtures.ipynb`** se:  
- Limpian y normalizan los datasets obtenidos de los Mundiales anteriores.  
- Se formatea `df_fixture` para crear una versión preliminar del Mundial 2026.  
- Permite trabajar con los datos aunque aún no se conozcan los 18 países restantes que clasificarán.

## 5. Predicción del Mundial 2026

En el archivo **`prediction_2026_worldcup.ipynb`** se:

- Cargan los datos históricos generados en el scraping  
- Se crean variables como goles, diferencias, rendimiento histórico, etc.  
- Se entrena un modelo de machine learning (RandomForest, XGBoost, u otro)  
- Se generan predicciones para los partidos del 2026

## Autor
Pool Jinez

## Creditos
Estas prácticas fueron realizadas siguiendo los lineamientos del YouTuber: Frank Andrade / canal: https://www.youtube.com/@thepycoachES
Estas son practicas realizadas para llevar un registro de los códigos utilizados en los proyectos y aprendizaje autodidacta mejorando mis habilidades como 'Data Science'
El valor añadido a este proyecto sera un analisis mas profundo en las predicciones en el Dataset utiliznado varios maodelos y metricas de precision.
