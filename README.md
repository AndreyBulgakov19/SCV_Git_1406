# Репозиторий для **pull request**
* В своём аккаунте на GitHub создать копию репозитория **"AndreyBulgakov19
/SCV_Git_1804"** с помощью кнопки **"Fork"**.
---
* Клонировать копию репозитория на локальный компьютер.
---
* Создать новую ветку.
---
* Добавить файл с инструкцией в новую ветку.
---
* Дополнить инструкцию разделами по работе с удалёнными репозиториями, pull request.
---
* Зафиксировать изменения (коммиты).
---
* Отправить изменения на GitHub.
---
* На сайте GitHub выполнить **Pull request**.
---
# Работа с GIT
## 1. Проверка наличия установленного GIT
В терминале выполнить команду `git version`.
Если ***Git*** установлен, появится сообщение с информацией о версии программы. Иначе будет сообщение об ошибке. 

## 2. Установка Git
Загружаем последнюю версию Git с сайта https://git-scm.com/downloads. 
Устанавливаем с настройками по умолчанию.

## 3. Настройка Git
При первом использовании *Git* необходимо представиться. Для этого нужно ввести в термигале две команды :
```
git config --global user.name "Your name"
git config --global user.email ваша "почта@example.com"
``` 
## 4. Создание репозитория
Получить репозиторий можно двумя способами.
1. В терминале переходим к папке, в которой хотим создать репозиторий. Выполним команду:
```
git init
```
В исходной папке появится скрытая папка *.git*

2. Клонировать существующий репозиторий Git из любого места. Сделать это можно так:
```
git clone (адрес репозитория)
```

## 5. Запись изменений в репозиторий
Каждый файл в рабочей папке может находиться в одном из двух состояний: под версионном контроле (отслеживаемые - tracked) и нет (untracked).

## 6. Просмотр истории коммитов
Отслеживаемые файлы могут быть неизмененными, измененными или подготовленными к комиту.
Чтобы посиотреть состояние файлов в репозитории необходимо выполнить команду: 
```
git status
```

Для того, чтобы начать отслеживать новый файл, используется команда:
```
git add "имя файла с расширением"
```

Для просмотра истории коммитов используется команда
```
git log
```


## 7. Инструкция по добавлению изображения
Для того, чтобы добавить изображение необходимо сделать следующее: Если фотографияяизображение не отобразится на экране, нам необходимо заключить в квадратные скобки описание этого изображения, далее в круглых скобках заключить прямую ссылку на это изображение.
```
![описание изображения](прямая ссылка на это изображение)
```
Например : 
![воздушный шар](7_5234234.jpg)

## 8. Игнорирование файлов
Чтобы игнорировать файл, для которого ранее был сделан коммит, необходимо удалить этот файл из репозитория, а затем добавить для него правило в **. gitignore** . Необходимо использовать команду **git rm** с параметром **--cached** , чтобы удалить этот файл из репозитория, но оставить его в рабочем каталоге как игнорируемый файл.

**. gitignore** нужен для скрытия файлов и папок от системы контроля версий Git. Обычно скрывают конфигурационные файлы (особенно с паролями), временные файли и папки. **gitignore** использует ***glob*** формат для выборки файлов.

## 9. Удаление ветки в Git
Когда после слива каких-то изменений из рабочей ветки в исходную версию проекта, ее, необходимо удалить, чтобы она более не мешалась в коде. 
Для локально расположенных веток существует команда:
```
git branch -d local_branch_name
```
Где флажок -d являющийся опцией команды **git branch** - это сокращенная версия ключевого слова **--delete**, предназначенного для удаления ветки, а **local_branch_name** – название ненужной ветки.
Однако удалить текущую ветку, которая в данный момент просматривается - нельзя. Если же все-таки попытаться это сделать, система отругает и выдаст ошибку с таким содержанием:
```
Error: Cannot delete branch local_branch_name checked out at название_директории
```
## 10. Исправление коммита
Если произошла опечатка в комментарии или забыли добавить файл и заметили это сразу после того, как закоммитили изменения, легко можно это поправить при помощи **commit —amend**. Эта команда добавит все из последнего коммита в область подготовленных файлов и попытается сделать новый коммит. Это дает возможность поправить комментарий или добавить недостающие файлы в область подготовленных файлов.
Для более сложных исправлений, например, не в последнем коммите или если уже успели отправить изменения на сервер, нужно использовать **revert**. Эта команда создаст коммит, отменяющий изменения, совершенные в коммите с заданным идентификатором.
Самый последний коммит может быть доступен по алиасу **HEAD**:
```
git revert HEAD
```
## 11 Инструкция создания ветки в Git
Для того чтобы создать новую ветку в **Git** необходимо совершить команду:
```
git branch new_branch_name
``` 
Следующая команда позволяет создать и сразу переключиться на эту ветку.
```
git checkout -b "branch name"
```
Если мы хотим переключиться на ветку, мы вводим команду:
```
git checkout branch_name
```

## 12 Инструкция слияния веток на Git
Для того, чтобы выполнить слияние ветки после добавления изменений на **Git** нам необходимо ввести команду:
```
git merge branch_name
```
Совершаем слияние из главной ветки master.

## 13 Разрешение конфликта в Git
После того как произошло слияние веток, возможен конфликт между этими ветками. Для того, чтобы разрешить конфликт нам необходимо выбрать из двух веток вариант написания, который нам больше подходить, затем нажать на выбор - оставить текущую версию, перейти на другую версию или объединить обе версии.
После того, как конфликт был разрешен, необходимо закоммитить изменения.

## 14 Работа с удаленными репозиториями

1. Создать аккаунт на GitHub.
2. Создать локальный репозиторий.
3. Связать удаленный репозиторий с локальным.
4. Создаем ветку.
5. Вноисм изменения и коммиты.
6. Отправляем изменения на GitHub.
7. Создаем Pull Request.

