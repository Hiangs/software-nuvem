# Usa a imagem base do Node.js
FROM node:18

# Cria e define o diretório de trabalho
WORKDIR /app

# Copia o package.json e package-lock.json
COPY package*.json ./

# Instala as dependências do projeto
RUN npm install

# Copia todo o código da aplicação para o diretório de trabalho
COPY . /app

# Expõe a porta que o Parse Server usará
EXPOSE 1337

# Define o comando para iniciar o Parse Server
CMD ["npm", "start"]
