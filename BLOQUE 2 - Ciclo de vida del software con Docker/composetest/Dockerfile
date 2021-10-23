FROM python:3.7-alpine

# Creación de un directorio de trabajo en Docker
WORKDIR /code

# Variables de entorno de Flask
ENV FLASK_APP=app.py 
ENV FLASK_RUN_HOST=0.0.0.0

# Ejecución
RUN apk add --no-cache gcc musl-dev linux-headers

# Instalación de dependencias
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

# Exposición de un puerto 
EXPOSE 5000

# Copiar todo el código
COPY . .

# Ejecución del código 
CMD ["flask", "run"]