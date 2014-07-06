# grunt-sassdoc [![Built with Grunt](https://cdn.gruntjs.com/builtwith.png)](http://gruntjs.com/) [![Build Status: Linux](https://travis-ci.org/pascalduez/grunt-sassdoc.png?branch=master)](https://travis-ci.org/pascalduez/grunt-sassdoc)

> [SassDoc](https://github.com/HugoGiraudel/SassDoc) grunt task.



## Getting Started

If you haven't used [grunt][] before, be sure to check out the [Getting Started][] guide, as it explains how to create a [gruntfile][Getting Started] as well as install and use grunt plugins. Once you're familiar with that process, install this plugin with this command:

```sh
npm install --save-dev grunt-sassdoc
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-sassdoc');
```

*Tip: the [load-grunt-tasks](https://github.com/sindresorhus/load-grunt-tasks) module makes it easier to load multiple grunt tasks.*


[grunt]: http://gruntjs.com
[Getting Started]: https://github.com/gruntjs/grunt/wiki/Getting-started



## Documentation

See the [Gruntfile](Gruntfile.js) in this repo for a full example.


## SassDoc task
_Run this task with the `grunt sassdoc` command._

Task targets, files and options may be specified according to the grunt [Configuring tasks](http://gruntjs.com/configuring-tasks) guide.



## Options

Any specified option will be passed through directly to SassDoc, thus you can specify any option that SassDoc supports.
See the [SassDoc documentation](https://github.com/HugoGiraudel/SassDoc#pass-extra-variables-to-the-view) for a list of supported options.

#### config

Type: `String`  
Default: `null`

Path to a view configuration file.

#### title

Type: `String`  
Default: `'SassDoc'`

Generated documentation page title.

#### display_access

Type: `Array`  
Default: `['public', 'private']`

Access levels that should be displayed.

#### display_alias

Type: `Boolean`  
Default: `false`

Enable/disable display of alias items.

_**Heads up**: If a config file is passed and found, its options will prevail over defauts.
Additionnal options passed to the grunt task, will complement it but not override it.
You should really manage your options in one place._



### Config examples

```js
grunt.initConfig({
  sassdoc: {
    default: {
      src: 'sass',
      dest: 'docs',
      options: {
        config: 'test/view.json'
      }
    }
  },
});
```

```js
grunt.initConfig({
  sassdoc: {
    default: {
      src: 'sass',
      dest: 'docs',
      options: {
        title: 'My cool project'
        display_access: ['public'],
        display_alias: true
      }
    }
  },
});
```

## Authors

[Pascal Duez](http://pascalduez.me)


## Licence

grunt-sassdoc is [unlicensed](http://unlicense.org/).
