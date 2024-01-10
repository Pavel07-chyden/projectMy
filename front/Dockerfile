# Используйте образ Node.js
FROM node:latest

# Установите зависимости проекта
WORKDIR /var/www/front
COPY package.json package-lock.json /var/www/front/
RUN npm install

# Копируйте и скомпилируйте код проекта
COPY . /var/www/front
RUN npm run build
