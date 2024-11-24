# LR6
Лабораторная работа №6
# Отчёт по выполнению лабораторной работы
## 1. Цель работы
Изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.
## 2. Ход работы
1. Делаем форк репозитория в личное хранилище.

2. Настраиваем клиент git, введя имя пользователя  `git config --global user.name "4319 Сирина А.С."` и email `git config --global user.email "sir2510@mail.ru"`.</br>
![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/1.jpg)
3. Клонируем личный удаленный репозиторий на компьютер `git clone https://github.com/sirinaaaa/LR6.git`.</br>
   ![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/2.jpg)
4. Добавляем файл через интерфейс GitHub и подтягиваем изменения в локальный репозиторий `git pull`. </br>
![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/3.jpg)</br>
   ![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/4.jpg)

5. Получаем историю операций для каждой ветки `git log`.</br>
   ![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/6.jpg)</br>
![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/7.jpg)

6. Смотрим последние изменения `git status`.</br>
![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/8.jpg)
7. Выполняем слияние и разрешаем конфликт.</br>
   7.1. Переходим в ветку master `git checkout master`, выполняем слияние `git merge origin/branch1` и получаем ошибку.</br>
   ![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/9.jpg)</br>
   7.2. Исправляем файл.</br>
   ![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/11.jpg)</br>
   7.3. Добавляем содержимое рабочего каталога в индекс для последующего коммита `git add mergefile.txt`, проверяем была ли исправлена ошибка `git status` и делаем коммит `git commit -m "разрешение конфликта"`.</br>
         ![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/10.jpg)</br>

9. Удаляем побочную ветку branch1 `git push origin --delete branch1`.</br>
![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/12.jpg)
10. Делаем изменения и фиксируем их, оставляя комментарии, несколько раз `git add -A`, `git commit -m "комментарий"`.</br>
   ![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/13.jpg)</br>
![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/14.jpg)
11. Делаем откат коммита `git reset --hard HEAD~`.</br>
   ![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/15.jpg)

12. Создаем ветку для отчета `git branch report`. переходим в нее `git checkout report` и отправляем в удаленный репозиторий `git push origin report`.</br>
   ![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/16.jpg)</br>
![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/17.jpg)

13. Получаем историю операций в форматированном виде `git log --pretty=format:"%h %ad %an %s" --graph --date=short`.</br>
![](https://github.com/sirinaaaa/LR6/blob/master/%D1%81%D0%BA%D1%80%D0%B8%D0%BD%D1%8B/18.jpg)</br>
14. Отправляем локальные изменения в сетевое хранилище GitHub `git push`.

## 3. Лог команд

Список команд, использованных в процессе работы:

`git config --global user.name "4319 Сирина А.С."` — настройка клиента git </br>
`git config --global user.email "sir2510@mail.ru"` — настройка клиента git </br>
`git clone https://github.com/sirinaaaa/LR6.git` — клонирование личного репозитория на компьютер </br>
`git pull` — подтягивание изменений в локальный репозиторий </br>
`git log` — получение истории операций </br>
`git log origin/branch1` — получение истории операций </br>
`git status` — проверка последних изменений </br>
`git checkout master` — переход в ветку master </br>
`git merge origin/branch1` — слияние веток </br>
`git add mergefile.txt` — сохранение файла mergefile.txt </br>
`git commit -m "разрешение конфликта"` — создание коммита </br>
`git add -A` — добавление содержимого рабочего каталога в индекс </br>
`git commit -m "комментарий"` — создание коммита с нужным комментарием </br>
`git reset --hard HEAD~` — откат коммита </br>
`git branch report` — создание новой ветки report </br>
`git checkout report` — переход в ветку report </br>
`git push origin report` — отправление ветки в удаленный репозиторий </br>
`git log --pretty=format:"%h %ad %an %s" --graph --date=short` — история операцие в форматированном формате </br>
`git push` — отправление локальных изменнений в сетевое хранилище 

## 4. Вывод
Я изучила базовые возможности системы управления версиями, получила опыт работы с Git Api и опыт работы с локальным и удаленным репозиторием.




   
   
