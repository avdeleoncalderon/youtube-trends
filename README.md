# Análisis Global de Tendencias en YouTube — Sterling & Draper

![Python](https://img.shields.io/badge/python-357ebd?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23357ebd.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)

---

## Objetivo / Pregunta de negocio

Una agencia de publicidad necesitaba saber **dónde colocar su presupuesto publicitario en YouTube** de forma más eficiente. Las preguntas que guiaron el análisis fueron:

1. ¿Qué categorías de video aparecen en tendencias con mayor frecuencia?
2. ¿Cómo varía esa distribución entre países?
3. ¿Qué consume el mercado estadounidense frente al resto del mundo?

---

## Datos

**Fuente:** Tabla de agregación `trending_by_time` proporcionada por el equipo de ingeniería de datos de la empresa simulada.

**Contenido:** 12,343 registros que cubren el periodo de **noviembre 2017 a junio 2018**, con las siguientes columnas:

| Campo | Descripción |
|---|---|
| `record_id` | Clave primaria única |
| `region` | País del registro (Francia, India, Japón, Rusia, EE. UU.) |
| `trending_date` | Fecha en que los videos estuvieron en tendencia |
| `category_title` | Categoría temática (18 categorías en total) |
| `videos_count` | Número de videos en tendencia de esa categoría ese día |

---

## Proceso

**Limpieza y preparación (Python + Pandas):**
- Se convirtió `trending_date` de tipo `object` a `datetime64` para habilitar filtros temporales en Tableau.
- Se verificó la ausencia de valores nulos en todas las columnas (resultado: 0 nulos).
- No fue necesario realizar joins; los datos ya estaban pre-agregados por región y categoría.
- **Supuesto clave:** cada fila representa un snapshot diario; no refleja videos individuales sino el volumen por categoría.

**Análisis (Python):**
- Suma total de `videos_count` por categoría y región para identificar dominancia histórica.
- Filtro de últimos 7 días para capturar el estado más reciente del mercado.

**Visualización (Tableau):**
- Dashboard interactivo con filtros globales de fecha y país.
- Gráficos de área para historial de tendencias en valores absolutos y porcentuales.

---

## Entregable

🔗 **[Ver Dashboard en Tableau Public](https://public.tableau.com/app/profile/ari.de.le.n/viz/YouTube_Trending_Analysis_SterlingDraper/Dashboard1?publish=yes)**

📓 El notebook de preprocesamiento está disponible en este repositorio: `youtube_trends_preprocessing.ipynb`

**Cómo ejecutar el notebook:**
```bash
# Clonar el repositorio
git clone <url-del-repositorio>

# Instalar dependencias
pip install pandas

# Abrir el notebook
jupyter notebook youtube_trends_preprocessing.ipynb
```
El archivo `trending_by_time.csv` debe estar en la misma carpeta que el notebook.

---

## Insights

1. **Entertainment y Music dominan globalmente.** Estas dos categorías concentran consistentemente el mayor volumen de videos en tendencia en los 5 países analizados, lo que las convierte en las apuestas más seguras para campañas de alcance masivo.

2. **EE. UU. tiene un perfil de consumo más fragmentado.** A diferencia de otros países, el mercado estadounidense distribuye su atención entre más categorías (Entertainment, Music, Howto & Style, Comedy), lo que exige una segmentación más granular para campañas locales.

3. **Las tendencias son efímeras.** Los picos de visibilidad duran entre 24 y 48 horas, lo que implica que el valor publicitario está en la velocidad de reacción, no en la planificación a largo plazo dentro de una misma tendencia.

---

## Recomendación / Siguiente paso

En un contexto laboral real, el siguiente paso sería conectar estos datos de tendencias con métricas de conversión y costo por clic (CPC) por categoría, para determinar no solo dónde hay más visibilidad, sino dónde cada dólar invertido genera mayor retorno. También evaluaría expandir el análisis a más regiones para robustecer las decisiones de segmentación global.

---

## Estructura del repositorio

```
📁 youtube-trends-analysis/
├── trending_by_time.csv               # Dataset de entrada
├── youtube_trends_preprocessing.ipynb # Notebook de limpieza y análisis
└── README.md                          # Este archivo
```

---

## Tecnologías utilizadas

- **Python 3.9** · Pandas — limpieza, conversión de tipos y análisis exploratorio
- **Tableau Public** — visualización interactiva y dashboard final

---

## Contacto

¿Preguntas o feedback? Puedes encontrarme en **[LinkedIn](https://www.linkedin.com/)** o escribirme a **[av.deleoncalderon@gamil.com]**.
