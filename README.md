# Forecasting-pipeline-azure-postgresql-ml

We’ll explore how to build an end-to-end time-series forecasting pipeline that predicts future temperature trends using data stored in Azure PostgreSQL.
This project demonstrates how to integrate data engineering, statistical modeling, and deep learning within an Azure Machine Learning (Azure ML) environment.

By combining Prophet (for interpretable statistical forecasting) and LSTM networks (for deep learning-based temporal modeling), we show how to move from raw data in a cloud database to trained, versioned ML models ready for deployment.



🎯 <b>Objective</b>

This project aims to:

* Build a reproducible forecasting workflow using Azure PostgreSQL, Python, and Azure ML.

* Compare Prophet vs. LSTM approaches for short- and long-term temperature prediction.

* Demonstrate MLOps best practices such as dataset registration and model versioning.

The test serves as a blueprint for IoT telemetry prediction, demand forecasting, or climate analytics projects that need both statistical and neural forecasting models.


🧩<b> Features</b>

* Data ingestion directly from Azure PostgreSQL using psycopg2.

* Exploratory analysis with Pandas, Seaborn, and statsmodels for trend & seasonality inspection.

* Two forecasting models:

  * Prophet: Decomposes trends and seasonal patterns automatically.

  * LSTM: Captures nonlinear and short-term dependencies.

* Scalable workflow: Easily replace dataset or model for new time-series sources.

* Reproducible artifacts: Trained model, scaler, and forecast outputs stored in /outputs

<b> Architecture </b>

        ┌──────────────────────────┐
        │  Azure PostgreSQL        │
        │  (Data Storage)          │
        └──────────┬───────────────┘
                   │ psycopg2
                   ▼
        ┌──────────────────────────┐
        │  Data Extraction & EDA   │
        │  (Pandas, Seaborn)       │
        └──────────┬───────────────┘
                   ▼
        ┌──────────────────────────┐
        │  Modeling                │
        │  - Prophet               │
        │  - LSTM (Keras)          │
        └──────────┬───────────────┘
                   ▼
        ┌──────────────────────────┐
        │  Forecast Visualization  │
        │  (Matplotlib, Plotly)    │
        └──────────────────────────┘

🧪 <b>Testing Objective</b>

This test validates how effectively a hybrid time-series forecasting framework can be built using both statistical and deep learning models on data retrieved from Azure PostgreSQL, integrated with Azure ML for experiment tracking.

It ensures:

  * Seamless data flow between storage, model training, and forecast generation.

  * Compatibility of AI frameworks (Prophet, TensorFlow) in Azure ML environments.

  * Reproducible outputs and modularity for future deployment or scaling.

⚡ <b>Key Takeaways</b>

  * Prophet excels at transparency and long-term patterns.

  * LSTM adapts well to noisy, nonlinear, and short-term fluctuations.

  * Azure ML + PostgreSQL provides a robust cloud-native MLOps foundation for any forecasting pipeline.

🗂️ Dataset used : https://www.kaggle.com/datasets/sumanthvrao/daily-climate-time-series-data
