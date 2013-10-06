BlankProject
============

Каркас для создания проекта.

Предусматривает модульную систему подключения стилей и js.
Использует LESS.
Включен jQuery 1.10.* и кастомная сборка Modernizr 2.6.2.

Для сборки проекта я использую CodeKit, все необходимые настройки приложены в файле конфигурации проекта codekit-config.json
В случае, если использование CodeKit невозможно, проект может быть собран с использованием Grunt.

Я предпочитаю разворачивать проект из корня сервера; в случае, если вы предпочитаете относительные пути, проверьте адресацию в head

Структура:

	| (Содержит html-шаблоны)
	|
	|---img (Предполагает размещение изображений проекта)
	|	|
	|	|---background (Фоновые изображения)
	|	|---controls (Элементы стилизации кнтролов)
	|	|---content (Рыбные изображения для шаблонов)
	|
	|---js (Содержит склеенный [/минифицированный] js)
	|	|
	|	|---main.js
	|
	|---css (Содержит склеенный [/минифицированный] css)
	|	|
	|	|---style.css
	|
	|---source (Содержит исходные файлы css и js)
		|
		|---js
		|	|
		|	|---app.js (Описание функцинала)
		|	|---dom.js (Привязка функционала к событиям)
		|	|
		|	|---lib
		|		|
		|		|---jquery
		|		|---modernizr
		|		|---...
		|
		|---less
			|
			|---reset.less (Кастомный сброс)
			|---style.less (Файл для импорта less-блоков)
			|
			|---blocks (Независимые модули)
				|
				|---wrapper.less
				|---container.less
				|---footer.less
				|---...

По-умолчанию результирующий css\js только склеивается, не сжимается: этот процесс может оказаться весьма ресурсоемким.
При выкладке на продакшн следует выставить соответствующие настройки в CodeKit/Grunt
