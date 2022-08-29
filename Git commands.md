# **Git commands**

## Initialization
Инициализирует *новый репозиторий* (папка в которой лежат файлы для отслеживания):

    git init

## Status 
Показывает *текущий статус* (что удалено, изменено и т.д.):

    git status

## Add
После сохранения изменений добавляет *новую версию* для отслеживания. **После добавления нужно делать commit с описанием изменений**:

    git add file_name

## Commit
Открывает *отдельное окно*, где можно написать commit:

    git commit

Но лучше делать этот вариант. Здесь *создается commit*, после которого в скобках написать *описание изменений*:

    git commit -m "What was changed"

Можно добавить файл и создать commit *в одной строке* (пока лучше не делать)...:
   
    git commit -a

... и добавить комментарий:
    
    git commit -am "What was changed"

## Difference
Показывает разницу между *текущим файлом* и *последним по времени* коммитом.

    git diff 

Показывает разницу между *любыми выбранными* коммитами 12345a и 12345b. **Порядок важен!** - поазывает, что изменилось в первом с сравнении со вторым.

    git diff 12345a 12345b

## Log
Выводит коммиты по порядку - вверху текущий и далее по времени добавления. Выводит по 4 строки на каждый коммит:

    git log

Выводит коммиты, но каждый коммит в одну строку:

    git log --oneline

Если находимся в коммите *не master*, то git log покажет коммиты от текущего к ранним. **Все что после и вплоть до master показано не будет!**. Чтобы показать вообще *все коммиты* берем команду:

    git log --all

Предыдущая команда, только вывод *в одну строку* на коммит:

    git log --oneline --all

## Checkout
Переход *к сохраненным коммитам* по 4-7 первым символам в названии коммита:

    git checkout 1234567

К *master-коммиту* следует переходить **не по его названию!**, а следующей командой:

    git checkout master

##Q

*Для выхода из разных режимов*, когда не показывается строка для ввода команд, жмем:

    q

## Pictures

To add pictures write this command:

    ![some_comment](file_name.ext)

For example:

    ![Hi, I'm Ducky](Duck.png)

Result:

![Hi, I'm Ducky](Duck.png)

## Branching in git

Branch description:

Branches in GIT is a "sandbox" for working with a part of file. It doesn't change the main file if switch to it from master branch.

Commands:

Show all branches and active branch:

    git branch

Create branch:

    git branch <branch_name>

Switch to branch:

    git checkout <branch_name>

After working in any branch you can merge it to the master. Switch to master baranch first and write this command:

    git merge <branch_name>

After that you can delete this branch:

    git branch -d <branch_name>



## The end
