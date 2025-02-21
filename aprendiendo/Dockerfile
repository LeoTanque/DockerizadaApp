FROM node:20.2.0-alpine AS build
WORKDIR /app

# Copiar package.json y package-lock.json (si existe) e instalar dependencias
COPY package*.json ./
RUN npm install

# Copiar el resto del código fuente
COPY . .

# Exponer el puerto 4200
EXPOSE 4200

# Iniciar el servidor de desarrollo de Angular
CMD ["npx", "ng", "serve", "--host", "0.0.0.0", "--port", "4200"]



