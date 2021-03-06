![git-logo](GitLogo.png)
# Работа с Git
## 1. Проверка наличия установленного Git
в терминале выполнить команду `git --version`
Если установлен, появится сообщение с информацией о версии прогрограммы. Иначе будет сообшение об ошибке

## 2. Установка Git
Загружаем последнию версию  Git с https://git-scm.com/downloads

## 3. Настройка Git 
При первом использовании Git  необходимо представится. для этого вам нужно ввести в терминале две команды
```
git config --global user.name "name"
git config --global user.email "email"
```

## 4. Создание локального репазитория
 в терминале выполнить команду `git init`
 создатся репозиторий git в выбранной папке .

 ## 5. Запись изменений в репозиторий
 в терминале выполнить команду 
 __git add "file"__
 Команда git add добавляет содержимое рабочего каталога в индекс для последующего коммита.
 если изменения сахранены файл добавится в репозиторрий.

## 6. Просмотр статуса 
 в терминале выполнить команду _git status_
 git status показывает состояния файлов в рабочем каталоге и индексе: какие файлы изменены, но не добавлены в индекс; какие ожидают коммита в индексе. Вдобавок к этому выводятся подсказки о том, как изменить состояние файлов.

 ## 7. Добавление списка изменений в репозиторий Git
 в терминале выполнить команду `git commit`
 Команда _**git commit**_  берёт все данные, добавленные в индекс с помощью git add, и сохраняет их слепок во внутренней базе данных, а затем сдвигает указатель текущей ветки на этот слепок.

## 8. Просмотр списка изменений diff
 в терминале выполнить команду `git diff`
и мы увидим разницу между сахраненным и закомиченным состоянием

## 9. Просмотр истории коммитов 
 в терминале выполнить команду *git log*
 появится все сохраненные коммиты 

 ## 10. Перемещение между сохранениями
 в терминале выполнить команду **git checkout "file_name"**
 Перейдем в выбранное состояние 

## 11. Игнорирование файлов 
Чтобы игнорировать обьемные файлы (фото, видео и.т.др) нужно создать файл 
```
.gitignore
```
и написать туда все что нужно игнорировать.
Например `photoName.png`
этот файл будет проигнорирован


## 12. Создание веток в Git 
Ветки в Git - это простой перемещаемый указатель на один из коммитов, обычно последний в цепочке коммитов. По умолчанию имя основной ветки в Git - master.
Создать ветку можно командой: 
```
git branch <new_branch_name>
```
В результате создается новый коммит.
Указатель на текуший коммит.

Чтобы при создании ветки сразу на неё переключатся используется команда
 ````
 git checkout -b <newBrancheName>
````
Список веток в репозитории можно посмотреть с помощью команды 
```
 git branch 
 ```

## 13. Слияние веток и разрешение конфликтов

Для слияния выбранной ветки  с текущей нужно выполнить команду 
```
git merge <nameSelectBranch>
```

## 14. Удаление веток 
Чтобы удалить слитую ветку нужно выполнить команду 
```
git branch -d <branchName>
```
Чтобы удалить даже не слитую ветку нужно выполнить команду 
```
git branch -D <branchName>
```
потенциально опасная команда, он удалить ветку даже если он не соединен с главной веткой

## 15. Создание удаленного репозитория и связывание с локальным репозиторием
Для начало нужно зарегистрироватся на сайте Github.com, а потом создать репозиторий Github 
для этого нужно нажать значок + и выбрать new repozitory (как на картинке)
![изображение создания репозитория](Igit.png)
написать имя репозитория и нажать на кнопку создать репозиторий
а потом поподаете страничку где вы можете следуя инструкциям связать с вашим локальным репозиторием

или у вас уже есть локальный репозиторий  можете написать эти команды и связать ваш локальный и удаленный репозиторий


```
git remote add origin https://github.com/Nurbolot02/Test.git  - связывает удаленный и локальный репо

git branch -M main - переименовывает ветку в main

git push -u origin main -  указывает на какую удаленную репо отправить данные
```

**Nurbolot02** - имя пользовотеля

*Test* - имя созданного проекта

## 16. Отправка изменений на удаленный репо (Push)

 После того как сделали коммит можете отправить изменение в удаленный репо командой 
```
git push
```
Если вы первый раз отправляете данные на удаленный репо может потребоватся авторизация

## 17. Вытягивание последнего состояние репо с удаленного репо и слияние с локальным (Pull)

Для того чтобы вытинуть последнее состояние с удаленного репо вводим команду 
```
git pull
```
после этого с удаленного репо выкачается последнее состояние репо и произойдет слияние с локальным репо

## 18. запрос на вливание изменений из вашей ветки в основную ветку исходного репозитория (Pull request)

* В своём аккаунте на GitHub создать копию репозитория  с помощью кнопки **"Fork"**.
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








 


