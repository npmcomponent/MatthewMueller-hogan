*This repository is a mirror of the [component](http://component.io) module [matthewmueller/hogan](http://github.com/matthewmueller/hogan). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/matthewmueller-hogan`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# hogan

  hogan.js as a component.

## Installation

    $ component install matthewmueller/hogan

## Example

```js
var hogan = require('hogan'),
    obj = { name : 'matt', age : 23 }
    str = 'hi my name is {{name}}, I am {{age}} years old.';

// Compile the function
var tpl = hogan.compile(str);
tpl(obj); // => hi my name is matt, I am 23 years old.'

// Or.. compile and render immediately
hogan(str, obj);

```

## API

### hogan(str, [obj], [opts])

Compile and render `str` given the context `obj`. Use `opts` to pass options directly into the hogan compiler.

### hogan#compile(str, [opts])

Compile a mustache `str`. Optional `opts` to pass optiosn directly to the hogan compiler. Return a template function which you can invoke.

```js
var tpl = hogan.compile('Hello from {{location}}!');
tpl('Kyoto, Japan'); // Hello from Kyoto, Japan!
```

## License

  MIT
