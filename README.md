# Análisis y Predicción del Riesgo de Siniestro en Seguros de Automóviles: CONTEXTO

El sector asegurador enfrenta desafíos constantes en la evaluación del riesgo de siniestralidad, un aspecto clave que impacta en la rentabilidad, la asignación de primas y la gestión de capital. La creciente regulación en este ámbito, con normativas como Solvencia II, impone estrictos requisitos en términos de solvencia, gobernanza del riesgo y transparencia financiera, exigiendo modelos robustos y auditables para la estimación del riesgo asegurador.

El avance de las técnicas de Machine Learning y el modelado estadístico ha permitido mejorar la predicción del riesgo de siniestralidad, aprovechando datos históricos del sector. En este proyecto, se emplea el conjunto de datos Porto Seguro Safe Driver Prediction para construir modelos supervisados bajo un escenario de desbalance estructural severo. Aunque se aplican estrategias de calibración, selección empírica de predictores y ajuste al desbalanceo, el rendimiento predictivo queda limitado por la baja separabilidad estadística del espacio de variables. La ofuscación, la escasa granularidad y el bajo poder informativo de los predictores imponen una cota superior al rendimiento alcanzable, independientemente de la arquitectura empleada.

Además del rendimiento predictivo, la propuesta enfatiza la explicabilidad, robustez y cumplimiento con carácter regulatorio. Pese a las limitaciones del dataset (ofuscación, desbalanceo y baja capacidad predictiva), es posible construir una solución estable, calibrada y explicable. El modelo XGBoost calibrado actúa como un primer filtro útil en la toma de decisiones aseguradoras, y la arquitectura desarrollada es escalable y alineada con los requisitos regulatorios y operativos del sector.

---

# Dataset:

Porto Seguro's: https://www.kaggle.com/competitions/porto-seguro-safe-driver-prediction/overview

El dataset de entrenamiento es train.csv y el de test test.csv. Ambos se descargaron e introducieron en el directorio raíz (el mismo en el que se ejecuta el notebook .ipynb). 

## Introducción/estructura del contenido:

### Notebook:
El notebook principal `Analisis_riesgo_siniestralidad_TFM_MarcRoman.ipynb` contiene el análisis detallado, visualizaciones y modelos utilizados para la predicción del riesgo de siniestralidad. Además, se proporciona un notebook auxiliar `set_venv_and_kernel.ipynb` para configurar el entorno virtual y el kernel de Jupyter, facilitando la reproducción del entorno por terceros. El archivo `[NON_executed_for_size_purposes] Analisis_riesgo_siniestralidad_TFM_MarcRoman.ipynb`es ídem al anterior pero se ajusta con una versión no ejecutada, a efectos de poder visualizar el notebook desde GitHub, sin necesidad de descargarlo.

### Memoria del trabajo:
El archivo `Analisis_riesgo_siniestralidad_TFM_MarcRoman_final.pdf`, contiene la memoria final del trabajo.

---

# Configuración del Entorno Virtual
Para configurar el entorno virtual y asociarlo como kernel de Jupyter, sigue estos pasos:

1. **Crear carpeta base de entornos**: `~/environments`
2. **Crear entorno virtual**: `~/environments/tfm_venv_001`
3. **Activar entorno**
4. **Instalar dependencias desde `requirements_tfm.txt`**
5. **Registrar el entorno como kernel de Jupyter**

Puedes ver y ejecutar el notebook `set_venv_and_kernel.ipynb` para automatizar estos pasos.

# Descripción de los Archivos que se encuentran en el repositorio:

| Archivo | Descripción |
|--------|-------------|
| `Analisis_riesgo_siniestralidad_TFM_MarcRoman.ipynb` | Notebook principal del TFM donde se realiza el análisis y predicción del riesgo de siniestralidad en seguros de automóviles. Contiene código, visualizaciones y explicaciones paso a paso. |
| `[NON_executed_for_size_purposes] Analisis_riesgo_siniestralidad_TFM_MarcRoman.ipynb` | Ídem al anterior pero sin celdas ejecutadas para < 80 Mb. |
| `Analisis_riesgo_siniestralidad_TFM_MarcRoman.html` | Versión exportada en HTML del notebook anterior, útil para visualizar el contenido sin necesidad de ejecutar código. |
| `Analisis_riesgo_siniestralidad_TFM_MarcRoman_final.pdf` | Memoria final del trabajo. |
| `requirements_tfm.txt` | Lista de dependencias necesarias para ejecutar el notebook. Se instala automáticamente al configurar el entorno virtual. |
| `set_venv_and_kernel.ipynb` | Notebook auxiliar que automatiza la creación del entorno virtual (`tfm_venv_001`), instalación de dependencias y registro del kernel en Jupyter. Ideal para que terceros puedan reproducir el entorno fácilmente. |
| `README.md` | Este archivo. Contiene la descripción general del proyecto, instrucciones de uso y detalles sobre los archivos incluidos. |
| `LICENSE` | Archivo de licencia del proyecto. Define los términos bajo los cuales se puede usar y distribuir el código. |
| `results/` | Carpeta donde se almacenan los resultados generados por el notebook, como modelos (.pkl), Imputers y/o archivos intermedios como parametría del proceso de optimización de Optuna (se genera de manera automática al ejecutar el notebook) |

---
