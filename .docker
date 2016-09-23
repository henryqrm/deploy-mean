# Sistema operacional que será usado no conteiner
FROM alpine:3.1


# Adiciona o nodeJS na imagem do conteiner 
RUN apk add --update nodejs

# Instala todas as dependências do projeto 
COPY package.json /src/package.json
RUN cd /src; npm install

# Bundle app source
COPY . /src

# Libera a porta 8080
EXPOSE  8080

# Executa o node
CMD ["node", "/src/index.js"]
