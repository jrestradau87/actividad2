#indicamos la imgen base para ejecutar node
FROM node:18-alpine
#Se crea el directorio de la aplicacion dentro del contenedor
WORKDIR /app
#Comando para copiar el archivo que contiene las dependencias 
COPY package*.json ./
#Instruccion para copiar las dependencias de node en el directorio de la app
RUN npm ci --omit=dev
# copiar el codigo
COPY . .
#Exponer la aplicacion en el puerto 3001
EXPOSE 3001
#Comando para iniciar la aplicacion 
CMD [ "npm","start" ] 