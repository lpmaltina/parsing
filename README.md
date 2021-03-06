# parsing

[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

В файле **parse_data.py** находится код для парсинга текстов, собранных с сайтов https://www.newsinlevels.com и https://www.daysinlevels.com.

Содержимое сайтов - тексты на английском языке, разбитые по уровням сложности.

Основные библиотеки, использованные для парсинга:
- requests
- beautifulsoup4

В качестве вспомогательного инструмента для работы со строками применяются регулярные выражения.

Тексты, собранные в результате парсинга, сохраняются в базу данных. Использованная СУБД - SQLite.

Имя базы данных - textinlevels.

В базе данных есть две таблицы: newsinlevels и daysinlevels, каждая из которых содержит тексты, собранные с соответствующего ресурса.

Обе таблицы имеют следующие столбцы:
- date - дата
- heading - заголовок текста
- article_text - текст на английском языке
- level - уровень сложности текста (возможные значения: 1, 2, 3)

Полученная база данных доступна по ссылке: https://drive.google.com/file/d/1qo2a3rWYOdaKWwOpLurzu-8g9eiX5lb_/view?usp=sharing.

Файл **view_data.ipynb** позволяет посмотреть:
- количественные данные о текстах (сколько текстов каких уровней с какого ресурса было собрано)
- фрагменты созданных датасетов
