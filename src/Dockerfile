# Como o projeto é feito em Node utilizar como base imagem oficial do Node
# É uma boa prática definir a versão da imagem base porque se não for definido sempre será utilizado a última versão, 
# o que pode alterar algum funcionamento de versões anteriores. Importante manter a idempotência.
FROM node:18.16.0
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