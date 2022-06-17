# Работа с удалленым репозиторием.
1. Для начала нужно зарегистрироваться на сайте github.com , это может быть любое  имя.
2. После регистрации нажимаем кнопочку "+" и вводим название репозитория. Выбираем тип Public (репозиторий всегда Public для бесплатной версии) и нажимаем Create.
3. Добавляем удаленный репозиторий (по протоколу SSH) под именем origin (вместо origin можно использовать любое другое имя).
~~~
git remote add origin git@github.com:myuser/project.git

~~~
Можем просмотреть результат добавления с помощью команды:
~~~
git remote -v
~~~
Если все было правильно сделано, то увидим:
~~~
origin git@github.com:myuser/project.git (fetch)
origin git@github.com:myuser/project.git (push)
~~~
4. Следующей командой вы занесете все изменения, которые были сделаны в локальном репозитории на Github.
~~~
git push -u github master
~~~
Все дальнейшие изменения вы можете переносить на удаленный репозиторий упрощенной командой.
~~~
git push
~~~