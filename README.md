# Simulación y Clasificación de Tráfico de Red para un SOC
## Proyecto Final de Programación Avanzada para la ciencia de datos 

Este proyecto implementa una simulación de tráfico de red en tiempo real, clasifica paquetes como **benignos** o **maliciosos (DDoS)** utilizando un modelo de machine learning, y presenta los resultados en un dashboard interactivo tipo **SOC (Security Operations Center)**.

---

ProyectoPACD/
├── app/
│ ├── simulator.py # Simula tráfico real a partir del dataset
│ └── classifier.py # Clasifica paquetes usando el modelo de ML
├── data/
│ └── processed/
│ └── clean_dataset.csv # Dataset limpio y normalizado
├── logs/
│ └── traffic_log.csv # Log de los paquetes clasificados
├── models/
│ └── traffic_model.pkl # Modelo de ML entrenado (Random Forest)
├── dashboard.py # Script del dashboard con Streamlit
├── requirements.txt # Dependencias del proyecto
└── README.md # Este archivo

---

## ¿Cómo ejecutar el proyecto?

### paso n°1: Instalar dependencias
Abre una terminal, navega a la raíz del proyecto y ejecuta el siguiente comando para instalar las librerías necesarias:
pip install -r requirements.txtxt

### paso n°2: Ejecutar el simulador en una terminal
En la misma terminal, inicia la simulación de tráfico. Este script generará paquetes, los clasificará y guardará los resultados en logs/traffic_log.csv
Generated bash:
python -m app.simulator
[bash
Copiar
Editar
python -m app.simulator]

### paso n°3: Ejecutar el dashboard en otra terminal
Abre una segunda terminal y ejecuta el siguiente comando para iniciar la interfaz web interactiva. Tu navegador se abrirá automáticamente con el dashboard:
Generated bash
streamlit run dashboard.py

### Características del Dashboard

El dashboard se actualiza automáticamente cada 5 segundos para ofrecer una visión en tiempo real de la simulación. Incluye las siguientes características:

*   **Métricas Clave:**
    *   Contadores de tráfico total, benigno, ataques DDoS y la precisión (accuracy) del modelo.
*   **Visualizaciones de Datos:**
    *   Distribución de predicciones (gráfico de pastel y barras).
    *   Evolución del tráfico a lo largo del tiempo.
    *   Comparativa entre predicciones y valores reales.
*   **Análisis del Modelo:**
    *   Matriz de confusión interactiva.
    *   Análisis de Falsos Positivos y Falsos Negativos.
    *   Gráfico de dispersión de la confianza del modelo.
*   **Tabla de Eventos:**
    *   Registro con los últimos paquetes clasificados.

### Tecnologías Utilizadas
* **Lenguaje:** Python 3.10
* **Análisis de Datos y ML:** Pandas, Scikit-learn
* **Dashboard y Visualización:** Streamlit, Plotly, Seaborn, Matplotlib
* **Modelo:** Joblib (para guardar y cargar el modelo entrenado)



Proyecto final — Programación Avanzada para Ciencia de Datos
