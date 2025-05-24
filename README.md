# Análisis y Predicción del Riesgo de Siniestro en Seguros de Automóviles: CONTEXTO

The insurance sector faces ongoing challenges in accurately assessing claim risk, a key factor that directly impacts profitability, premium allocation, and capital management. Increasing regulatory pressure—through frameworks such as Solvency II—imposes strict requirements regarding solvency, risk governance, and financial transparency, demanding the use of robust and auditable models for insurance risk estimation. 

Advances in machine learning techniques and statistical modeling have significantly improved claim prediction by leveraging the availability of historical insurance data. In this study, we use the Porto Seguro Safe Driver Prediction dataset to develop predictive models aimed at optimizing claim risk estimation, thereby enhancing pricing accuracy and capital allocation. 

However, the problem exhibits a structurally imbalanced class distribution, as most policyholders do not file claims. This introduces methodological challenges in detecting low-frequency events with high reliability. Beyond predictive performance, the proposed approach emphasizes explainability, robustness, and regulatory compliance, aligning with Solvency II requirements and EIOPA guidelines on the use of AI in insurance. An MLOps perspective is also incorporated, ensuring traceability, monitoring, and efficient model deployment in production environments. 

The combination of advanced modeling, regulatory governance, and operational scalability positions this proposal at the intersection of predictive accuracy, interpretability, and regulatory compliance within the insurance domain.

---

# Dataset:

Porto Seguro's: https://www.kaggle.com/competitions/porto-seguro-safe-driver-prediction/overview

El dataset de entrenamiento es train.csv y el de test test.csv. Ambos se descargaron e introducieron en el directorio raíz (el mismo en el que se ejecuta el notebook .ipynb). 

## Introducción/estructura del contenido:

El notebook principal `Analisis_riesgo_siniestralidad_TFM_MarcRoman.ipynb` contiene el análisis detallado, visualizaciones y modelos utilizados para la predicción del riesgo de siniestralidad. Además, se proporciona un notebook auxiliar `set_venv_and_kernel.ipynb` para configurar el entorno virtual y el kernel de Jupyter, facilitando la reproducción del entorno por terceros.

## Configuración del Entorno Virtual
Para configurar el entorno virtual y asociarlo como kernel de Jupyter, sigue estos pasos:

1. **Crear carpeta base de entornos**: `~/environments`
2. **Crear entorno virtual**: `~/environments/tfm_venv_001`
3. **Activar entorno**
4. **Instalar dependencias desde `requirements_tfm.txt`**
5. **Registrar el entorno como kernel de Jupyter**

Puedes ver y ejecutar el notebook `set_venv_and_kernel.ipynb` para automatizar estos pasos.

## Descripción de los Archivos

| Archivo | Descripción |
|--------|-------------|
| `Analisis_riesgo_siniestralidad_TFM_MarcRoman.ipynb` | Notebook principal del TFM donde se realiza el análisis y predicción del riesgo de siniestralidad en seguros de automóviles. Contiene código, visualizaciones y explicaciones paso a paso. |
| `[NON_executed_for_size_purposes] Analisis_riesgo_siniestralidad_TFM_MarcRoman.ipynb` | Ídem al anterior pero sin celdas ejecutadas para < 80 Mb. |
| `Analisis_riesgo_siniestralidad_TFM_MarcRoman.html` | Versión exportada en HTML del notebook anterior, útil para visualizar el contenido sin necesidad de ejecutar código. |
| `requirements_tfm.txt` | Lista de dependencias necesarias para ejecutar el notebook. Se instala automáticamente al configurar el entorno virtual. |
| `set_venv_and_kernel.ipynb` | Notebook auxiliar que automatiza la creación del entorno virtual (`tfm_venv_001`), instalación de dependencias y registro del kernel en Jupyter. Ideal para que terceros puedan reproducir el entorno fácilmente. |
| `README.md` | Este archivo. Contiene la descripción general del proyecto, instrucciones de uso y detalles sobre los archivos incluidos. |
| `LICENSE` | Archivo de licencia del proyecto. Define los términos bajo los cuales se puede usar y distribuir el código. |
| `results/` | Carpeta donde se almacenan los resultados generados por el notebook, como modelos (.pkl), Imputers y/o archivos intermedios como parametría del proceso de optimización de Optuna (se genera de manera automática al ejecutar el notebook) |

---
