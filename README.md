# lab2
<details>
 <summary>Part1</summary>
 <p>
1)Создайте пустой репозиторий на сервисе github.com (или gitlab.com, или bitbucket.com). 

2)Выполните инструкцию по созданию первого коммита на странице репозитория, созданного на предыдещем шаге. 
```
Documents % mkdir MyRepo
cd MyRepo
echo "MyRepo">> README.md
git init
>>Initialized empty Git repository in /Users/makbuk/Documents/MyRepo/.git/
git config user.name "Ekaterina Karpina"
git config user.email "karpina.katia@gmail.com"
git add README.md
git commit -m "first commit"
>>[main (root-commit) d220c65] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
git branch -M master
git remote add origin https://github.com/Ekaterina416b/MyRepo.git
>>makbuk@MacBook-Air-makbuk MyRepo % git push -u origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 225 bytes | 225.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Ekaterina416b/MyRepo.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.
```
3)Создайте файл hello_world.cpp в локальной копии репозитория (который должен был появиться на шаге 2). Реализуйте программу Hello world на языке C++ используя плохой стиль кода. Например, после заголовочных файлов вставьте строку using namespace std;.
```
touch hello_world.cpp
nano hello_world.cpp
```
[hello_world.cpp](hello_world.cpp)

4)Добавьте этот файл в локальную копию репозитория.
```
git add hello_world.cpp
```
5)Закоммитьте изменения с осмысленным сообщением. 
``` 
git commit -m "Add hello_world.cpp with bad code style"
>>[master acc580f] Add hello_world.cpp with bad code style
 1 file changed, 7 insertions(+)
 create mode 100644 MyRepository/hello_world.cpp
``` 

6,7)Изменитьте исходный код так, чтобы программа через стандартный поток ввода запрашивалось имя пользователя. А в стандартный поток вывода печаталось сообщение Hello world from @name, где @name имя пользователя.Закоммитьте новую версию программы. Почему не надо добавлять файл повторно git add?
```
git commit -am "Update hello_world.cpp to ask for user's name"
>>[master 5aa4647] Update hello_world.cpp to ask for user's name
 1 file changed, 5 insertions(+), 1 deletion(-)
```
Флаг -a автоматически добавляет изменения в уже отслеживаемых файлах, поэтому git add не требуется.
8)Запуште изменения в удалёный репозиторий.
```
git push origin master
>>Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (8/8), 948 bytes | 948.00 KiB/s, done.
Total 8 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Ekaterina416b/MyRepository.git
   3c5a746..5aa4647  master -> master
```

9)Проверьте, что история коммитов доступна в удалёный репозитории.  
[Ссылка на коммиты](https://github.com/Ekaterina416b/MyRepo/commits/master/) 
 </p>
</details>
 <details>
 <summary>Part2</summary>
 <p>
 1)В локальной копии репозитория создайте локальную ветку patch1.
  
 ```
 MyRepository % git checkout -b patch1
 >>Switched to a new branch 'patch1'
 ```
 2)Внесите изменения в ветке patch1 по исправлению кода и избавления от using namespace std;.
 ```
 nano hello_world.cpp
 ```
 3)commit, push локальную ветку в удалённый репозиторий.
 ```
 git add hello_world.cpp
 git commit -m "Remove using namespace std; and improve code style"
>>[patch1 9a3bf03] Remove using namespace std; and improve code style
 1 file changed, 5 insertions(+), 5 deletions(-)
git push origin patch1
>>Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 476 bytes | 476.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'patch1' on GitHub by visiting:
remote:      https://github.com/Ekaterina416b/MyRepo/pull/new/patch1
remote: 
To https://github.com/Ekaterina416b/MyRepo.git
 * [new branch]      patch1 -> patch1
```
 4)Проверьте, что ветка patch1 доступна в удалёный репозитории. 
 
 [Ссылка на ветку](https://github.com/Ekaterina416b/MyRepo/commits/patch1/) 
 
 5)Создайте pull-request patch1 -> master.
 <img width="929" alt="scrin 2 5" src="https://github.com/user-attachments/assets/9b2f2605-d764-4c16-a84c-ee9499217697" />

