fusion project
======

Небольшой интро в гит.

Итак, установить гит и родной клиет (если нет желания все делать из командной строки) можно вот отсюда https://help.github.com/articles/set-up-git

Как там работать с клиентом, я не знаю (но должно быть не сложно), начните с документации http://git-scm.com/documentation

    		   	       	       	   Азы (из командной строки)


1. Создать клон репозитария:
> cd to/the/folder/you/want/clone/your/project/in
>
> git clone git@github.com:zoberg/fusion.git

2. Базовая информация об участнике (чтобы понятно было кто что закомитил):
> git config --global user.name "Roman Zakharov"
>
> git config --global user.email "zoberg@gmail.com"

   посмотреть свой конфиг:
> git config --global --list

3. Модификация файлов:
Например, открыли файл README.md, что-то там написали, сохранили. Потом:
> git status

   получили следующее:
> On branch master
>
> Changes not staged for commit:
>
>   (use "git add <file>..." to update what will be committed)
>
>   (use "git checkout -- <file>..." to discard changes in working directory)
>
>	modified:   README.md
>
> no changes added to commit (use "git add" and/or "git commit -a")

   То есть, мы в главной ветке, из измененных файлов только README.md
   Теперь отправим изменения. Чтобы добавить все файлы в индекс:
> git add .

   Чтобы просмотреть, что мы собираемся отправить:
> git diff --cached

   Чтобы просмотреть, что было изменено, но не добавлено в индекс:
> git diff

   Отправляем изменения
> git commit

   Тут можно добавить сообщение в следующем формате: краткое описание изменений в одну строку, потому пустая строка, потом более длинное изменение описания.
   Теперь изменения отправлены, но доступны только локально, а чтобы опубликовать их в репозитории делаем так:
> git push

4. Обновление файлов:

   Чтобы скачать изменения, сделанные другими участниками:
> git fetch

   Чтобы скачать изменения, сделанные другими участниками И объдинить их со своей локальной версией проекта:
> git pull

   Остальное можно посмотреть в git-cheat-sheet и прочитать в документации.