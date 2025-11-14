# LR6

Лабораторная работа №6



\*\*Цель лабораторной работы: изучение базовых возможностей системы

управления версиями, опыт работы с Git Api, опыт работы с локальным и

удаленным репозиторием.\*\*



Логи команд:
# Пункты 1-6

`git config --global user.name "Юрчик Артем 4415"`

`git config --global user.email "arteryurchik330@gmail.com"`

`cd C:/Users/Floukt/Desktop/Лабы/ОП`

`git clone https://github.com/Floukot/LR6.git`

`cd LR6`

`git pull origin master`

\## Пункты 7-10

`git branch -a`

`git log -p`

`git checkout -b dev`

`echo "Это изменение сделано в ветке dev" > conflict\_file.txt`

`git add .`

`git commit -m "Изменения в ветке dev: создан conflict\_file.txt"`

`git checkout master`

`echo "Это изменение сделано в ветке master" > conflict\_file.txt`

`git add .`

`git commit -m "Изменения в ветке master: конфликтующее содержимое"`

`git merge dev`

`git add conflict\_file.txt`

`git commit -m "Разрешил конфликт слияния с веткой dev"`

`git branch -d dev`

\### Пункты 11-13

`echo "Первое изменение - создание файла" > local\_changes.txt`

`git add .`

`git commit -m "Первое локальное изменение: создан файл local\_changes.txt"`

`echo "Второе изменение - добавлена новая строка" >> local\_changes.txt`

`git add .`

`git commit -m "Второе локальное изменение: добавлена строка в файл"`

`echo "Третье изменение - завершающие правки" >> local\_changes.txt`

`git add .`

`git commit -m "Третье локальное изменение: финальные правки"`

`git reset --soft HEAD~1`

`git status`

`git checkout -b report`

