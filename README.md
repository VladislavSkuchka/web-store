Учебный проект "Верстка интернет магазина"
=========================================
**Страницы проекта**

Название страниц| Содержание страниц
----------------|--------------------
index.html      | Главная страница сайта
product.html    | Страница с товаром, флексслайдером с которой осуществляетцо заказ товаров
category.html   | Страница с каталогом, сайжбаром и товаром

**Структура папок**

Название папок  | Содержание файла
----------------|----------------------
app             | Директория с готовым проектом
app/css         | Готовые стили к продакшену
app/js          | Готовый js к продакшену
app/img         | Готовые картинки к продакшену
app/fonts       | Шрифты
src             | Директория с исходными файлыми
src/css         | Исходные стили, здесь мы пишем наши стили и они будут конвертироваться в app/css
src/img         | Исходные картинки, они будут минифицироваться и перегоняться в app/img
src/js          | Исходный js будет минифицироваться и переносится в app/js
src/sprite      | Папка для нарезанных картинок под будущие спрайты, после конветрации попадут в app/img

---
**Используемые технологии**

 Сборщик проектов Gulp.js
 Фреймворк Bootstrap 3
 Библиотека JavaScript - jQuery

---
**Используемые плагины**

Название плагинов | Цель плагинов
------------------|-----------------
 jquery-ui        |для создания range slider
 formstayler      |для стилизации элементов форм
 flexslider       |для стилизации карусели на странице product.html
 slicknav         |для стилизации мобильного меню

---
**Используемые шрифты и иконки**

Шрифты            | названия
------------------|---------------
Font-Awesome      | Иконочный шрифт
                  |
Harmonia_black    | Сконвертированные шрифты
Harmonia_regular  |
Harmonia_semibold |
Harmonia_bold     |
Harmonia_italic   |
Harmonia_light    |

---
**Стандартные компоненты и классы**

Характеристика    | Стили
------------------|-------------------
Заголовки         |.title
                  |.title.big
                  |.title.small
------------------|--------------------
Kнопки            |.btn-default
                  |.btn-radius
------------------|---------------------
Отступы блоков    |.default-section
Теустовие стили   |.default-span
                  |.default-p
------------------|---------------------
Формы             |.checkbox-group input
                  |.checkbox-group label
                  |.subscribe-form
                  |.subscribe-input-group
                  |.subscribe-input-group label
                  |.subscribe-input
------------------|-------------------------
Блоки с продукцией|.item
                  |.best-item
                  |.new-item
------------------|---------------------------
Font-Awesome      |.custom-icon
------------------|--------------------------
Font-Awesome под  |.icon-add-to-cart-ic:hover
 hover            |.icon-cart-ic:hover
                  |.icon-like-ic:hover
                  |.icon-search-ic:hove
                  |.icon-share-ic:hover
                  |.icon-user-ic:hover
------------------|----------------------------
Флекс контейнер   |.flex-container
------------------|----------------------------
Выравнивание      |.align-center
элементов         |.align-end
                  |.justify-sp-between
------------------|----------------------------
Кольори           |.orange-text
                  |.light-grey-text
                  |.red-bg
                  |.black-bg
                  |.blue-bg
                  |.green-bg
                  |.white-bg
                  |.light-orange-bg
                  |.orange-bg
------------------|-----------------------------















```js
var gulp         = require('gulp'), // Подключаем Gulp
    browserSync  = require('browser-sync'), // Подключаем Browser Sync
    concat       = require('gulp-concat'), // Подключаем gulp-concat (для конкатенации файлов)
    uglify       = require('gulp-uglifyjs'), // Подключаем gulp-uglifyjs (для сжатия JS)
    cssnano      = require('gulp-cssnano'), // Подключаем пакет для минификации CSS
    rename       = require('gulp-rename'), // Подключаем библиотеку для переименования файлов
    imagemin     = require('gulp-imagemin'), // Подключаем библиотеку для работы с изображениями
    pngquant     = require('imagemin-pngquant'), // Подключаем библиотеку для работы с png
    cache        = require('gulp-cache'), // Подключаем библиотеку кеширования
    autoprefixer = require('gulp-autoprefixer'),// Подключаем библиотеку для автоматического добавления префиксов
    spritesmith = require('gulp.spritesmith'), // Подключение библиотеки для создания спрайтов
    merge = require('merge-stream');

```

```