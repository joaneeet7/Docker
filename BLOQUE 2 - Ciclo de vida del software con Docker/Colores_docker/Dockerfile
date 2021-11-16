FROM node:12.13

# Creación de un directorio de trabajo
RUN echo "Creación del directorio de trabajo"
WORKDIR /app

# Volumen para la información
RUN echo "Creación del volumen de información"
VOLUME "$PWD":/app

# Copiar los ficheros .json
RUN echo "Copia de los ficheros .json"
COPY package.json ./
COPY package-lock.json ./

# Ejecutar la instalación de los módulos
RUN echo "Instalación de los módulos"
RUN npm install

# Exposición del puerto 3000
EXPOSE 3000

# Copiar todo el código 
COPY . .

# Ejecución de la DAPP
CMD ["npm", "run", "start"]