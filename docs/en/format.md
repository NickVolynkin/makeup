# Initialization data format

## `params`

```js
{
    label: 'project name',
    items: [item1, item2, ...]
    ... // @see source/js/params.js:102
}
```

## `item`

`item` is either a block or a group. A group can contain other groups and/or blocks. Nesting depth is not limited. The `item` object has the following structure:

```js
{
    // {String} Name to show in the list
    "name": "",

    // {Object} Styles, applied to the current and all nested items. See the paragraph on styles.
    "styles": {},

    // {Array} An array of nested items.

    "items": [
        // {item}
        ...
    ]
}
```
Any other properties can be added to an `item` object.

## `styles`

```js
"styles": {
    // {String} Styles, applied to the wrapper Стили, применяемые к врапперу
    "wrapper": "color: red;",

    // {String} Styles, applied to the image container
    "image": "background: green; border: 1px solid yellow;",

    // {String} Styles, applied to the markup container
    "markup": "box-shadow: 0 0 3px rgba(0, 0, 0, .3)"
}
```
If both an item and some of its parents have styles, those will be joined (by concatenation of defining strings). Styles are prioritized from root to end element with the latter having the highest priority.
