# Инструкция по GIT на простом языке:
GIT by DragonDamage

### Ссылки на скачивание самого ПО:


https://git-scm.com/download/win - Windows

https://git-scm.com/download/linux - Linux

https://git-scm.com/download/mac - Mac
_______________________________________________________________________________________________________________________________________________________________________

> Если с нуля, то:

`$ mkdir Desktop/name_repository/` - создаем папку-репозиторий

`$ cd Desktop/name_repository/` - переходим в неё

`$ git init` - приклеиваемся к репозиторию (делаем папку репозиторием для Git)
_______________________________________________________________________________________________________________________________________________________________________

> Если репозиторий уже есть, то:

`$ git clone https://github.com/DragonDamage/Git-instruction.git`

Результатом клонирования появится папка Git-instruction в данном случае
_______________________________________________________________________________________________________________________________________________________________________

> Если уже есть локальная копия, то можно обновить в ней изменения сделанные удаленно в ветке develop/master другими разработками, командой:

`$ git pull origin develop` или `master`

`$ git checkout develop` или `$ git checkout master` - переключиться на нужную ветку
_______________________________________________________________________________________________________________________________________________________________________

Далее первичные настройки:

`$ git config --global user.name "Name"` - вводим имя

`$ git config --global user.email mail@mail.ru` - вводим меил

`$ git config --list` - посмотреть все конфиги

`$ git config --global color.ui true` - настройка подцветки

`$ git config --global color.status auto` - настройка подцветки статусов

`$ git config --global color.branch auto` - настройка подцветки веток

.

> Git готов к работе, можешь производить свои изменения или же проект с нуля

.

Дальнейшие действия, после внесения твоих изменений:

`$ git status` – показать какие файлы были изменены

`$ git add —-all` – добавить все изменения

`$ git status` – убедиться что изменения видны и стали зелёными

`$ git commit –m “add change”` – коммитим и ставим комментарий

`$ git push –u origin develop` или `master` – заливаем (пушим) изменения на ветку `develop` или `master`

### Готово :+1:


# О файле .gitignore

Данный файл можно создать в репозитории, и он будет игнорировать коммиты файлов, которые ты туда запишешь. (каждая папка/файл на новой строке) Пример заполнения:
```
folder1/
node.js
*.log
```

# Работа с ветками (branches)

`$ git branch -a` - посмотреть все ветки проекта

`$ git branch <name-branch>` - создать новую ветку

`$ git checkout <name-branch>` - переключиться в нужную ветку

`$ git merge <name-branch>` - обьединить ветку и все изменения с веткой `master` (выполняется из ветки `master`)

`$ git branch -d <name-branch>` - удалить ветку

`$ git reset --hard <хэш коммита>` - перейти на нужный коммит, игнорируя предыдущие


# Дополнительные команды:

`$ git add <File-1> <File-2>` - добавить только 2 файла в коммит

`$ git log` - посмотреть историю коммитов (HEAD - это последний коммит)

`$ git show <хэш коммита>` - показать что это был за коммит

`$ git restore <название файла>` - отменить изменения до предыдущего коммита

`$ git restore --staged <file>` - отменить изменения до предыдущего коммита, которые уже подготовлены для следующего коммита

`$ git diff` - показать все изменения в файлах

`$ git diff --staged` - показать все изменения, которые уже подготовлены для коммита

`$ git commit -am "add change"` - добавляем и коммитим все изменения + ставим комментарий

`$ git mv <file> <file1>` - переименовать файл

`$ git mv <file> </folder/file1>` - переименовать и перенести файл в другую директорию + выполнение git add автоматически

`$ git rm <file>` - удалить файл

`$ git reset` - вытащить из коммита

`$ git remote add origin https://github.com/DragonDamage/Git-instruction.git` - подключение к локальному репозиторию (origin - главный)

`$ git remote -v` - посмотреть репозитории локально

`$ git fetch origin` - скачать недостающие коммиты

`$ git merge origin` или `master` - увидеть недостающие коммиты

`$ git rebase master` - забрать изменения из `master` в ту ветку, в которой находишься

`$ git push origin master -f` - переписать историю ветки в которой находишься в ветку `master`

`$ git tag <name tag>` - добавить простой тэг к коммиту

`$ git tag -a <name tag> -m "<you comment>"` - добавить подробный тэг к коммиту

`$ git push --tags` - отправить все тэги на сервер 


> Полезно для твоей ветки `master` в github.com (чтобы никто не сделал force push master)

#### Settings -> Branches -> Add rule -> вводим: master -> create
