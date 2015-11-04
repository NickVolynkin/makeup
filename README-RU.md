![MakeUP logo](docs/makeup.svg)

[![Build Status](https://travis-ci.org/2gis/makeup.svg)](https://travis-ci.org/2gis/makeup) [![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/2gis/makeup?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[English](README.md) | Русский
## Что такое MakeUP?

MakeUP – инструмент для вёрстки и приятного контроля за качеством вёрстки на веб-проектах.

Вы поладите с MakeUP, если ваша вёрстка основана на независимых блоках, а вам важна стабильность и надежность проекта.

Если говорить формально, MakeUP – это js-библиотека, которая предоставляет визуальный интерфейс для изолированной разработки и быстрого ручного регрессионого тестирования вёрстки, основанной на абсолютно-независимых блоках.

Обязательно зайдите на [промо-сайт MakeUP](http://2gis.github.io/makeup)!

## Чем MakeUP может быть мне полезен?

MakeUP предназначен для:

* Сравнения вёрстки блоков с исходными дизайн-макетами,
* Контроля за состояниями блоков (модификации блоков, разный контент),
* Комфортной изолированной разработки блоков.

### Примеры

Посмотреть на фичи MakeUP можно на [демо-сайте](http://2gis.github.io/makeup/demo).

Все примеры можно найти в папке [demo/](demo/): достаточно открыть в браузере один из `.html` файлов.

### Горячие клавиши

Для удобства работы в MakeUP есть набор горячих клавиш. Смотрите
[шпаргалку](docs/ru/keyboard.md).

## Как начать использовать MakeUP?

### Экспресс-версия MakeUP

Экспресс-версию MakeUP можно загрузить почти на любой сайт (кроме тех, где выставлен HTTP заголовок content-security-policy). Для этого скопируйте и выполните строчку кода в консоли Dev Tools вашего браузера:

```js
var s=document.createElement('script');
s.src ="//2gis.github.io/makeup/autoload/script.js";
document.body.appendChild(s)
```

### Быстрый старт

  1. Создайте страницу со всеми ресурсами вашей вёрстки (разметка, стили, изображения):

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <title>MakeUP</title>
      <link rel="stylesheet" href="style.css"> <!-- Стили проекта -->
  </head>
  <body>
      <button class="button">My button</button> <!-- Разметка -->
  </body>
  </html>
  ```

1. Подключите два файла: скрипт и стили MakeUP.

  ```html
  <!DOCTYPE html>
  <html>
  <head>
      <title>MakeUP</title>
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

  Смотрите подробное [описание формата данных для инициализации](docs/ru/format.md).

## Разработка

Если вы хотите разрабатывать сам Мейкап – это здорово. Чтобы начать, следуйте инструкции:

1. Убедитесь, что у вас установлены *nodejs*, *npm* и *gulp*.

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

## Лицензия

MakeUP опубликован под лицензией Mozilla Public License, version 2.0.

## node-makeup

До 23 октября 2015 года под именем «makeup» в *npm* находился другой проект — «node-makeup». Вы можете получить доступ к проекту «node-makeup» на [defunctzombie/node-makeup](https://github.com/defunctzombie/node-makeup).
