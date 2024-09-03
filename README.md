# openserver
описание настроек

Запросы не корректно работали в стрикт режиме
В mysql my.ini 
[mysqld]
sql_mode				= ""

unit tests не запускались, т.к. сыпались ошибки deprecated Deprecated: Return type of Tightenco\Collect\Support\Collection::count() should either be compatible with Countable::count(): int, or the #[\ReturnTypeWillChange] attribute should be used to temporarily suppress the notice in
и сессия не стартовала Could not start session because headers have already been sent. "\vendor\tightenco\collect\src\Collect\Support\Collection.php":42.

В php.ini
display_errors                 = Off
display_startup_errors         = Off

Ну и в админке битрикса не подключаются файлы со стилями начинающиеся с .
Комментим блок 
#<LocationMatch "/\.(?!well-known)">
 #   Require            all denied
#</LocationMatch>

в файле httpd.conf в конфиге папке с конфигом php
