[![Build Status](https://travis-ci.org/2gis/makeup.svg)](https://travis-ci.org/2gis/makeup) [![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/2gis/makeup?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

EN | [RU](README-RU.md)

# Makeup

Makeup is aimed at development and convenient quality assurance of markup on web projects. You'll certainly make use of Makeup if your design is based on independent blocks and you prioritize stability and reliability.

See our interactive [Makeup promotion site](http://2gis.github.io/makeup)!

## Features

Makeup is a JavaScript library, providing a visual interface for isolated development and quick manual regression testing of web pages, built from absolutely independent blocks.

Makeup lets you:

* Compare page design with the sample layout
* Monitor blocks for modifications and content mismatching
* Develop isolated blocks with ease

Makeup supports keyboard shortcuts. They are listed in a [cheatsheet](docs/en/keyboard.md).

Try all the features on the [Makeup demo page](http://2gis.github.io/makeup/demo)!


## Makeup Express

Express version of Makeup can be launched on any website except those with HTTP header `content-security-policy`. To use it, run the following script from the developer tools console of your browser:

```javascript
var s=document.createElement('script');
s.src ="//2gis.github.io/makeup/autoload/script.js";
document.body.appendChild(s);
```

## Quick start

1. Make a web page with all resourses of your page's layout (markup, styles and images):

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>Makeup</title>
        <link rel="stylesheet" href="style.css"> <!-- project styles -->
    </head>
    <body>
        <button class="button">My button</button> <!-- markup -->
    </body>
    </html>
    ```

2. Link the script and styles to your page:

   ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>Makeup</title>
        <link rel="stylesheet" href="style.css">

        <script src="makeup.js"></script><!-- Makeup -->
        <link rel="stylesheet" href="makeup.css"> <!-- Makeup styles -->
    </head>
    <body>
        <div style="display: none;">
            <button class="button">My button</button>
        </div>
    </body>
    </html>
    ```

3. Initialize the Makeup

    ```js
    Makeup(params, templating);
    ```

   * Here `params` is an optional argument for parameters, including the blocks list. If no value was passed, all parameters will be used with default values and the blocks list will be generated from current DOM tree.
   * `templating` is an optional function which accepts the name (and parameters) of a particular block and returns its html:


    ```js
    templating(ctx) {
        return html;
    };
    ```

    * `ctx` is an object, identifying the selected block and its parameters
    * `html` is the returned html code of the selected block.

    If no instance of `templating` was passed, a built-in function will be used. It searches for `$('.' + ctx.name)` in the DOM tree and takes its `outerHTML`.


  [Initialization data format](docs/format.md)

## Examples

Can be found in the [`demo/`](demo/) subfolder. Just open any `.html` file in your browser.

## Development

If you would like to take part in development of Makeup,


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

2. Launch Makeup with

    ```bash
    npm i
    npm start
    ```

    Demo page will then be available at [localhost:3333/demo](http://localhost:3333/demo).



Another project named "node-makeup" had been published in *npm* under the name "makeup" till 23.10.2015. You can find it at [defunctzombie/node-makeup](https://github.com/defunctzombie/node-makeup).
