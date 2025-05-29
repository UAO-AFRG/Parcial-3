# Usa una imagen base de Debian o Ubuntu para facilitar instalación de paquetes
FROM python:3.10-slim

# Variables de entorno para evitar preguntas durante instalación de paquetes
ENV DEBIAN_FRONTEND=noninteractive

WORKDIR /webapp

# Instala dependencias del sistema necesarias para MySQL y compilación
RUN apt-get update && apt-get install -y \
    python3-dev \
    default-libmysqlclient-dev \
    build-essential \
    pkg-config \
    default-mysql-client \
    && rm -rf /var/lib/apt/lists/*

# Copia requirements.txt y instala dependencias Python
COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

# Copia el código fuente de la app
COPY . .

# Variables de entorno para Flask
ENV FLASK_APP=run.py
ENV FLASK_ENV=development
ENV FLASK_RUN_HOST=0.0.0.0
ENV FLASK_RUN_PORT=8000

EXPOSE 8000

# Comando para iniciar la app Flask
CMD ["flask", "run", "--host=0.0.0.0", "--port=8000"]
