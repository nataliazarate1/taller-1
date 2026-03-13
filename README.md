# Taller de Servicios públicos
**Autor:** Natalia Zárate Yara

---

## Descripción del proyecto

Este proyecto analiza la disponibilidad de servicios públicos utilizando microdatos del DANE. El objetivo principal es identificar la cobertura de servicios como energía eléctrica, acueducto, alcantarillado y recolección de basuras.

El análisis incluye estadísticas descriptivas, distribución por departamentos y regiones, correlaciones entre variables numéricas y gráficas que resumen los hallazgos de forma visual.

El proyecto se implementa en Python dentro de un entorno reproducible usando Docker y Docker Compose, garantizando que todos los análisis puedan ejecutarse sin conflictos de dependencias. Además, se incluyen notebooks con los análisis completos y los resultados en formatos CSV y gráficos.

El enfoque principal es generar información útil para apoyar la toma de decisiones en políticas públicas y programas de asistencia de servicios publicos. 

---

## Instrucciones para ejecutar con Docker

```bash
# Clonar el repositorio
git clone https://github.com/nataliazarate1/taller-seguridad-alimentaria.git
cd taller-seguridad-alimentaria

# Descargar los datos (enlaces)
# - PDF WFP: https://docs.wfp.org/api/documents/WFP-0000158611/download/
# - Microdatos DANE: https://microdatos.dane.gov.co/index.php/catalog/861/get-microdata

# Construir y ejecutar los contenedores
docker-compose up

# Abrir Jupyter Notebook
# Acceder en http://localhost:8888
```
---

## Estructura de carpetas 

taller-seguridad-alimentaria/
├── README.md                    
├── Dockerfile                   
├── docker-compose.yml           
├── requirements.txt             
├── datos/                       
│   └── Carpetas DANE              
├── notebooks/
│   └── analisis.ipynb  
├── resultados/
│   ├── resultados.csv
│   ├── graficos
│       └──grafico_correlaciones.png
└── informe/
    ├── Informe.pdf
    └── Capturas de pantalla.pdf

---

## Fuentes de datos

Programa Mundial de Alimentos (WFP): https://docs.wfp.org/api/documents/WFP-0000158611/download/

DANE – Microdatos de vivienda: https://microdatos.dane.gov.co/index.php/catalog/861/get-microdata

---

## Principales hallazgos

La gran mayoría de las viviendas cuenta con energía eléctrica (~96%), pero hay variación significativa según departamento y región.

El acueducto está presente en ~75% de las viviendas, mientras que el alcantarillado solo llega al 50% de los hogares.

La recolección de basuras se encuentra en ~65% de las viviendas, evidenciando brechas en servicios básicos urbanos y rurales.
