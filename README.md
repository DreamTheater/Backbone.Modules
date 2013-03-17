[lnk]: https://travis-ci.org/DreamTheater/Backbone.Modules
[img]: https://secure.travis-ci.org/DreamTheater/Backbone.Modules.png

# Backbone.Modules [![Build Status][img]][lnk]
The plugin is for defining modules.

**Dependencies:**

  - [Backbone](https://github.com/documentcloud/backbone) `>= 0.9.10`
  - [Underscore](https://github.com/documentcloud/underscore) `>= 1.4.4`

## Reference API
### Backbone
#### Static members
  - Function `define(namespace, object)`
    - String `namespace`
    - Object `object`

## Getting Started
### Define Backbone classes
```js
Backbone.define('company.application.Model', Backbone.Model.extend());

Backbone.define('company.application.Collection', Backbone.Collection.extend({
    model: company.application.Model
}));
```

### Define custom class
```js
var Class = Backbone.define('company.application.Class', function () {
    this.instanceProperty = 'instanceProperty';
});

Class.staticProperty = 'staticProperty';
Class.prototype.prototypeProperty = 'prototypeProperty';
```

## Changelog
### 0.1.2
  - When absent argument `object` method `define` just returns current value

### 0.1.1
  - New usage method

### 0.1.0
  - Initial release
