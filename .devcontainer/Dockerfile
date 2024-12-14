# Verwende eine offizielle Python-Base-Image
FROM python:3.10-slim

# Setze den Arbeitsordner
WORKDIR /workspace

# Installiere grundlegende Abhängigkeiten
RUN apt-get update && apt-get install -y \
    build-essential \
    libmysqlclient-dev \
    && rm -rf /var/lib/apt/lists/*

# Kopiere Python-Abhängigkeiten
COPY requirements.txt requirements.txt

# Installiere Python-Pakete
RUN pip install --no-cache-dir -r requirements.txt

# Starte den Container im Arbeitsordner
CMD ["bash"]