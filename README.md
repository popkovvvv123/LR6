# Лабораторная работа №6

Цель лабораторной работы: изучение базовых возможностей системы управления версиями, опыт работы с Git API, опыт работы с локальным и удаленным репозиторием.

Выполнение работы

* Сделать fork репозитория на GitHub
![делать fork репозитория на GitHub](screenshots/sc-01.png)
![делать fork репозитория на GitHub](screenshots/sc-02.png)

* Клонировать свой личный удалённый репозиторий на компьютер.
![Клонировать свой личный удалённый репозиторий на компьютер](screenshots/sc-03.png)
```bash
git clone https://github.com/popkovvvv123/LR6
```

 * Добавить файл через интерфейс GitHub.
![Добавить файл через интерфейс GitHub. Подтянуть изменения в локальный репозиторий](screenshots/sc-04.png)

Подтянуть изменения в локальный репозиторий.
![Добавить файл через интерфейс GitHub. Подтянуть изменения в локальный репозиторий](screenshots/sc-05.png)
```bash
git pull
```

*  Получить историю операций для каждой из веток.
![code](screenshots/sc-06.png)
```bash
git log --graph
```

* Просмотреть последние изменения. 
![Получить историю операций для каждой из веток](screenshots/sc-07.png)
```bash
git log
```

* Выполнить слияние в ветку master, разрешив конфликт.
![Выполнить слияние в ветку master, разрешив конфликт](screenshots/sc-08.png)
```bash
git branch test-branch
git checkout test-branch
git status
git add mergefile.txt
git commit -m "file changing from test-branch"
git branch
git checkout master
git merge test-branch
```

* Удалить побочную ветку после успешного слияния.
![Удалить побочную ветку после успешного слияния](screenshots/sc-09.png)
```bash
git branch -d test-branch
```

* Сделать изменения и зафиксировать их, оставляя комментарии ,несколько раз. 
![Сделать изменения и зафиксировать их, оставляя комментарии ,несколько раз](screenshots/sc-10.png)
```bash
git add . 
git commit -m "file changing #1 from master branch"
git add . 
git commit -m "file changing #2 from master branch"
```

* Сделать откат коммита. 
![Сделать откат коммита](screenshots/sc-11.png)
```bash
git reset --soft HEAD~1
git log
```

* Создать ветку для отчёта.
![Создать ветку для отчета](screenshots/sc-12.png)
```bash
git branch report
git checkout report
```

* Начать оформлять отчёт.

* Получить историю операций в форматированном виде.
![Получить историю операций в форматированном виде](screenshots/sc-13.png)
```bash
git log --pretty=format:"%h %ad %an %s"
```

* Отправить локальные изменения в сетевое хранилище GitHub
![Отправить локальные изменения в сетевое хранилище GitHub](screenshots/sc-14.png)
```bash
git push 
```
