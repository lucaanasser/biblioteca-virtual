# frontend/Dockerfile
FROM node:18

WORKDIR /app

# Instala dependências primeiro para usar cache
COPY package*.json ./
RUN npm install

# Copia o restante do projeto
COPY . .

EXPOSE 5173

CMD ["npm", "run", "dev", "--", "--host"]
