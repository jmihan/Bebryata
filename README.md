В репозитории три разных программы. 
1. Первая программа написана на языке C++. Основной код в Bebryata/tryAPI/MyForm.h и немного в Bebryata/tryAPI/MyForm.cpp. Делает API запрос, делает правильно, но у меня    почему-то апишки не работают(((
   Возможно проблема во мне, но я вроде делал все по инструкции к API. Пробовал пользоваться: API яндекс карт, 2ГИС API, MapBox API. Работало лишь MapBox, но видимо из-    за своей специфики работы, достоверную информацию эти карты могут выдать только Америки и еще какого-то узкого круга местоположений. Российские геолокации не            работали(и почему-то Франция тоже). Как я говорил выше, яндекс API и 2ГИС API не работают у меня, и та и друга пишет что не верный ключ(но ключ я скопировал и он не      может быть неверным).
2. Вторая программа(основной код расположен в Bebryata/mobile/src/main/java/com/example/myapplication. Также есть .apk файл по пути:                                        Bebryata\mobile\outputs\apk\release): в ней я пытался написать приложение для андроид. Вроде получилось, вроде даже что-то работает. Оно определяет геолокацию,          возвращает широту и долготу. Но только вот в чем загвоздка: в эмуляторе все прекрасно работает и выдает правильные географические координаты. Но если я                  пробую на своем телефоне у меня ничего не работает, хотя вроде разрешение на предоставление геоданных я разрешил. Сработало лишь один раз, зато как, с точностью около    километра. Скорее всего из-за плохого сигнала в общаге(все таки лес вокруг).  
3. Третья программа - самая рабочая из всех. Находится в корне Bebryata, основной код в MyForm.cpp. Работающий .exe файл можно найти в Bebryata/x64/Release. Также здесь    написана маленькая некая база данных(далее БД) с информацией о магазинах с дисконтными картами в академгородке (файл shop_1.sql, но что-то с sql затянулось и я          переписал БД в shops1.txt файл :) ). Как я говорил ранее, программа самая рабочая из трех предыдущих, она по входным координатам(к сожалению широта и долгота вводятся    в ручную) выдает магазины в порядке возрастания расстояния до них. Все работает корректно, расстояние посчитано с учетом кривизны земли.


Вот такие три программки получились, по идее надо бы их в одну соединить и добавить функционал добавления/удаления/хранения дисконтных карт и получилось бы как раз таки то, что требуются в кейсе хакатона. Но большинство вещей, которые я использовал в разработке данных трех программ, я делал впервые и мне просто напросто не хватило времени на то, чтобы сделать все как надо.


P.S. Дизайном на фигме занимался Владимир, базой данных магазинов - Александр, Михаил писал полностью весь код, а Семён занимался аналитикой.  


UPD: К сожалению в коде полетела кодировка(  Но там вроде не особо критично, комментарии и некоторый вывод в уведомления.
