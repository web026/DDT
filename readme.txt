В первом тесте проверялась правильность геокодирования адрес -> координаты сервиса openstreetmap.org;
Был взят список адресов, по которым были получены координаты с помощью сервиса https://tech.yandex.ru/maps/geocoder/, 
эти координаты взяты за эталон и записаны с адресами в таблицу data_coord.xlsl.
Далее с помощью библиотеки Nominatim, которая использует геокодирование сервиса https://nominatim.openstreetmap.org по списку адресов был получен список новых координат, которые сравнивались с эталонными. 
Пройденным тестом считалось совпадение координат 98% и выше.

Во втором тесте проверялась правильность геокодирования координаты -> адрес сервиса openstreetmap.org;
Был взят список координат, по которым получены адреса, 
также использовался сервис https://tech.yandex.ru/maps/geocoder/, 
адреса были приняты за правильные и записаны в таблицу data_address.xlsl вместе с координатами.
Далее было выполнено пробразование координат в адрес через библиотеку Nominatim и сравнение их с правильными адресами.
Тест считается пройденным, если совпадение в строк адресов 80% и более.
