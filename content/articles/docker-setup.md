---
title: "🐳 Развертывание в Docker"
tags: ["devops", "docker"]
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
FROM nginx:alpine
COPY ./public /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```

{{< callout type="info" >}}
**Совет по оптимизации:** Использование базового дистрибутива `alpine` уменьшает итоговый размер образа контейнера до ~10 МБ.
{{< /callout >}}
