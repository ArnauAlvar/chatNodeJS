FROM node:latest

# Directorio de trabajo
WORKDIR /usr/src/app

COPY ./app/package.json .

RUN chmod -R 777 .

RUN npm install -g npm@7.11.2


# SITUAR NODE_MODULES EN LA CARPETA DEL PROYECTO
# RUN set NODE_PATH=./node_modules/;
Run export NODE_PATH=/usr/src/app/node_modules

# instalar dependencias
# Hay que instalar pm2 para hacer que el contenedor no se pare
RUN npm install -g pm2
RUN npm install socket.io --save
RUN npm install express --save

RUN npm update
RUN npm install


# CMD [ "pm2-runtime", "npm", "--", "start" ]

CMD ["npm", "start"]