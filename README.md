# QuAns API

**API для системы вопросов и ответов на Golang**  

---

## Особенности (технические требования)

- Использован net/http
- Работа с БД через GORM
- Использован PostgreSQL
- Использованы миграции с помощью goose
- Обернуто в Docker, для запуска docker-compose
- Чистая архитектура — `handlers`, `repository`, `models`

---

## API Endpoints

## Вопросы (Questions)

- `GET /questions/` - список всех вопросов
- `POST /questions/` - создать новый вопрос
- `GET /questions/{id}` - получить вопрос и все ответы на него
- `DELETE /questions/{id}` - удалить вопрос (вместе с ответами)

## Ответы (Answers)
- `POST /questions/{id}/answers/` - добавить ответ к вопросу
- `GET /answers/{id}` - получить конкретный ответ
- `DELETE /answers/{id}` - удалить ответ

---

## Запуск проекта

1. Клонируйте репозиторий
2. Запуск с помощью Docker
   docker-compose up --build
   API будет доступ: http://localhost:8080
3. Для остановки контейнеров использовать
   docker-compose down
4. Для удаления БД
   docker-compose down -v

