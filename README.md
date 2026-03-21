# Análisis de Tendencias Globales de YouTube para Sterling & Draper

En la industria de la publicidad digital, identificar **contenido viral y tendencias emergentes** es clave para optimizar las campañas de marketing. Este proyecto automatiza el análisis de videos en tendencia en YouTube, permitiendo a los gerentes de planificación **identificar categorías populares por región** y tomar decisiones basadas en datos sobre dónde enfocar los esfuerzos publicitarios.

### Herramientas y tipo de proyecto
![Python](https://img.shields.io/badge/python-357ebd?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23357ebd.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)
![Análisis de tendencias](https://img.shields.io/badge/Análisis_de_tendencias-295F98?style=for-the-badge)
![Automatización](https://img.shields.io/badge/Automatización-295F98?style=for-the-badge)
![Business Intelligence](https://img.shields.io/badge/BI-295F98?style=for-the-badge)

## Preguntas clave
1. ¿Qué categorías de videos estuvieron en tendencia con mayor frecuencia durante el periodo analizado?
2. ¿Cómo varía la distribución de categorías populares entre las diferentes regiones globales?
3. ¿Existen diferencias significativas entre el contenido consumido en Estados Unidos frente al resto del mundo?

## Metodología
- **Reunión de Requisitos Técnicos:** Colaboración con stakeholders (Melanie y Ashok) y administradores de bases de datos para definir los KPIs de negocio y la estructura de la tabla de agregación `trending_by_time`.
- **Preprocesamiento con Python:** Limpieza y transformación de datos brutos para asegurar la integridad de las fechas y categorías antes de la carga en el dashboard.
- **Visualización en Tableau:** Creación de un dashboard interactivo con filtros globales de fecha y país, incluyendo gráficos de historial de tendencias en valores absolutos y porcentuales.
- **Análisis Comparativo:** Evaluación de las discrepancias regionales en el consumo de contenido para personalizar estrategias de marketing local.

## Conclusiones y recomendaciones

### Hallazgos principales:
- **Categorías Dominantes:** Sectores como **Entretenimiento** y **Música** mantienen una presencia constante en el Top de tendencias global, siendo los vehículos más seguros para publicidad masiva.
- **Particularidades Regionales:** En Estados Unidos, se observa una mayor fragmentación de intereses comparado con otras regiones, destacando categorías como "Howto & Style" y "Comedy".
- **Dinámica Temporal:** Las tendencias suelen tener picos de 24-48 horas, lo que exige una capacidad de respuesta rápida de los equipos de marketing.

### Estrategias recomendadas:
- **Optimización de Presupuesto:** Enfocar la inversión publicitaria en las categorías con mayor retención en el historial de tendencias (como Música) para maximizar impresiones.
- **Segmentación por País:** Adaptar el contenido de los anuncios según la categoría líder de cada región, evitando campañas genéricas globales.
- **Uso del Dashboard:** Utilizar la actualización diaria del sistema para ajustar las pujas de anuncios en tiempo real basándose en los videos que están ganando tracción.

## Diccionario de Datos
El equipo de ingeniería de datos proporcionó la tabla de agregación `trending_by_time` con la siguiente estructura:

- `record_id` — Clave primaria única para cada registro.
- `region` — País o región geográfica del video.
- `trending_date` — Fecha y hora en que el video se hizo tendencia.
- `category_title` — Categoría temática del video (ej. Entretenimiento, Noticias).
- `videos_count` — Número total de videos de esa categoría en la sección de tendencias en ese momento.

---
**Enlace al Dashboard:** [Ver en Tableau Public](https://public.tableau.com/app/profile/ari.de.le.n/viz/YouTube_Trending_Analysis_SterlingDraper/Dashboard1?publish=yes)
