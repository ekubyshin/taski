# Используем официальный Python образ
FROM python:3.9-slim

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем файл с зависимостями
COPY requirements.txt .

# Устанавливаем зависимости
RUN pip install --no-cache-dir -r requirements.txt

# Копируем весь код приложения
COPY . .

# Открываем порт 8000 для Django сервера
EXPOSE 8000

# Выполняем миграции и запускаем сервер
CMD python manage.py migrate && \
    python manage.py runserver 0.0.0.0:8000

