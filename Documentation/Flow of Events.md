1. Добавление продукта
	1. Краткое описание. Данный вариант использования описывает добавление продукта пользователем.
	2. Предусловия. Пользователь должен запустить приложение и кликнуть по кнопке «Продукты» в стартовом окне. Затем должен зайти в интересующий его раздел. Далее пользователь должен кликнуть по кнопке «Добавить продукт».
	3. Основной поток
		1. Вариант использования начинается, когда пользователь выбрал операцию «Добавление продукта» в любом разделе.
		2. Система выдает окно, в котором пользователь должен ввести:
			- раздел для хранения продукта
			- название продукта
			- год изготовления продукта
			- объем продукта
			- количество единиц продукта
			- название хранилища, в которое надо поместить продукт
		3. Если введены некорректные данные, то пункт 2. 
		4. Запрос к БД.
		5. Если выбранное пользователем хранилище отсутствует в БД, то пункт 2.
		6. Запись продукта в БД.
2. Удаление продукта
	1. Краткое описание. Данный вариант использования описывает удаление продукта пользователем.
	2. Предусловия. Пользователь должен запустить приложение и кликнуть по кнопке «Продукты» в стартовом окне. Затем должен зайти в интересующий его раздел. Далее пользователь должен кликнуть по кнопке «Удалить продукт».
	3. Основной поток
		1. Вариант использования начинается, когда пользователь выбрал операцию «Удаление продукта» в любом разделе.
		2. Система выдает окно, в котором пользователь должен ввести:
			- название продукта
			- год изготовления продукта
			- объем продукта
			- количество единиц продукта
			- v)	название хранилища, из которого надо удалить продукт
		3. Если введены некорректные данные, то пункт 2. 
		4. Запрос к БД.
		5. Если выбранный пользователем продукт отсутствует в БД, то пункт 2.
		6. Удаление продукта из БД.
3. Перемещение продукта
	1. Краткое описание. Данный вариант использования описывает перемещение продукта пользователем из одного хранилища в другое.
	2. Предусловия. Пользователь должен запустить приложение и кликнуть по кнопке «Продукты» в стартовом окне. Затем должен зайти в интересующий его раздел. Далее пользователь должен кликнуть по кнопке «Переместить продукт».
	3. Основной поток
		1. Вариант использования начинается, когда пользователь выбрал операцию «Перемещение продукта» в любом разделе.
		2. Система выдает окно, в котором пользователь должен ввести:
			- название продукта
			- год изготовления продукта
			- объем продукта
			- количество единиц продукта
			- название хранилища, из которого надо переместить продукт
			- название хранилища, в которое надо поместить продукт
		3. Если введены некорректные данные, то пункт 2. 
		4. Запрос к БД.
		5. Если выбранный пользователем продукт отсутствует в БД, то пункт 2.
		6. Изменение хранилища продукта в БД.
4. Поиск продукта
	1. Краткое описание. Данный вариант использования описывает добавление продукта пользователем.
	2. Предусловия. Пользователь должен запустить приложение и кликнуть по кнопке «Продукты» в стартовом окне. Затем должен зайти в интересующий его раздел. Далее пользователь должен кликнуть по значку поиска.
	3. Основной поток
		1. Вариант использования начинается, когда пользователь выбрал операцию «Поиск продукта» в любом разделе.
		2. Система выдает окно, в котором пользователь должен ввести:
			- название продукта
			- год изготовления продукта
			- объем продукта
		3. Запрос к БД.
		4. Если продукт присутствует, система выводит характеристики продукта. Иначе - сообщение об отсутствии продукта в БД.
5. Добавление раздела
	1. Краткое описание. Данный вариант использования описывает добавление раздела пользователем.
	2. Предусловия. Пользователь должен запустить приложение и кликнуть по кнопке «Продукты» в стартовом окне. Затем должен кликнуть по кнопке «Добавить раздел».
	3. Основной поток
		1. Вариант использования начинается, когда пользователь выбрал операцию «Добавление раздела».
		2. Система выдает окно, в котором пользователь должен ввести:
			- название нового раздела
		3. Запрос к БД.
		4. Если введенные пользователем раздел уже существует, то пункт 2.
		5. Добавление раздела в БД. 
6. Удаление раздела
	1. Краткое описание. Данный вариант использования описывает удаление раздела пользователем.
	2. Предусловия. Пользователь должен запустить приложение и кликнуть по кнопке «Продукты» в стартовом окне. Затем должен кликнуть по кнопке «Удалить раздел».
	3. Основной поток
		1. Вариант использования начинается, когда пользователь выбрал операцию «Удаление раздела».
		2. Система выдает окно, в котором пользователь должен ввести:
			- название удаляемого раздела
		3. Если введенный раздел отсутствует в БД, то пункт 2.
		3. Система предлагает удалить содержимое раздела или переместить его содержимое. Если выбирается перемещение содержимого, то выполняется альтернативный поток А1.
		4. Удаление раздела целиком из БД.
	4. Альтернативный поток А1
		1. Система должна запросить:
			- название раздела, в который нужно переместить содержимое удаляемого раздел
		2. Запрос к БД.
		3. Если введенные пользователем раздел для перемещения отсутствует, то пункт 1 потока А1.
		4. Перемещение содержимого раздела.
		5. Удаление раздела из БД.
7. Добавление хранилища
	1. Краткое описание. Данный вариант использования описывает добавление хранилища пользователем.
	2. Предусловия. Пользователь должен войти запустить приложение и кликнуть по кнопке «Иерархия хранилища» в стартовом окне. Затем должен кликнуть по кнопке «Добавить хранилище».
	3. Основной поток
		1. Вариант использования начинается, когда пользователь выбрал операцию «Добавление хранилища».
		2. Система выдает окно, в котором пользователь должен ввести:
			- название нового хранилища
		3. Если выбранное пользователем хранилище присутствует в БД, то пункт 2.
		4. Добавление хранилища в БД.
8. Удаление хранилища
	1. Краткое описание. Данный вариант использования описывает удаление хранилища пользователем.
	2. Предусловия. Пользователь должен войти запустить приложение и кликнуть по кнопке «Продукты» в стартовом окне. Затем должен кликнуть по кнопке «Удалить хранилище».
	3. Основной поток
		1. Вариант использования начинается, когда пользователь выбрал операцию «Удаление хранилища».
		2. Система выдает окно, в котором пользователь должен ввести:
			- название удаляемого хранилища
		3. Запрос к БД.
		4. Если хранилище отсутствует, то пункт 2. 
		5. Система предлагает удалить содержимое хранилища или переместить его содержимое. Если выбирается перемещение содержимого, то выполняется альтернативный поток А1.
		6. Удаление целиком хранилища из БД.
	4. Альтернативный поток А1
		1. Система должна запросить:
			- название хранилища, в который нужно переместить содержимое удаляемого хранилища.
		2. Запрос к БД.
		3. Если хранилище отсутствует, то пункт 1 потока А1. 
		4. Перемещение содержимого удаляемого хранилища.
		5. Удаление хранилища из БД.