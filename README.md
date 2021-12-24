# BRANCHES
**Git HW repository to learn branches, merges, etc**

0. Переходим в папку, куда будем клонировать репозиторий для работы.
```
Command: cd /Users/macintosh/Desktop/CODING/KSENDZOV
```
0.1. Клонируем.
```
Command: git clone git@github.com:PaulBuzz/GITHW3.git
Result: Клонирование в «GITHW3»…
Enter passphrase for key '/Users/macintosh/.ssh/id_rsa': 
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Получение объектов: 100% (3/3), готово.
```
0.2. Заходим в эту папку.
```
Command: cd GITHW3
```
0.3. Проверяем, что мы в ветке main.
```
Command: git branch
Result: * main
```
1. На локальном репозитории сделать ветки для:
- Postman
- Jmeter
- CheckLists
- Bug Reports
- SQL
- Charles
- Mobile testing
```
Command: git branch postman; git branch jmeter; git branch checklists; git branch bug_reports; git branch sql; git branch charles; git branch mobile_testing
```
- Проверяем, что все ветки создались:
```
Command: git branch
Result:  bug_reports
  charles
  checklists
  jmeter
* main
  mobile_testing
  postman
  sql
```
2. Запушить все ветки на внешний репозиторий
```
Command: git push -u origin postman
Command: git push -u origin jmeter
Command: git push -u origin checklists
Command: git push -u origin bug_reports
Command: git push -u origin sql
Command: git push -u origin charles
Command: git push -u origin mobile_testing
Result: Enter passphrase for key '/Users/macintosh/.ssh/id_rsa': 
Всего 0 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
remote: 
remote: Create a pull request for 'charles' on GitHub by visiting:
remote:      https://github.com/PaulBuzz/GITHW3/pull/new/charles/
remote: 
To github.com:PaulBuzz/GITHW3.git
 * [new branch]      charles -> charles 
Ветка «charles» отслеживает внешнюю ветку «charles» из «origin».
```
- ^^^ для всех других веток результат одинаковый, меняются только названия. 
- <img width="1020" alt="githw3 0" src="https://user-images.githubusercontent.com/84155505/145040119-6a8717da-a786-4503-8ccc-dfb91032531a.png">
3. В ветке Bug Reports сделать текстовый документ со структурой баг репорта
```
Command: git checkout bug_reports
Result: * bug_reports
  charles
  checklists
  jmeter
  main
  mobile_testing
  postman
  sql
 Command: touch bug_report.txt
 Command: vim bug_report.txt
```
4. Запушить структуру багрепорта на внешний репозиторий
```
Command: git add .
Command: git commit -m "adding bug_report to bug_reports branch"
Result: [bug_reports d14051c] adding bug_report.txt to bug_report branch
 1 file changed, 36 insertions(+)
 create mode 100644 bug_report.txt
Command: git push
Result: Enter passphrase for key '/Users/macintosh/.ssh/id_rsa': 
Перечисление объектов: 4, готово.
Подсчет объектов: 100% (4/4), готово.
При сжатии изменений используется до 8 потоков
Сжатие объектов: 100% (3/3), готово.
Запись объектов: 100% (3/3), 1.10 КиБ | 1.10 МиБ/с, готово.
Всего 3 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
To github.com:PaulBuzz/GITHW3.git
   23ceb13..d14051c  bug_reports -> bug_reports
```
- <img width="1019" alt="githw3 1" src="https://user-images.githubusercontent.com/84155505/145040809-d4bc0a7e-11d4-4115-8c22-444d68b1944b.png">
5. Вмержить ветку Bug Reports в Main
```
Command: git checkout main
Command: git merge bug_reports
Result: Обновление 23ceb13..d14051c
Fast-forward
 bug_report.txt | 36 ++++++++++++++++++++++++++++++++++++
 1 file changed, 36 insertions(+)
 create mode 100644 bug_report.txt
```
6. Запушить main на внешний репозиторий.
```
Command: git push
Result: Enter passphrase for key '/Users/macintosh/.ssh/id_rsa': 
Всего 0 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
To github.com:PaulBuzz/GITHW3.git
   23ceb13..d14051c  main -> main
```
- <img width="1010" alt="githw3 2" src="https://user-images.githubusercontent.com/84155505/145041537-146d829e-eb17-49cc-ba53-8a4d2b502c61.png">
7. В ветке CheckLists набросать структуру чек листа.
```
Command: git checkout checklists
Command: git touch checklist.txt
Command: vim checklist.txt
Command: git add .
Command: git commit -m "adding checklist.txt to checklists branch"
Result: [checklists df59f06] adding checklist.txt to checklists branch
 1 file changed, 17 insertions(+)
 create mode 100644 checklist.txt
```
8. Запушить структуру на внешний репозиторий
```
Command: git push
Result: Enter passphrase for key '/Users/macintosh/.ssh/id_rsa': 
Перечисление объектов: 4, готово.
Подсчет объектов: 100% (4/4), готово.
При сжатии изменений используется до 8 потоков
Сжатие объектов: 100% (3/3), готово.
Запись объектов: 100% (3/3), 708 байтов | 708.00 КиБ/с, готово.
Всего 3 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
To github.com:PaulBuzz/GITHW3.git
   23ceb13..df59f06  checklists -> checklists
```
9. На внешнем репозитории сделать Pull Request ветки CheckLists в main
- <img width="1015" alt="githw 3" src="https://user-images.githubusercontent.com/84155505/145042675-78712327-27e8-40eb-91e6-fdb0c274067e.png">
- <img width="1009" alt="githw 4" src="https://user-images.githubusercontent.com/84155505/145042707-c39ed8c2-a4e6-4176-a7d6-099011196fe1.png">
- <img width="998" alt="githw 5" src="https://user-images.githubusercontent.com/84155505/145042725-d9f34209-e624-472a-aaf6-dac971ba560d.png">
- <img width="958" alt="githw 6" src="https://user-images.githubusercontent.com/84155505/145042751-244de36f-4eff-493e-93f6-767e13246671.png">
- <img width="1011" alt="githw 7" src="https://user-images.githubusercontent.com/84155505/145042776-25c74575-5d45-414d-8dd4-f9fb0f02606e.png">
- <img width="1012" alt="githw 8" src="https://user-images.githubusercontent.com/84155505/145043075-1f90b5f8-f5f3-494e-8dc2-f56e8bc6aaac.png">
10. Синхронизировать Внешнюю и Локальную ветки Main
```
Command: git checkout main
Command: git pull
Result: Enter passphrase for key '/Users/macintosh/.ssh/id_rsa': 
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
Распаковка объектов: 100% (2/2), 773 байта | 386.00 КиБ/с, готово.
Из github.com:PaulBuzz/GITHW3
   d14051c..8da5f9a  main       -> origin/main
Обновление d14051c..8da5f9a
Fast-forward
 checklist.txt | 17 +++++++++++++++++
 1 file changed, 17 insertions(+)
 create mode 100644 checklist.txt
```
- <img width="937" alt="githw 9" src="https://user-images.githubusercontent.com/84155505/145043309-5e19ccea-348e-4ee1-9d20-f04ca71a0337.png">
