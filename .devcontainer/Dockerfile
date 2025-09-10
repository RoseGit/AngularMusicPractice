FROM node:10-alpine

# Instala dependencias básicas
RUN apk add --no-cache bash git openssh

# Crea directorio de trabajo
WORKDIR /workspace

# Copia el package.json si existe (mejora caché de npm install)
COPY package*.json ./

# Instala dependencias
RUN npm install || true

# Copia el resto del código
COPY . .

CMD ["npm", "start"]
