git-hooks
=========

  Copyright 2014  Konstantin Slupko (email: linux0uid@gmail.com)


Hooks for development on git

Этот репозиторий предназначен для работы с базами данных, прежде всего MySQL.
Основная задача данных хуков - обеспечение автоматизации Web-разработки.


INSTALL

1. Для использование "хуков" в своем проекте - скопируйте все содержимое данного репозитория (или конкретные файлы) в каталог /{dir of your project}/.git/hooks/
2. Внесите необходимые изменения в используемые файлы:
    a) если используете drush установите переменную use_drush="yes" (вводить параметры базы данных нет необходимости);
    б) во всех других случаях введите:
	    - имя базы данных;
	    - пользователя базы данных;
	    - пароль для пользователя базы данных.
3. Сделайте очередной/первый коммит.


VERSION

v0.2.4	- Добавлена поддержка drush для Drupal.
        - Увеличена скорость работы скриптов и файл shema.sql больше не нужен.

v0.2.1	- Добавлена обработка ошибок.

v0.2.0	- Добавлено создание файла shema.sql (структура базы данных).
	- Из файла db.sql были исключены команды выбора базы данных, ее полной очистки; они были перенесены в файл shema.sql. Таким образом импортировать файл db.sql можно на хостинг с ограниченными правами уже без ручного редактирования.
	СОВМЕСТИМОСТЬ: файлы v0.2.x НЕ совместимы с v0.1.x, используйте только в новых проектах.

v0.1.1	- При выполнении git commit создается файл db.sql с дампом базы данных.
