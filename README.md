## Установка и настройка Git

1. Настрой имя и email (один раз):


- git config --global user.name "Твоё Имя"
- git config --global user.email "твой@email.com"


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

## Работа с удалённым репозиторием (GitHub)

1. Свяжи локальный проект с GitHub:

- git remote add origin https://github.com/username/myproject.git
- git branch -M main    # Переименуем ветку master -> main - (рекомендовано)
- git push -u origin main

2. В будущем пушить изменения:
- git push

## Ветки (branches)
1. Создать ветку:
- git branch feature

2. Переключиться на неё:
- git checkout feature

3. Создать и переключиться сразу:
- git checkout -b feature

4. Слить изменения:
- git checkout main
- git merge feature

## Работа с GitHub и командой

1. Клонирование чужого проекта:
- git clone https://github.com/user/repo.git

2. Обновление своего проекта:
- git pull

3. Pull Request (PR):

Создаёшь ветку → коммитишь → пушишь на GitHub → создаёшь PR через веб-интерфейс.

--- 

### Продвинутые команды и техники

1. Git stash — временно сохранить изменения:
- git stash
- git stash pop

2. Rebase (переписывание истории):
- git checkout feature
- git rebase main

3. Interactive rebase (слияние коммитов):
- git rebase -i HEAD~3

4. Cherry-pick (взять отдельный коммит):
- git cherry-pick <hash>

5. Tags (теги для релизов):
- git tag v1.0
- git push origin v1.0