# Создание rest api на NodeJs + express
1. Подготовка окружения. Сделать пулл из репозитория (git clone, git pull) 

2. Инициализация проекта:
      - Создать файл package.json командой npm init
      - Установить зависимости (mysql2 для работы с mysql и express для создания сервера, dotenv для работы с файлом .env)`npm install mysql2 express`
      - Создать файл index.js
      - Работа с файлом .env: задать в .env файле переменные DB_NAME, DB_USERNAME, DB_PASSWORD и, с помощью установленного модуля dotenv подтянуть их для дальнейшей работы (Документация по dotenv: https://www.npmjs.com/package/dotenv)
      
3. Создать бд на mysql. Таблицы: Users и Posts с полями: 
      - Users: id, first_name, last_name
      - Posts: id, title, description, userId(ManyToOne связь с таблицей Users)
      
4. Создать файл conn.js, подключиться к БД с помощью mysql2, название, имя пользователя и пароль брать из .env (см. пункт 2) и экспортировать созданное соединение в index.js (Информация по mysql2 - https://www.npmjs.com/package/mysql2) 

5. Создать express сервер в файле index.js (Порт брать из .env)

6. Прописать эндпоинты Rest Api (Можно с помощью express router, можно в самом index.js файле):
    - /api/Users/list - возвращает данные всех пользователей что есть в базе
    - /api/Posts/list - вовзращает данные всех постов что есть в базе
    - /api/Posts/:id - возвращает данные поста, имеющего переданный id (передавать id можно или в параметрах запроса или в query параметрах)

7. Залить код на свой репозиторий.
