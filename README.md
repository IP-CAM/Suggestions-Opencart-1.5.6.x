Подсказки DaData.ru для OpenCart
====================

Описание
---------------

Данный модуль включает автодополнение ФИО и адресов в интернет-магазинах на базе OpenCart. Он использует сервис [подсказок](https://dadata.ru/suggestions) DaData.ru.

Модуль совместим с версиями OpenCart 1.5.6.x.

Установка
---------

### 1. Установите модуль

Прежде всего, скачайте дистрибутив, распакуйте его, и скопируйте файлы из каталога `upload` в корень opencart-магазина. Затем следуйте [инструкции по модификации исходных кодов](doc/install.md) магазина.

### 2. Включите подсказки в настройках

Модуль настраивается в админке по адресу: *Дополнения > Модули > DaData*.

![Настройки модуля](doc/dadata-opencart-admin.png)

*API-ключ* — необходимо получить в [личном кабинете](https://dadata.ru/profile/#info) DaData.ru.

*Количество возвращаемых подсказок* — количество подсказок, которое демонстрируется пользователю.

Оставшиеся поля настройки (автоматическое исправление по мере ввода, показывать дополнительные поля адреса, показывать пол) управляют поведением подсказок. Вы можете включить их по необходимости.

*Статус* – показывает статус работы модуля: «включено» – подсказки работают, «отключено» – подсказки не работают.

После заполнения всех полей необходимо сохранить настройки.

### 3. Пользуйтесь подсказками!

Подсказки работают при вводе ФИО и адреса во время регистрации и оформления заказа:

![Подсказки по ФИО](doc/dadata-opencart-demo-1.png)
![Подсказки по адресу 1](doc/dadata-opencart-demo-2.png)
![Подсказки по адресу 2](doc/dadata-opencart-demo-3.png)
