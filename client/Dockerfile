# Usa a imagem base do Node.js
FROM node:18

# Cria e define o diretório de trabalho
WORKDIR /usr/src/app

# Copia o package.json e package-lock.json
COPY package*.json ./

# Instala as dependências do projeto
RUN npm install

# Copia todo o código da aplicação para o diretório de trabalho
COPY . .

# Expõe a porta que o Parse Server usará
EXPOSE 1337

# Define a variável de ambiente do Parse Server
ENV PARSE_SERVER_APPLICATION_ID=yourAppId
ENV PARSE_SERVER_MASTER_KEY=yourMasterKey
ENV PARSE_SERVER_DATABASE_URI=mongodb://mongo:27017/dev

# Define o comando para iniciar o Parse Server
CMD ["npm", "start"]
