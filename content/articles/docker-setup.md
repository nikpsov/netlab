---
title: Развертывание в Docker
tags:
  - devops
  - docker
  - containers
---

# 🐳 Развертывание в Docker

Практическое руководство по контейнеризации приложений и веб-сервисов.

---

## 🚀 Основные команды Docker

```bash
# Запуск контейнера в фоновом режиме с пробросом портов
docker run -d -p 8080:80 --name netlab-web nginx:alpine

# Просмотр запущенных контейнеров
docker ps

# Просмотр логов контейнера
docker logs -f netlab-web
```

---

## 📦 Пример Dockerfile

```dockerfile
FROM node:24-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npx quartz build

FROM nginx:alpine
COPY --from=builder /app/public /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```

> [!TIP] Оптимизация
> Использование многоэтапной сборки (Multi-stage builds) уменьшает итоговый размер образа контейнера.

---

## 🔗 Связи
- Базовые сетевые концепции описаны в [[Основы компьютерных сетей]].
- Для возврата в начало перейдите на [[🚀 NetLab — База знаний и Гайды|Главную страницу]].