6)В локальной копии в ветке patch1 добавьте в исходный код комментарии.
```
nano hello_world.cpp
```
7)commit, push.
```
git add hello_world.cpp
git commit -m "Add comments to the code"
>>[patch1 04b01bb] Add comments to the code
 1 file changed, 1 insertion(+), 1 deletion(-)
git push origin patch1
>>Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 338 bytes | 338.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Ekaterina416b/MyRepo.git
   9a3bf03..04b01bb  patch1 -> patch1
```
8)Проверьте, что новые изменения есть в созданном на шаге 5 pull-request
<img width="935" alt="scrin  2 8" src="https://github.com/user-attachments/assets/2e0e56a2-fafe-49d1-af3c-65bf47394f62" /> 

9) В удалённый репозитории выполните слияние PR patch1 -> master и удалите ветку patch1 в удаленном репозитории.
<img width="958" alt="scrin 2 9" src="https://github.com/user-attachments/assets/8c9830b9-84d2-4e0d-8c34-6517d8018614" />

10)Локально выполните pull.
```
git checkout master
>>Switched to branch 'master'
Your branch is up to date with 'origin/master'.
git pull origin master              
>>remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 918 bytes | 459.00 KiB/s, done.
From https://github.com/Ekaterina416b/MyRepo
 * branch            master     -> FETCH_HEAD
   f14591f..6ac9698  master     -> origin/master
Updating f14591f..6ac9698
Fast-forward
 hello_world.cpp | 10 +++++-----
 1 file changed, 5 insertions(+), 5 deletions(-)
```
11)С помощью команды git log просмотрите историю в локальной версии ветки master.
```
git log
```
[task2.11.txt](https://github.com/Ekaterina416b/lab2.1/blob/master/task2.11.txt) 

12)Удалите локальную ветку patch1.
```
git branch -d patch1
>>Deleted branch patch1 (was 04b01bb)
```
</p>
</details>
<details>
 <summary>Part3</summary>
 <p>
1)Создайте новую локальную ветку patch2.
  
```
git checkout -b patch2
>>Switched to a new branch 'patch2'
```
2)Измените code style с помощью утилиты clang-format. Например, используя опцию -style=Mozilla.
```
clang-format -i -style=Mozilla hello_world.cpp
```
3)commit, push, создайте pull-request patch2 -> master.
```
git add hello_world.cpp
git commit -m "Apply Mozilla code style to hello_world.cpp using clang-format"
>>[patch2 95f3087] Apply Mozilla code style to hello_world.cpp using clang-format
 1 file changed, 8 insertions(+), 7 deletions(-)
git push origin patch2
>>Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 494 bytes | 494.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'patch2' on GitHub by visiting:
remote:      https://github.com/Ekaterina416b/MyRepo/pull/new/patch2
remote: 
To https://github.com/Ekaterina416b/MyRepo.git
 * [new branch]      patch2 -> patch2
```
4,5)В ветке master в удаленном репозитории измените комментарии, например, расставьте знаки препинания, переведите комментарии на другой язык.
Убедитесь, что в pull-request появились конфликтны.
<img width="986" alt="scrin 3 4" src="https://github.com/user-attachments/assets/18b497da-d592-4b15-be11-023db61b8f25" /> 


6)Для этого локально выполните pull + rebase (точную последовательность команд, следует узнать самостоятельно). Исправьте конфликты.
```
git pull --rebase origin master
nano hello_world.cpp
git add hello_world.cpp
git rebase --continue
```
7)Сделайте force push в ветку patch2
```
git push origin patch2 --force-with-lease
```
8)Убедитель, что в pull-request пропали конфликтны.

<img width="907" alt="Снимок экрана 2025-03-16 в 19 07 36" src="https://github.com/user-attachments/assets/510da74f-dced-4b48-b20e-785a68d529ca" />

9)Вмержите pull-request patch2 -> master.
<img width="928" alt="Снимок экрана 2025-03-16 в 18 51 13" src="https://github.com/user-attachments/assets/b687ce2f-fee5-4a2c-8bb7-871add62fad0" />
</p>
</details>
