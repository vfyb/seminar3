# **Git commands**

## Initialization
Initilize *new repository* (folder with files which will be tracked by GIT):

    git init

## Status 
Show *current status* (deleted, changed etc.):

    git status

## Add
After save add *new version* for tracking. **After "add" command next will be "commit" with description of changes**:

    git add file_name

## Commit
Open *separate window*, where you can write commit:

    git commit

Better use this command. Here *you create commit* and write *description*:

    git commit -m "What was changed"

You can add new version and create commit *in one line* (__don't use it for now!__)...:
   
    git commit -a

... and add the description:
    
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

*For quit from different regimes*, when can't enter the command, press:

    q

## Pictures

To *add pictures* write this command:

    ![some_comment](file_name.ext)

For example:

    ![Hi, I'm Ducky](Duck.png)

Be sure that you write <file_name> exactly the same like it named (considering the *case* for example).

Result will be look like this:

![Hi, I'm Ducky](Duck.png)

## Branching in git

### Branch description:

Branches in GIT is a __"sandbox"__ for working with a *part of file* or/and create *alternative version* of this part. It doesn't change the main file if switch to it from master (or other) branch, it just create alternative version.

### Commands:

Show *all branches* and *active branch*:

    git branch 

*Create* branch:

    git branch <branch_name>

*Switch* to branch:

    git checkout <branch_name>

After working in any branch you can **merge** it to the master or another branch. Switch to **target branch** first and write this command:

    git merge <branch_name>

You can see some **conflicts** at that moment, such as *difference* of text versions of two branches in the same part of text. So you can **add all versions or/and change and combine them into one correct**.

After that you can __delete__ this branch:

    git branch -d <branch_name>

**Be sure** that you **delete all branches** which you merge to another and **don't need them further**. 

## The end
