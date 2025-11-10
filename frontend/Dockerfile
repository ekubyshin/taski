# Используем официальный Node.js образ
FROM node:16-alpine

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем package.json и package-lock.json
COPY package*.json ./

# Устанавливаем зависимости
RUN npm ci --silent

# Копируем весь код приложения
COPY . .

# Открываем порт 3000 для React dev server
EXPOSE 3000

# Запускаем React development сервер
CMD ["npm", "start"]

