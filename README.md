````markdown
# Análisis de Cancelación de Clientes (Churn) – TelecomX

Este proyecto tiene como objetivo analizar los datos de clientes de una empresa de telecomunicaciones (TelecomX) para identificar patrones asociados con la cancelación del servicio (churn), utilizando técnicas de limpieza, visualización y análisis exploratorio de datos.

---

## Librerías utilizadas

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import requests
````

---

## 1. Extracción de los datos

Los datos fueron obtenidos desde un archivo JSON público ubicado en el siguiente URL:

```
https://raw.githubusercontent.com/alura-cursos/challenge2-data-science-LATAM/refs/heads/main/TelecomX_Data.json
```

Se utilizó `pandas.read_json()` para cargar los datos en un DataFrame y se realizó una vista preliminar para entender su estructura.

---

## 2. Transformación de los datos

* Se normalizaron los nombres de las columnas (minúsculas, sin espacios ni puntos).
* Se desanidaron columnas anidadas como `customer`, `phone`, `internet` y `account`.
* Se convirtieron columnas numéricas como `charges_monthly`, `charges_total` y `tenure`.
* Se rellenaron valores nulos con la mediana (cuando fue necesario).
* Se estandarizaron los valores categóricos como `"No internet service"` → `"No"` para simplificar el análisis.

---

## 3. Análisis y visualización

Se realizaron varios gráficos para explorar patrones relevantes en torno al `churn`:

* ✅ **Distribución de cancelaciones** (churn)
* ✅ **Relación entre churn y tipo de contrato**
* ✅ **Distribución de cargos mensuales según churn**
* ✅ **Duración del cliente (`tenure`) por tipo de contrato**
* ✅ **Correlación entre variables numéricas**
* ✅ **Resumen estadístico agrupado por churn**

---

## 4. Informe Final

**Hallazgos principales:**

* La proporción de clientes que han cancelado el servicio (`churn`) es aproximadamente **X%**.
* Los clientes con **contratos mensuales** tienen una tasa de cancelación mucho más alta.
* Los clientes que cancelan suelen tener **cargos mensuales más altos**.
* La duración de la relación con la empresa (`tenure`) es **significativamente menor** en quienes cancelan.

**Recomendaciones:**

* Incentivar la **contratación anual o bianual** para fidelizar clientes.
* Ofrecer **descuentos personalizados** para clientes con altos cargos mensuales.
* Analizar y mejorar servicios asociados a clientes con alta rotación.

---

## Estructura del proyecto

* `TelecomX_Data.json`: Datos en bruto (desde la URL).
* `notebook.ipynb`: Libreta de Google Colab con código ETL, análisis y visualizaciones.
* `README.md`: Documentación del proyecto.

---

## Créditos

Desafío del curso de Ciencia de Datos - [Alura LATAM](https://www.aluracursos.com/)
```
