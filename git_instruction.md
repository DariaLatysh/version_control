# Подсказка для работы с GIT

## Создание репозитория
Берем локальный каталог, который не находится под версионным контролем, и превращаем его в репозиторий.

Иноциализация: указываем папку, в которой GIT начнет отслеживать изменения, в папке создается скрытая папка .git.
```sh
git init
```

## Текущее состояние GIT
Посмотреть текущее состояние GIT , есть ли изменения, которые необходимо сохранить.
```sh
git status
```

## Добавление собержимого
Эта команда добавляет собержимое рабочего каталога в индекс для последующего коммита.
```sh
git add name.txt
```

## Зафиксировать или сохранить
Эта команда берет все данные, добавленные в индекс с помощью git add, и сохраняет их слепок во внутренней базе данных, а атем сдвигает указатель текущей ветки на этот слепок.
```sh
git commit -m "Message"
```

## Журнал изменений
Перед переключением версий файла в GIT используйте эту команду, чтобы увидеть количество сохранений.
```sh
git log
```
Журнал изменений, показывающей количество сохранений с сокращенными индексами.
```sh
git log --oneline
```

## Переключение между ветками
Для работы необходимо указать не только интересующую вас верку, но и вернуться в ту ветку, где работаем. 
```sh
git checkout name_branch
```
Также при помощи данной команды можно переключаться между коммитами.

## Разница 
Показывает разницу между текущим файлом и сохраненным.
```sh
gif diff
```

## Создание ветки
Этой командой можно создать новую ветку, делать это необходимо в папке с репозиторием.
```sh
git branch new_branch
```

## Список веток
Эта коменда выводит список веток в репозитории.
```sh
git branch
```

## Удачение ветки
С помощью этой команды можно удалить ветку.
```sh
git branch -d new_branch
```

## Слияние веток
С помощью этой команды можно слить любую ветку с текущей.
```sh
git merge name_branch
```

## Коммиты в виде древа
Эта команда выводит на экран список коммитов в виде красивого графического дерева.
```sh
git log --graph
```
Показывает сптсок коммитов в виде красивого графического дерева с сокращенными индексами.
```sh
git log --oneline --graph
```

## Работа с удаленными репозиториями

Пр запуске команды git init всё происходит только в локальном репозитории: в папке на компьютере пользователя, эту папку создавшего.

### Копирование
Копировать внешний репозиторий на свой ПК.
```sh
git clone <Адрес репозитория, который копируем>
```
Команда git clone состовная: она не только загружает все изменения, но и пытается слить все ветки на локальном компьютере и в удаленном репозитории.

### Выкачать
Эта команда позволяет скачать все из текущего репозитория и автоматически сделать merge с нашей версией.
```sh
git pull
```

### Отправить
Отправить свою версию репозитория во внешний репозиторий.
```sh
git push
```
При первои её использовании нужна авторизация на внешнем репозитории.

### Как настроить совместную работу
1. Создать аккаунт на GitHub.com.
2. Создать локальный репозиторий.
3. "Подружить" ваш локальный и удаленный репозитории. GitHub при первом создании нового репозитория подскажет, как это сделать.
4. Отправить (push) ваш локальный репозиторий в удаленный (на GitHub), при этом, возможно, вам нужно авторизоваться на удаленном репозитории.
5. Провести изменения "с другого компьютера".
6. Выкачать (pull) актуальное состояние из удаленного репозитория.

### Предложить изменения
Запрос на вливание изменений в репозитории.
```sh
pull request
```
В больших компаниях один ответсвенный за проект создает аккаунт. Другие пользователи дают команду pull request. Предлагать изменения на GitHub нужно в отдельной ветке. Сначала пользователь копирует репозиторий на свой компьютер, делает fork репозитория, затем клонирует версию на свой ПК, создает ветку с предлагаемыми изменениями, отправляет изменения комендой push в свой аккаунт на GitHub и дает команду pull request.

### Как создать pull request
1. Делаем fork (ответвление) репозитория.
2. Делаем git clone своей версии репозитория.
3. Создаем новую ветку и в неё вносим свои изменения.
4. Фиксируем изменения (делаем коммиты).
5. Отправляем свою версию в свой GitHub.
6. На сайте GitHub нажимаем кнопку pull request.