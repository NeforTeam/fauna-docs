# API help link https://ru.wikipedia.org/w/api.php

# Request syntax
Аргументы http запроса начинаются со знака "?", который разделяет путь к обработчику, и тело запроса. К примеру в запросе https://ru.wikipedia.org/w/api.php?action=help&format=json адрес https://ru.wikipedia.org/w/api.php является путем к обработчкику, а ?action=help&format=json аргументами запроса. Аргументы запроса указываются последовательно, каждый аргумент отделяется знаком "&" без пробелов.

В запросах к обработчику есть основной(но не обязательный) аргумент:
- action: Действие, которое следует выполнить.

А так же дополнительные, один из которых:
- format: Формат вывода, т.е. в каком виде вы хотите получить ответ на запрос.
Все аргументы вы можете узнать на странице странице встроенной справки (https://ru.wikipedia.org/w/api.php)

# Прямая отправка запросов


При переходе по прямой ссылке обработчика без указания аргументов, обработчик выдаст Справку MediaWiki API. Попробовать функции обработчика в интерактивной песочнице(https://ru.wikipedia.org/wiki/%D0%A1%D0%BB%D1%83%D0%B6%D0%B5%D0%B1%D0%BD%D0%B0%D1%8F:ApiSandbox). Для более полного понимания работы обработчика, рекомендуется делать запросы через адресную строку браузера.

# Request Auth


Большая часть запросов требует авторизации при помощи токенов, в том числе и анонимное редактирование. Для получения csrf токена, выполните запрос:

https://ru.wikipedia.org/w/api.php?action=query&format=jsonfm&meta=tokens

# Using

Примеры запросов
Не требующие авторизации:

https://ru.wikipedia.org/w/api.php?action=help&format=json
Получить справку MediaWiki API в формате json.

Требующие авторизацию:
Большая часть запросов требует авторизации при помощи токенов, в том числе и анонимное редактирование. Для получения csrf токена, выполните запрос:

https://ru.wikipedia.org/w/api.php?action=query&format=jsonfm&meta=tokens

# Sandbox

https://ru.wikipedia.org/wiki/%D0%A1%D0%BB%D1%83%D0%B6%D0%B5%D0%B1%D0%BD%D0%B0%D1%8F:ApiSandbox

# Help notes and links

https://www.mediawiki.org/wiki/API:Get_the_contents_of_a_page/ru