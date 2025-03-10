# lab2
Создайте пустой репозиторий на сервисе github.com (или gitlab.com, или bitbucket.com).
```
~$ sudo apt update
~$ sudo apt install git
~/Рабочий стол$ git config --global user.email "karpina.katia@gmail.com"
~/Рабочий стол$ git config --global user.name "Карпина Екатерина"
```
[task2.1](task2.1)  
Выполните инструкцию по созданию первого коммита на странице репозитория, созданного на предыдещем шаге.
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
