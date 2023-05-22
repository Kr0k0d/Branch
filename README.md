# Homework 2
### 1. На локальном репозитории сделать ветки для:
- Postman
- Jmeter
- CheckLists
- Bag Reports
- SQL
- Charles
- Mobile testing

Для создания веток нужно использовать команду 
```
git branch postman
```
В примере я указал ветку Postman, также нужно сделать с другими ветками 

---

### 2. Запушить все ветки на внешний репозиторий
Чтобы сделать это, я использовал команду
```
git push origin --all
```
Но это команда работает не так как я думал, и в дальнейшем из-за нее могут быть ошибки. Поэтому я использовал проверенный метод, и запушил каждую ветку по отдельности 
```
$ git push -u origin Postman
```
_Вывод_
```
 * [new branch]      Postman -> Postman
branch 'Postman' set up to track 'origin/Postman'.
```

---

### 3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта
Для этого, нам нужно перейти на ветку bag_reports
```
git checkout Bag_Reports
```
Дальше нужно создать файл и вписать в него информацию
```
$ vim Bugs.txt
```
```
	Котороткое описани: Короткое описание проекта
	Проект: Название тестируемого проекта
	Компонент прилодения: Название части  или функции тестируемого продукта
	Номер версии: Версия на которой была найдена ошибка
	Серьезность: S1(Blocker), S2(Critical), S3(Major), S4 (Minor), S5(Trivial)
	Приоритет: P1(Hight), P2(Medium), P3(low)
	Статус: Стутус бага 
	Автор: Создатель баг репорта
	Назначен на: Имя сотрудника, назначеного на решение проблемы
```
---

### 4. Запушить структуру багрепорта на внешний репозиторий
```
git add .

git commit -m "Bugs"
```
_Вывод_
```
[Bag_Reports 27f2c97] Bugs
 1 file changed, 9 insertions(+)
 create mode 100644 Bugs.txt
```

---

### 5. Вмержить ветку Bag Reports в Main
Для этого нужно сперва зайти в ветку Main
```
git checkout main
```
Теперь можно вмержить любую ветку в ветку main
```
git merge bag_reports
```
_Вывод_
```
Updating c71f814..27f2c97
Fast-forward
 Bugs.txt | 9 +++++++++
 1 file changed, 9 insertions(+)
 create mode 100644 Bugs.txt
```

---

### 6. Запушить main на внешний репозиторий.
```
git status
```
_Вывод_
```
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```
```
git push
```
_Вывод_
```
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 658 bytes | 329.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Kr0k0d/Branch.git
   c71f814..27f2c97  main -> main
```

---

### 7. В ветке CheckLists набросать структуру чек листа.
Делаем все тоже самое, что и в пункте *3*
```
git checkour checklists

vim Check.txt
```
```
1. Введение 
	- Краткое описание продукта
	- Цель тестирования
	- Оласть применения тестирования 
2. Функциональное тестировние 
	- Проверка функций продукта
	- Список тест-кейсов для каждой функции
3. Тестирование производительности
	- Список тест-кейсов для оценки производительносьти продукта
4. Тестирование безопасности
	- Список тест-кейсов для оценки уровня безопасности продукта
5. Тестирование совместимости
	- Список тест-кейсов для оценки совместимости продукта с различными операционными системами, браузерами и т.д
6. Тестирование удобства использования
	- Список тест-кейсов дял оценки удобства использования продукта
7. Тестирование локализации и мультиязычности
	- Список тест-кейсов для оценки корректности работы продукта на различных языках
8. Результат тестирования
	- Общее описание результатов тестирования
	- Список обнаруженных ошибок и недостатков
9. Заключение
	- Оценка качества продукта
	- Рекомендации по улучшению продукта
```

---

### 8. Запушить структуру на внешний репозиторий
Делаем все тоже самое, что и в пункте *4*
```
git add .

git commit -m "CheckList"
```
_Вывод_
```
[CheckLists e4efccf] CheckList
 1 file changed, 23 insertions(+)
 create mode 100644 Check.txt
```
```
git push
```
_Вывод_
```
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (a), 785 bytes | 392.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Kr0k0d/Branch.git
   c71f814..e4efccf  CheckLists -> CheckLists
```
---

### 9. На внешнем репозитории сделать Pull Request ветки CheckLists в mainnl.

Для этого нужно зайти в свой репозиторий, перейти на ветку _*CheckLists*_, нажать _*Compair & pull request*_, после написать комит, нажать _Create pull request_ и после нажать на кнопки _Merge pull request_ и _Confirm merge_.

### 10. Синхронизировать Внешнюю и Локальную ветки Main.
```
git checkout main
```
_Вывод_
```
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```
```
git pull
```
_Вывод_
```
Updating 27f2c97..f306595
Fast-forward
 Check.txt | 23 +++++++++++++++++++++++
 1 file changed, 23 insertions(+)
 create mode 100644 Check.txt
```
