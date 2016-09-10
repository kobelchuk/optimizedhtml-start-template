<h1>OptimizedHTML 1.0 - лучшие практики скоростной оптимизированной верстки сайтов</h1>

<p>
	<img src="http://agragregra.github.io/github-images/optimized-html-github-poster.jpg" alt="Start HTML Template">
</p>

<p>Автор: <a href="http://webdesign-master.ru" target="_blank">WebDesign Master</a> | <a href="http://webdesign-master.ru/blog/tools/2016-08-19-optimizedhtml.html" target="_blank">Manual in Russian</a></p>

<h2>Как использовать OptimizedHTML:</h2>

<ol>
	<li><a href="https://github.com/agragregra/optimizedhtml-start-template/archive/master.zip">Скачайте</a> <strong>optimizedhtml-start-template</strong> с GitHub;</li>
	<li>Установите модули Node.js командой: <strong>npm i</strong>;</li>
	<li>Запустите шаблон командой: <strong>gulp</strong>. Готово, можно работать.</li>
</ol>

<h2>Таски Gulp:</h2>

<ul>
	<li><strong>gulp</strong>: запуск дефолтного gulp таска (sass, js, watch, browserSync) для разработки;</li>
	<li><strong>build</strong>: сборка проекта в папку <strong>dist</strong> (очистка, сжатие картинок, удаление всего лишнего);</li>
	<li><strong>deploy</strong>: выгрузка проекта на рабочий сервер из папки <strong>dist</strong> по FTP;</li>
	<li><strong>clearcache</strong>: очистка кеша gulp. Полезно для очистки кеш картинок и закешированных путей.</li>
</ul>

<h2>Правила работы со стартовым HTMl шаблоном:</h2>

<ol>
	<li>Все HTML файлы должны иметь одинаковое стартовое наполнение, как у файла <strong>app/index.html</strong>;</li>
	<li>Найдите комментарий <strong>Template Basic Images Start</strong> в файле app/index.html. Все ваши кастомные бозовые картинки, такие, как og:image для социальных сетей и фавиконки для различных устройств следует задать в этом месте шаблона;</li>
	<li>Найдите комментарий <strong>Load Fonts CSS Start</strong> в файле app/index.html. Используйте функцию <strong>loadCSS</strong>, если сайт находится в подпапке. Используйте (раскомментируйте) функцию <strong>loadLocalStorageCSS</strong>, если сайт находится в корне домена (предпочтительный способ загрузки шрифтов). Все шрифты подключаются в файле <strong>app/sass/fonts.sass</strong> с использованием Bourbon;</li>
	<li>Найдите комментарий <strong>Custom Browsers Color Start</strong> в файле app/index.html. Здесь можно задать цвет шапки браузера на различных устройствах;</li>
	<li>Найдите комментарий <strong>Custom HTML</strong> в файле app/index.html. Здесь следует писать ваш HTML;</li>
	<li>Найдите комментарий <strong>Optimized loading JS Start</strong> в файле app/index.html. Здесь происходит оптимизированная загрузка всех скриптов;</li>
	<li>Для установки новой jQuery библиотеки просто выполните в терминале команду "<strong>bower i plugin-name</strong>". Библиотека автоматически будет размещена в папке <strong>app/libs</strong>. Для установки Bower просто выполните команду npm i -g bower в трминале. После этого укажите все ссылки на скрипты jQuery библиотек в таске <strong>'libs'</strong> файла (gulpfile.js);</li>
	<li>Весь ваш JS код пишите в <strong>app/js/common.js</strong>;</li>
	<li>Все Sass переменные размещайте в <strong>app/sass/_vars.sass</strong>;</li>
	<li>Все CSS медиазапросы размещайте в <strong>app/sass/_media.sass</strong>;</li>
	<li>Все CSS стили jQuery библиотек размещайте в <strong>app/sass/_libs.sass</strong>;</li>
	<li>Все базовые стили (html, body, fonts, buttons, etc...) размещайте в <strong>app/sass/_base.sass</strong>;</li>
	<li>В файле <strong>app/header.sass</strong> должны размещаться стили, предназначенные для отображения верхней части сайта на первом экране (на самых больших мониторах). Здесь отображаются стили как главной, так и всех внутренних страниц;</li>
	<li>Переименуйте <strong>ht.access</strong> в <strong>.htaccess</strong> перед размещением на рабочем сервере. Этот файл содержит правила для кеширования файлов на сервере.</li>
</ol>
