FROM node:latest

# Directorio de trabajo
WORKDIR /usr/src/app

COPY ./app/package.json ./

# actualizar a ultima version NPM
RUN npm install -g npm@latest

# Hay que instalar pm2 para hacer que el contenedor no se pare
RUN npm install -g pm2

# SITUAR NODE_MODULES EN LA CARPETA DEL PROYECTO
RUN export NODE_PATH=./node_modules

# instalar dependencias
RUN npm install




# CMD [ "pm2-runtime", "npm", "--", "start" ]

CMD ["npm", "start"]