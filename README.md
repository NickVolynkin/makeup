![MakeUP logo](docs/makeup.png)

[![Build Status](https://travis-ci.org/2gis/makeup.svg)](https://travis-ci.org/2gis/makeup) [![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/2gis/makeup?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

English | [Русский](README-RU.md)
## What is MakeUP?

MakeUP is a tool for development and comfortable quality assurance of markup on web projects. You'll certainly find it useful if your design is based on independent blocks and you prioritize stability and reliability.

MakeUP is a JavaScript library. It provides visual interface for isolated development and quick manual regression testing of web pages, built from independent blocks.

See our interactive [MakeUP promotion site](http://2gis.github.io/makeup)!

## Why should I use it?

MakeUP lets you:

* Compare page design with the sample layout,
* Monitor blocks for modifications and mismatching content,
* Develop isolated blocks with ease.

###Examples

Features of MakeUP can be seen on the [MakeUP demo page](http://2gis.github.io/makeup/demo).

Examples can be found in the [demo/](demo/) subfolder. Just open any `.html` file in your browser.

### Shortcuts

MakeUP has convenient keyboard shortcuts. See the [cheatsheet](docs/en/keyboard.md).

## How can I use it?



### MakeUP Express

Express version of MakeUP can be launched on any website except those with HTTP header `content-security-policy`. To use it, run the following script from the developer tools console of your browser:

```javascript
var s=document.createElement('script');
s.src ="//2gis.github.io/makeup/autoload/script.js";
document.body.appendChild(s);
```

### Quick start with MakeUP

1. Make a web page with all resourses of your page's layout (markup, styles and images):

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>MakeUP</title>
        <link rel="stylesheet" href="style.css"> <!-- project styles -->
    </head>
    <body>
        <button class="button">My button</button> <!-- markup -->
    </body>
    </html>
    ```

2. Link the files for MakeUP script and styles to your page:

   ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>MakeUP</title>
        <link rel="stylesheet" href="style.css">

        <script src="makeup.js"></script><!-- MakeUP -->
        <link rel="stylesheet" href="makeup.css"> <!-- MakeUP styles -->
    </head>
    <body>
        <div style="display: none;">
            <button class="button">My button</button>
        </div>
    </body>
    </html>
    ```

3. Initialize the MakeUP

    ```javascript
    Makeup(params, templating);
    ```

    See the full [reference on initialization data format](docs/en/format.md).

## Development

You are welcome to take part in the development of MakeUP. To start working, follow this instruction:

1. Make sure that you have *nodejs*, *npm* and *gulp* installed.

1. Fork this repository and clone your fork:

    ```bash
    git clone git@github.com:<your_name>/makeup.git
    cd makeup
    ```
    To commit your contribution, make a pull request (use the [GitHub Flow](https://guides.github.com/introduction/flow/)).

    You can also clone this repository directly, but then you won't be able to push to it or make pull requests:

    ```bash
    git clone git@github.com:2gis/makeup.git
    cd makeup
    ```

2. Launch MakeUP with

    ```bash
    npm i
    npm start
    ```

    Demo page will then be available at [http://localhost:3333/demo](http://localhost:3333/demo).

## License

MakeUP is published under the Mozilla Public License, version 2.0.

## node-makeup

A project named "node-makeup" had been published in *npm* under the name "makeup" till 23.10.2015. You can find it at [defunctzombie/node-makeup](https://github.com/defunctzombie/node-makeup).
