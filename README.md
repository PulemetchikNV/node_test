# Создание rest api на NodeJs + express
1. Подготовка окружения. Сделать пулл из репозитория (git clone, git pull) 

2. Инициализация проекта:
      - Создать файл package.json командой npm init
      - Установить зависимости npm install mysql2 express
    
3. Создать бд на mysql. Таблицы: Users и Posts с полями: 
      - Users: id, first_name, last_name
      - Posts: id, title, description, userId(ManyToOne связь с таблицей Users)
  
4. Создать express сервер в файле index.js 

5. Прописать эндпоинты Rest Api (Можно с помощью express router, можно в самом index.js файле):
    - /api/Users/list - возвращает данные всех пользователей что есть в базе
    - /api/Posts/list - вовзращает данные всех постов что есть в базе
    - /api/Posts/:id - возвращает данные поста, имеющего переданный id (передавать id можно или в параметрах запроса или в query параметрах)

6. Залить код на свой репозиторий.
