# angular-jquery

**🚧 This module is deprecated and not maintained anymore 🚧**

jQuery-like extensions for AngularJS embedded jQLite

## Getting Started

+ Install with bower, `npm install angular-jquery --save`

+ Or download the [production][min] or the [development][max] version.

[min]: https://raw.github.com/mgcrea/angular-jquery/master/dist/angular-jquery.min.js
[max]: https://raw.github.com/mgcrea/angular-jquery/master/dist/angular-jquery.js

In your app.js:

```js
import 'angular-jquery';

angular.module('myApp', ['mgcrea.jquery'])
```

## Documentation

Available components:

+ jQuery: selector (wrapping document.querySelectorAll)

+ dimensions: .offset(), .height(), .width()

+ debounce: debounce() function

## Examples

```js

  .directive('myDirective', function(jQuery) {

    return {
      restrict: 'EAC',
      link: function postLink(scope, iElement, iAttrs) {

        var myElements = jQuery('.container > .element');
        angular.each(myElements, function(el) {
          console.warn(el.offset(), el.width())
        })

      }
    };

  });
```
