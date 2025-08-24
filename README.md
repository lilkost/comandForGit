## Установка и настройка Git

1. Настрой имя и email (один раз):


    git config --global user.name "Твоё Имя"
    git config --global user.email "твой@email.com"


2. Проверить настройки:


- git config --list

## Создание и инициализация репозитория

1. Создай папку проекта:
- mkdir myproject
- cd myproject

2. Инициализируй Git:
- git init

3. Добавь файлы:
- echo "Hello world" > README.md
- git add README.md
- git commit -m "Первый коммит"

## Основные команды Git

1. Добавление изменений в индекс (staging):

- git add <файл>        # добавить один файл
- git add .             # добавить все изменения

2. Создание коммита:
- git commit -m "описание изменений"

3. Просмотр истории:
- git log --oneline --graph --decorate --all

4. Статус изменений:
- git status

5. Отмена изменений:

- git checkout -- <файл>   # вернуть файл к последнему коммиту
- git reset HEAD <файл>    # убрать из staging