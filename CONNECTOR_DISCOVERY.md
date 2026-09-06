# Retool Connector — Discovery & Vendor API Specification

**Официальный сайт:** https://retool.com  
**Базовый эндпоинт API:** `https://<retool-domain>/api/v2`  
**Схема авторизации:** Retool Access Token (Bearer Token)

## Поддерживаемые сущности API
- приложения apps (/api/v2/apps)
- ресурсы ресурсов (/api/v2/resources)
- пользователи (/api/v2/users)
- группы доступа

## Архитектурные требования
- Использование безопасного клиента с контролем таймаутов, повторных попыток (backoff) и обработкой rate limit.
- Валидация входных данных через Pydantic-схемы без утечки чувствительных полей в логи.
- Тестовая точка проверки подключения: `GET /api/v2/users`.
