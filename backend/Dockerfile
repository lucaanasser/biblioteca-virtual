# backend/Dockerfile
FROM node:18-alpine

WORKDIR /app

# Copia apenas arquivos de dependências para instalar
COPY package*.json ./

# Instala as dependências (incluindo dotenv)
RUN npm install

# Copia o restante do código
COPY . .

EXPOSE 3000

CMD ["node", "index.js"]
