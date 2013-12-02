## Web Application workflows and useful tools

---
= data-x='1000'

## Useful Tools

* Total Finder
* [Google Chrome Canary](https://www.google.com/intl/en/chrome/browser/canary.html)
* Alfred
* Dash
* Sublime plugins
  * Docblockr
  * VCS Gutter
  * Sublime linter
* How to sync all of these
  * [dropbox](https://github.com/danielhusar/my-sublime-plugins#sync-between-devices)
  * [dotfiles](http://dotfiles.github.io/)


---
= data-x='2000'

## Progressive enhancement
* Mobile first
* Avoid respond.js and still support old browsers
* Don't use ids
* CSS Transitions

---
= data-x='3000'

## Javascript good practise

### Unit tests


```javascript
describe('APP', function() {
  describe('Prototypes', function() {
    it('FMT is working.', function () {
      APP.fmt("test%@1%@2", 1, 2).should.equal('test12');
    });
  });
});
```

---
= data-x='4000'


## Javascript good practise

### Bindings

Not so good

```javascript
$('ul li').click(fn);
```

Better

```javascript
$('ul').on('click', 'li', fn);
```

Best

```javascript
$('[data-items]').on('click.app', '[data-item]', fn);
```

---
= data-x='5000'

## Javascript good practise

### Closures and strict mode


```javascript
(function(window, document, APP, $, undefined) {
  'use strict';

  ...

})(this, this.document, this.APP, this.jQuery);
```


---
= data-x='6000'

## Javascript good practise

### Promises


```javascript
var promise = function(){
  var df = $.Deferred();

  if (...) {
    df.resolve();
  } else {
    df.reject();
  }

  return df.promise();
}

var testPromise = promise();
testPromise.done(fn);
```

---
= data-x='7000'

## Javascript good practise

### Declare variables them outside of loops


Not so good

```javascript
for(var i = 0; i < someArray.length; i++) {
```

Better

```javascript
for(var i = 0, len = someArray.length; i < len;  i++) {
```

---
= data-x='8000'

## Javascript good practise

### Cache selectors


```javascript
var $el = $(...);

$el.on(...);
...
$el.addClass(...);
```

---
= data-x='9000'


## Javascript good practise

### Lint your code

* jshint
* eslint

---
= data-x='10000'


## Grunt

* Javascript linting
* Javascript beauty
* Running unit tests
* Switching between prod and dev environment
* Start http server with watch task
* Creating sprites
* Minifying images
* Creating screenshots

---
= data-x='11000'

## Yeoman
* [Community generators](http://yeoman.io/community-generators.html)
* Custom generator

---
= data-x='12000'

## Bower
* Package manager

---
= data-x='13000'

## Thank you