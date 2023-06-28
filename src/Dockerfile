# Como o projeto é feito em Node utilizar como base imagem oficial do Node
FROM node
# Entrar no diretório /app
WORKDIR /app 
# Copiar todo arquivo que se inicie com 'package' e seja extensão .json
COPY package*.json ./
# Executa o comando npm install
RUN npm install
# Copiar tudo do diretório raiz local para o diretório raiz da Aplicação em Container
COPY . .
# Expôr porta 8080 por se tratar de uma aplicação Web. Tal porta esta definida no arquivo 'server.js'
EXPOSE 8080
# Executar comando 'node server.js' para execução da aplicação
CMD ["node", "server.js"]