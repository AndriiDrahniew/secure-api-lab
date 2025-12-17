# Лабораторно-практична робота №3
Цей проєкт реалізує REST API. 
API підтримує аутентифікацію та авторизацію за ролями, а також демонструє роботу з основними HTTP-методами.
## Встановлення та запуск
```
npm install
```
```
npm start
```
```
npm test
```
## Структура проєкту
```
├─ data.js          # модуль з даними (користувачі, документи, співробітники)
├─ server.js        # основний файл сервера
├─ test-client.js   # скрипт для програмного тестування API
├─ .gitignore       # ігнорування node_modules та службових файлів
└─ package.json     # маніфест проєкту
```
## Хід виконання
![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-11%20193312.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20103748.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20103821.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20104037.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20104052.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20111625.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20111751.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20111831.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20111958.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20113825.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20114545.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20114733.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20125313.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20125312.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20125344.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20125548.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20125632.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20125850.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20125957.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20130341.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20130514.png)

![Photo](https://github.com/AndriiDrahniew/secure-api-lab/blob/main/screenshots/Screenshot%202025-11-12%20130831.png)

## Таблиця ендпоінтів
| Метод | URL | Опис | Заголовки (Auth) | Тіло запиту (JSON) | Коди відповіді |
|--------|-----|------|------------------|--------------------|----------------|
| **GET** | `/documents` | Отримати список всіх документів | `X-Login`, `X-Password` | – | 200 OK, 401 Unauthorized |
| **POST** | `/documents` | Створити новий документ | `X-Login`, `X-Password` | `{ "title": "Q3 Report", "content": "..." }` | 201 Created, 400 Bad Request, 401 Unauthorized |
| **DELETE** | `/documents/:id` | Видалити документ за ID | `X-Login`, `X-Password` | – | 204 No Content, 401 Unauthorized, 404 Not Found |
| **GET** | `/employees` | Отримати список співробітників | `X-Login`, `X-Password` (роль `admin`) | – | 200 OK, 401 Unauthorized, 403 Forbidden |
| **GET** | `/non-existent` | Звернення до неіснуючого ресурсу | `X-Login`, `X-Password` (опціонально) | – | 404 Not Found |
## Посилання на репозиторій
[secure-api-lab (GitHub)](https://github.com/AndriiDrahniew/secure-api-lab)
