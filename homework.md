# Homework - инструкцию по работе с Git #

## Основные команды: ##

1. git add - команда git add добавляет содержимое рабочего каталога в индекс (staging area) для последующего коммита

2. git status - команда git status показывает состояния файлов в рабочем каталоге и индексе: какие файлы изменены, но не добавлены в индекс; какие ожидают коммита в индексе.

3. git commit - команда git commit берёт все данные, добавленные в индекс с помощью git add, и сохраняет их слепок во внутренней базе данных, а затем сдвигает указатель текущей ветки на этот слепок.

4. git reset - команда git reset, как можно догадаться из названия, используется в основном для отмены изменений.

5. git clean - команда git clean используется для удаления мусора из рабочего каталога.

6. git init - команда создает новый репозиторий Git. С ее помощью можно преобразовать существующий проект без управления версиями в репозиторий Git или инициализировать новый пустой репозиторий.

7. git log - перечисляет коммиты, сделанные в репозитории в обратном к хронологическому порядке — последние коммиты находятся вверху.

8. git checkout -  позволяет перемещаться между ветками, созданными командой git branch

## Ветви в git:

1. git branch - позволяет создавать, просматривать, переименовывать и удалять ветки. Она не дает возможности переключаться между ветками или выполнять слияние разветвленной истории.
Создать ветку можно командой в терминале git branch <Название новой ветки> (без ковычек)
 Удалить ветвь можно командой в терминале git branch -d <название ветви> (без ковычек)

2.  git checkout - позволяет перемещаться между ветками, созданными командой git branch. К примеру: git checkout <название ветки> (без ковычек)

3. git merge - выполняет слияние отдельных направлений разработки, созданных с помощью команды git branch , в единую ветку. К примеру: git merge <название ветки> (без ковычек)

## Добавление картинок:
Чтобы вставить изображение в текст, достаточно написать следующее:

![текст к картинке] (название картинки находящейся в папке с репозиторием, к примеру: DHD00833.jpg)

## При каждом новом репозитории вводить после git init:
* git config --global user.email (email) (без скобочек)
* git config --global user.name (name) (без скобочек)

## Списки
Чтобы выделить ненумерованный список, используйте (*) или (+)
К примеру:
* Элемент 1
* Элемент 2
+ Элемент 3

## Конфликт изменений
При работе в двух ветках одновременно может
возникнуть ситуация, когда в одной и другой
ветке мы по-разному изменили блок текста.


## Работа с удаленными репозиториями

 __Как настроить совместную работу:__
1. Создать аккаунт на GitHub.com
2. Создать локальный репозиторий
3. “Подружить” ваш локальный и удалённый репозитории.
 GitHub при создании нового репозитория подскажет, как это можно сделать
4. Отправить (push) ваш локальный репозиторий в удалённый (на GitHub), при этом, возможно,
вам нужно будет авторизоваться на удалённом репозитории
5. Провести изменения “с другого компьютера”
6. Выкачать (pull) актуальное состояние из удалённого репозитория

__Необходимые команды:__

1. git pull - Эта команда позволяет скачать все 
из текущего репозитория и автоматически
сделать merge с нашей версией (она не только
загружает все изменения, но и пытается слить
все ветки на локальном компьютере и в
удаленном репозитории).

2. git push - команда позволяет отправить нашу
версию репозитория на внешний
репозиторий. ТРЕБУЕТ АВТОРИЗАЦИИ
на внешнем репозитории.

3. git clone - команда для выбора существующего репозитория и создания его клона, т. е. копии.

## pull request
* команда для предложения изменений
* запрос на вливание изменений в репозиторий

В больших компаниях один ответственный за проект создает аккаунт. Другие пользователи дают
команду pull request. Предлагать изменения на GitHub нужно в отдельной ветке. Сначала
пользователь копирует репозиторий на свой компьютер, делает fork репозитория, затем
клонирует версию на своём ПК, создаёт ветку с предлагаемыми изменениями, отправляет
изменения командой push в свой аккаунт на GitHub и даёт команду pull request.

__Как сделать pull request:__
* Делаем fork (ответвление) репозитория
* Делаем git clone своей версии репозитория
* Создаем новую ветку и в НЕЕ вносим свои изменения
* Фиксируем изменения (делаем коммиты)
* Отправляем свою версию в свой GitHub
* На сайте GitHub нажимаем кнопку pull request