# FROM node:alpine
FROM daveamit/node-alpine-grpc

# camada de cached para os módulos do Node
RUN cd /tmp && npm install

RUN mkdir -p /src 
# Instalar MariaDB SQL e rodar o script para injetar o SQL

RUN npm install mysql
# Definir diretório de trabalho

WORKDIR /src
ADD . /src

# Expor porta 80
EXPOSE  8080

# Rodar o app usando nodemon
CMD ["node", "/src/index.js"]