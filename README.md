# lab2
1) Создайте пустой репозиторий на сервисе github.com (или gitlab.com, или bitbucket.com).
```
~$ sudo apt update
~$ sudo apt install git
~/Рабочий стол$ git config --global user.email "karpina.katia@gmail.com"
~/Рабочий стол$ git config --global user.name "Карпина Екатерина"
```
[task2.1](task2.1)  
2) Выполните инструкцию по созданию первого коммита на странице репозитория, созданного на предыдещем шаге.
```
~/projects/MyRepository$ git init
>> Инициализирован пустой репозиторий Git в /home/ekaterina/projects/MyRepository/.git/
~/projects/MyRepository$ git remote add origin https://github.com/Ekaterina416b/MyRepository.git
~/projects/MyRepository$ touch README.md
~/projects/MyRepository$ git add README.md
~/projects/MyRepository$ git commit -m "first commit"
>>[master (корневой коммит) abaf6cf] first commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
~/projects/MyRepository$ git push -u origin master
>>Username for 'https://github.com': Ekaterina416b
Перечисление объектов: 3, готово.
Подсчет объектов: 100% (3/3), готово.
Запись объектов: 100% (3/3), 241 байт | 241.00 КиБ/с, готово.
Всего 3 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
To https://github.com/Ekaterina416b/MyRepository.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.
```
3) Создайте файл hello_world.cpp в локальной копии репозитория (который должен был появиться на шаге 2). Реализуйте программу Hello world на языке C++ используя плохой стиль кода. Например, после заголовочных файлов вставьте строку using namespace std;
```
~/projects/MyRepository$ touch hello_world.cpp
~/projects/MyRepository$ nano hello_world.cpp
```
[hello_world.cpp](https://github.com/Ekaterina416b/MyRepository/blob/main/hello_world.cpp)
4) Добавьте этот файл в локальную копию репозитория.
```
~/projects/MyRepository$ git add hello_world.cpp
```
5)Закоммитьте изменения с осмысленным сообщением
```
git commit -m "Add Hello World program in C++"
>>  World program in C++"
[master a681570] Add Hello World program in C++
 1 file changed, 7 insertions(+)
 create mode 100644 hello_world.cpp
~/projects/MyRepository$ git push origin master
Перечисление объектов: 4, готово.
Подсчет объектов: 100% (4/4), готово.
При сжатии изменений используется до 2 потоков
Сжатие объектов: 100% (3/3), готово.
Запись объектов: 100% (3/3), 430 байтов | 430.00 КиБ/с, готово.
Всего 3 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
To https://github.com/Ekaterina416b/MyRepository.git
   abaf6cf..a681570  master -> master
```
6) Изменитьте исходный код так, чтобы программа через стандартный поток ввода запрашивалось имя пользователя. А в стандартный поток вывода печаталось сообщение Hello world from @name, где @name имя пользователя.
```


