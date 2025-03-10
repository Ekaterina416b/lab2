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
