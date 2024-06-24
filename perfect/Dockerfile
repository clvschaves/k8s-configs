# Use uma imagem base do Python
FROM python:3.8-slim

# Instale as dependências do sistema necessárias
RUN apt-get update && apt-get install -y \
    build-essential \
    libssl-dev \
    libffi-dev \
    libsqlite3-dev \
    && rm -rf /var/lib/apt/lists/*

# Use uma imagem base do Python
FROM python:3.8-slim

# Instale as dependências do sistema necessárias
RUN apt-get update && apt-get install -y \
    build-essential \
    libssl-dev \
    libffi-dev \
    libsqlite3-dev \
    && rm -rf /var/lib/apt/lists/*

# Instale Prefect e outras dependências
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Defina o diretório de trabalho
WORKDIR /opt/prefect


# Defina o comando padrão para iniciar o Prefect
CMD ["prefect", "orion", "start"]


