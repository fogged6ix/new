1. ls - это команда лист, она показывает что находится в директории. 
   - Аргументы
	 "`-`" - нужно ставить перед аргументом, который включает в себя только одну букву(например "l")
	 "`--`" - когда аргумент содержит больше 1 буквы
     - "`--color=yes, no, auto`" - включает или выключает обозначение цветом
     - ***Отображение всех фалов***
        - "`-l`" -  выводит всё находящееся листом(в столбик с подробной информацией)
	    - "`-a`" - выводит абсолютно все файлы (dotfiles)(полное название `all`). "`.`" - обозначает текущую папку пользователя, "`..`" - обозначает родительский каталог (минус каталог назад). "`-A`" - все файлы только без dotfiles. "`-al`" - все файлы листом
	- ***Сортировка файлов***
	     - В linux имеет разные отметки времени(timestamp), их 3 штуки
	     `atime` - время, когда в последний раз обращались к файлу 
	     `mtime` - последний раз когда меняли содержимое файла
	     `ctime` - последнее изменение метаданных (права доступа, расположение файла и т. д)
	     - Что же такое timestamp (отметка времени) - это числовое представление времени. Вызывается командой `date`. `ls -lt` - как раз и показывает список файлов с временем создания
           
           `$ date`
           `Mon 01 Nov 2021 08:14:52 PM UTC`
         `ls -ltu` - показывает когда менялось содержимое файлов
         `ls -ltc` - показывает изменения метаданных файлов
    - ***Сортировка по размеру***
         - `ls -s`  - показывает списком файлы и их размер 
         - `ls -ls` -  показывает файлы и их размер, но уже столбцом
         - `ls -lS` - показывает файлы и их размер, но уже сортирует их и идет от большего к меньшему
         - `ls -lh` (`--human-readable` or `-h`) - показывает размер файлов не в байтах, а в более читаемую форму - kb, Mb, Gb
         - `ls -lSh` - показывает размер файлов в человеческом виде
    - ***Форматирование***
         - `ls -1` - отображает все файлы в столбик (без данных и пр.) (тоже самое, что и просто `ls`, но в столбик)
         - `--format` - используется для написания скрипта и в ls для ввода данных для других частей скрипта
         Если написать `ls --format=commas`, то отобразятся файлы через commas(запятую)
         Короткий вариант написания `ls -m`
         Если хотим отобразить полную информацию как в команде `ls -l`, то можно использовать вариант с полным написанием `ls --format=long`
         - `ls -lQ` - отображает файлы в кавычках `""`
         - `--time-style` - отображение времени в разных форматах (`ls -l --time-style=locale`, `ls -l --time-style=iso`, `ls -l --time-style=full-iso`)
	- ***Другие аргументы и помощь***
	     - `ls -al --author` - показывает имя пользователя который создал файл 
	     - `ls -ald` - показывает текущую директорию, в некоторых обстоятельствах мб полезно
	     - `ls -ali` - показывает индексы
	     - `ls -alR` - выводит всю информацию по каталогам внутри и находящимся файлам внутри этих каталогов
	     - `ls -alr` - выводит list в обратном порядке
	     - `ls -alSr` - выводит list по размеру файлов и директорий в обратном порядке
	    