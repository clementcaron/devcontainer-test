# Image de base avec Python 3.11 (test avec microsoft devcontainers)
FROM mcr.microsoft.com/devcontainers/python:1-3.11-bookworm

# Eviter les interactions durant apt install
ENV DEBIAN_FRONTEND=noninteractive

# Installer les dépendances système
RUN apt-get update && apt-get install -y \
    build-essential \
    curl \
    git \
    wget \
    vim \
    libssl-dev \
    libffi-dev \
    libglib2.0-0 \
    libxext6 \
    libsm6 \
    libxrender1 \
    && rm -rf /var/lib/apt/lists/*

# Créer un dossier de travail
WORKDIR /workspace

# Installer les bibliothèques data science utiles
RUN pip install --upgrade pip && \
    pip install \
    numpy \
    pandas \
    matplotlib \
    seaborn \
    scikit-learn \
    scipy \
    jupyterlab \
    ipykernel \
    plotly \
    notebook \
    statsmodels \
    xgboost \
    lightgbm

# Expose le port de Jupyter
EXPOSE 8888
