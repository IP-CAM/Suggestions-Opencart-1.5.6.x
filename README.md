Подсказки DaData.ru для OpenCart
====================

Описание
---------------

Данный модуль включает автодополнение ФИО и адресов в интернет-магазинах на базе OpenCart. Он использует сервис [подсказок](https://dadata.ru/suggestions) DaData.ru.

Модуль совместим с версиями OpenCart 1.5.6.x.

Установка
---------

### 1. Установите модуль

Прежде всего, скачайте [дистрибутив](https://github.com/hflabs/suggestions-opencart/releases), распакуйте его, и скопируйте файлы из каталога `upload` в корень opencart-магазина.

Для замены регионов России на корректные значения из КЛАДР выполните SQL-скрипт `zone.sql` над БД магазина через phpMyAdmin либо из консоли:

```
$ mysql opencart -u opencart -p < zone.sql
```

### 2. Включите подсказки в настройках

Модуль настраивается в админке по адресу: *Дополнения > Модули > DaData*.

![Настройки модуля](doc/dadata-opencart-admin.png)

*API-ключ* — необходимо получить в [личном кабинете](https://dadata.ru/profile/#info) DaData.ru.

*Количество возвращаемых подсказок* — количество подсказок, которое демонстрируется пользователю.

Оставшиеся поля настройки (автоматическое исправление по мере ввода, показывать дополнительные поля адреса, показывать пол) управляют поведением подсказок. Вы можете включить их по необходимости.

*Статус* – показывает статус работы модуля: «включено» – подсказки работают, «отключено» – подсказки не работают.

*Версия подсказок* — какой сервис использовать при работе (подробнее см. [Версии подсказок] (https://dadata.ru/suggestions/#pricing)). 

После заполнения всех полей необходимо сохранить настройки.

### 3. Пользуйтесь подсказками!

Подсказки работают при вводе ФИО и адреса во время регистрации и оформления заказа:

![Подсказки по ФИО](doc/dadata-opencart-demo-1.png)
![Подсказки по адресу 1](doc/dadata-opencart-demo-2.png)
![Подсказки по адресу 2](doc/dadata-opencart-demo-3.png)


История изменений
-----------------

* 1.1 
 * Добавлена возможность использовать платную версию сервиса
 * Переписан код модуля - больше не нужно править исходники магазина.
 
** ВНИМАНИЕ: перед тем как устанавливать новый модуль необходимо откатить изменения из этого документа (т.е. сделать процедуру обратную установке версии 1.0) инструкция [тут](https://github.com/hflabs/suggestions-opencart/blob/11635aa10a304efdf8e5cfface4af2f444823784/doc/install.md) **

* 1.0
 * Первый релиз