# Use a imagem base do Airflow
FROM apache/airflow:2.1.0

# Instale as dependências do Polaris
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copie o código do Polaris (se necessário)
COPY polaris /opt/airflow/polaris

# Defina o diretório de trabalho
WORKDIR /opt/airflow

