grunt-localtunnel-me [![Build Status](https://travis-ci.org/simshanith/grunt-localtunnel-me.svg?branch=master)](https://travis-ci.org/simshanith/grunt-localtunnel-me) [![Dependency Status](https://david-dm.org/simshanith/grunt-localtunnel-me.svg)](https://david-dm.org/simshanith/grunt-localtunnel-me) [![devDependency Status](https://david-dm.org/simshanith/grunt-localtunnel-me/dev-status.svg)](https://david-dm.org/simshanith/grunt-localtunnel-me#info=devDependencies)
===============

> Expose local ports to a public URL with https://localtunnel.me

[![NPM](https://nodei.co/npm/grunt-localtunnel-me.png?downloads=true&stars=true)](https://nodei.co/npm/grunt-localtunnel-me/)

## Getting Started
This plugin requires Grunt.

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-localtunnel-me --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-localtunnel-me');
```

## The "localtunnel" task

### Overview
In your project's Gruntfile, add a section named `localtunnel` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  localtunnel: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    }
  }
})
```

### Options

#### port
Type: `Integer`  
Default: `8000`

The port to tunnel. Local server should already be listening to this port before attempting to tunnel.

#### subdomain
Type: `String`
Default: `undefined`

Request a subdomain to tunnel to on <https://localtunnel.me>.

#### local_host
Type: `String`
Default: `localhost`

The local hostname for the requests tunnel.


#### open
Type: `String | Boolean`
Default: `false`

If `true`, opens the browser to the public tunnel page. If a string, the option is treated as a path, eg:

```js
grunt.initConfig({
  localtunnel: {
    myTunnel: {
     options: {
      open: '/path/to/workspace/',
      subdomain: 'uniqueworkspace'
   }
  }
}
});
```
...should expect to open `https://uniqueworkspace.localtunnel.me/path/to/workspace/` upon successful tunnel.

#### keepalive
Type: `Boolean`  
Default: `false`

Keep the server alive indefinitely. Note that if this option is enabled, any tasks specified after this task will _never run_. By default, once grunt's tasks have completed, the web server stops. This option changes that behavior.

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
_(Nothing yet)_

## License
Copyright (c) 2014 Shane Daniel. Licensed under the MIT license.
