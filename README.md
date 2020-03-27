# Возможности

1. Скрипт умеет генерировать мусор из сиволов a-z в обоих регистрах.
1. Умеет загонять в LocalStorage до 50 000 строк по 100 символов (больше не позволяют ограничения браузера)
1. Умеет работать с данными в сессии, даже если они не были загнаны в LocalStorage(удаляется при сбросе сессии)
1. Ищет путем формирования нового массива путем фильтрации загруженного в память.

# Не умеет

1. Загонять в LocalStorage более 50 000 строк по 100 символов, так как выходит за квоту.

# Пути улучшения

1. Использовать бинарный поиск, вместо тупого перебора (массив заранее при создании сортируется, так что путь развития заложен)
1. При вводе первого символа до сабмита формы искать диапазон в сортированном массиве, чтобы его взять и уже в нем проводить поиск. Массив опять же, сортирован заранее.
1. Использовать другие типы хранилища, например WebSQL (не смотрел квоту).
1. Использовать сжатие строк, но конкретно для данного примера это просто усложнит задачу на уровне генерации мусора.

# Чего нет возможности проверить

1. Можно ли завернуть в мусор более 5 миллионов строк, так как браузер начинает пищать «а может хватит» и вываливается из оперативной памяти.