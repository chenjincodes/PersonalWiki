## Certain array functions like `compact()`, `difference()`, and `without()` [Back](./../underscore.md)

There are some interesting array functions that will be discussed here like `compact()`, `difference()`, and `without()`.

Firstly, according to the implementation of `_.compact()`, it's not hard to know that this method is always used to filter out `false` from an array.

```js
_.compact = function(array) {
    return _.filter(array, _.identity);
};
```

`_.filter()` is similar to `Array.prototype.filter()`, and it's used to filter out some elements under a given condition, as the function `_.identity` describes.