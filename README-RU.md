[![Build Status](https://travis-ci.org/2gis/makeup.svg)](https://travis-ci.org/2gis/makeup) [![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/2gis/makeup?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[EN](README.md) | RU

# Makeup

## Что такое Makeup?

Makeup – инструмент для вёрстки и приятного контроля за качеством вёрстки на веб-проектах.

Вы поладите с Makeup, если ваша верстка основана на независимых блоках, а вам важна стабильность и надежность проекта.

Если говорить формально, Makeup – это js-библиотека, которая предоставляет визуальный интерфейс для изолированной разработки и быстрого ручного регрессионого тестирования вёрстки, основанной на абсолютно-независимых блоках.

Обязательно зайдите на [промо-сайт Makeup](http://2gis.github.io/makeup)!





## Чем Makeup может быть мне полезен?

Makeup предназначен для:

* Сравнения вёрстки блоков с исходными дизайн-макетами,
* Контроля за состояниями блоков (модификации блоков, разный контент),
* Комфортной изолированной разработки блоков.

### Примеры

Посмотреть на фичи Makeup можно на [демо-сайте](http://2gis.github.io/makeup/demo).

Все примеры можно найти в папке [demo/](demo/): достаточно открыть в браузере один из `.html` файлов.

### Горячие клавиши

Для удобства работы в Makeup есть набор горячих клавиш. Смотрите
[шпаргалку](docs/ru/keyboard.md).

## Как начать использовать Makeup?

### Экспресс-версия Makeup

Экспресс-версию Makeup можно загрузить почти на любой сайт (кроме тех, где выставлен HTTP заголовок content-security-policy). Для этого скопируйте и выполните строчку кода в консоли Dev Tools вашего браузера:

```js
var s=document.createElement('script');s.src ="//2gis.github.io/makeup/autoload/script.js";document.body.appendChild(s)
```

### Быстрый старт

  1. Создайте страницу со всеми ресурсами вашей вёрстки (разметка, стили, изображения):

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <title>Makeup</title>
      <link rel="stylesheet" href="style.css"> <!-- Стили проекта -->
  </head>
  <body>
      <button class="button">My button</button> <!-- Разметка -->
  </body>
  </html>
  ```

1. Подключите два файла: скрипт и стили Makeup.

  ```html
  <!DOCTYPE html>
  <html>
  <head>
      <title>Makeup</title>
      <link rel="stylesheet" href="style.css">

      <script src="makeup.js"></script><!-- Сам Мейкап -->
      <link rel="stylesheet" href="makeup.css"> <!-- Стили Мейкапа -->
  </head>
  <body>
      <div style="display: none;">
          <button class="button">My button</button>
      </div>
  </body>
  </html>
  ```

1. Инициализируйте Мейкап

  ```js
  Makeup(params, templating);
  ```
  Подробное описание формата данных для инициализации вынесено в [отдельный документ](docs/ru/format.md).









## Разработка

Если вы хотите разрабатывать сам Мейкап – это здорово. Чтобы начать, следуйте инструкции:

1. Убедитесь, что у вас установлены `nodejs`, `npm` и `gulp`.

1. Форкните этот репозиторий и клонируйте свой форк:

    ```bash
    git clone git@github.com:<your_name>/makeup.git
    cd makeup
    ```
    Чтобы залить свои изменения в основной репозиторий, создайте pull-request (подробнее в [GitHub Flow](https://guides.github.com/introduction/flow/)).

    Вы также можете напрямую клонировать этот репозиторий, но вы не сможете заливать в него изменения (git push) или создавать pull-request'ы.

    ```bash
    git clone git@github.com:2gis/makeup.git
    cd makeup
    ```
2. Запустите сборку

    ```bash
    npm i
    npm start
    ```

Демо будет доступно по адресу [localhost:3333/demo](http://localhost:3333/demo).



До 23 октября 2015 года под именем «makeup» в npm находился другой проект — «node-makeup». Вы можете получить доступ к проекту «node-makeup» в [гите](https://github.com/defunctzombie/node-makeup).

Another project ("node-makeup") has been published in npm with name "makeup" till 23.10.2015. You can find previous project in [github with name "node-makeup"](https://github.com/defunctzombie/node-makeup).
