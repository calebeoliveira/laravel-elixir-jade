laravel-elixir-jade-angular
=========================

Simple Laravel Elixir wrapper to compile Jade to AngularJS views.

Original project by Thomas Creeten, see https://github.com/CREEATION/laravel-elixir-jade


### Installation
Run the following command in your Laravel project:

    npm install laravel-elixir-jade-angular

Next, add the following line into your gulpfile.js:

    require('laravel-elixir-jade-angular');

And your done!

***NOTE 1: Jade files, with default options, should be in a `/resources/jade/` folder. Make sure to create one!***

***NOTE 2: Specify an `extension` option for custom output file extensions***

### Options
For Jade's options, see http://jade-lang.com/api/

Compiled Templates are located in your `/resources/views/` folder as default.

All other options should be pretty straight forward.

These are the default options:

```javascript
{
    baseDir: './resources',
    dest: '/views/',
    pretty: true,
    search: '**/*.jade',
    src: '/jade/',
    extension: '.html'
}
```

### Example gulpfile.js

```javascript
var elixir = require('laravel-elixir');

require('laravel-elixir-jade-angular');

elixir(function(mix) {
	mix.jade({
        search: '*.jade',
        src: '/templates/'
	});
});
```
