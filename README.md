# api documentation for  [gulp-notify (v3.0.0)](https://github.com/mikaelbr/gulp-notify)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-gulp-notify.svg)](https://travis-ci.org/npmdoc/node-npmdoc-gulp-notify)
#### gulp plugin to send messages based on Vinyl Files or Errors to Mac OS X, Linux or Windows using the node-notifier module. Fallbacks to Growl or simply logging

[![NPM](https://nodei.co/npm/gulp-notify.png?downloads=true)](https://www.npmjs.com/package/gulp-notify)

[![apidoc](https://npmdoc.github.io/node-npmdoc-gulp-notify/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-gulp-notify_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-gulp-notify/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-gulp-notify/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Mikael Brevik",
        "email": "mikaelbre@gmail.com",
        "url": "https://github.com/mikaelbr"
    },
    "bugs": {
        "url": "https://github.com/mikaelbr/gulp-notify/issues"
    },
    "dependencies": {
        "gulp-util": "^3.0.8",
        "lodash.template": "^4.4.0",
        "node-notifier": "^5.0.1",
        "node.extend": "^1.1.6",
        "through2": "^2.0.3"
    },
    "description": "gulp plugin to send messages based on Vinyl Files or Errors to Mac OS X, Linux or Windows using the node-notifier module. Fallbacks to Growl or simply logging",
    "devDependencies": {
        "gulp": "^3.8.10",
        "gulp-plumber": "^1.1.0",
        "mocha": "^3.2.0",
        "should": "^11.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "a04b8af9acdbe4e63c845678ce0c3d30694c59a3",
        "tarball": "https://registry.npmjs.org/gulp-notify/-/gulp-notify-3.0.0.tgz"
    },
    "engines": {
        "node": ">=0.8.0",
        "npm": ">=1.2.10"
    },
    "gitHead": "658efc5d81ae0d5224a053100653d46000319373",
    "homepage": "https://github.com/mikaelbr/gulp-notify",
    "keywords": [
        "gulpplugin",
        "notify",
        "gulp",
        "notification",
        "reporter",
        "windows notification",
        "mac notification",
        "notify-send",
        "notify-osd",
        "growl"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "mikaelb",
            "email": "mikaelbre@gmail.com"
        }
    ],
    "name": "gulp-notify",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/mikaelbr/gulp-notify.git"
    },
    "scripts": {
        "gulp": "gulp --gulpfile ./examples/gulpfile.js",
        "test": "mocha -R spec"
    },
    "version": "3.0.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module gulp-notify](#apidoc.module.gulp-notify)
1.  [function <span class="apidocSignatureSpan">gulp-notify.</span>logLevel (newLogLevel)](#apidoc.element.gulp-notify.logLevel)
1.  [function <span class="apidocSignatureSpan">gulp-notify.</span>logger (newLogger)](#apidoc.element.gulp-notify.logger)
1.  [function <span class="apidocSignatureSpan">gulp-notify.</span>on (event, fn)](#apidoc.element.gulp-notify.on)
1.  [function <span class="apidocSignatureSpan">gulp-notify.</span>onError (options, callback)](#apidoc.element.gulp-notify.onError)
1.  [function <span class="apidocSignatureSpan">gulp-notify.</span>withReporter (reporter)](#apidoc.element.gulp-notify.withReporter)
1.  object <span class="apidocSignatureSpan">gulp-notify.</span>extra_api

#### [module gulp-notify.extra_api](#apidoc.module.gulp-notify.extra_api)
1.  [function <span class="apidocSignatureSpan">gulp-notify.extra_api.</span>logError (options, isError)](#apidoc.element.gulp-notify.extra_api.logError)
1.  [function <span class="apidocSignatureSpan">gulp-notify.extra_api.</span>logLevel (newLogLevel)](#apidoc.element.gulp-notify.extra_api.logLevel)
1.  [function <span class="apidocSignatureSpan">gulp-notify.extra_api.</span>logger (newLogger)](#apidoc.element.gulp-notify.extra_api.logger)
1.  [function <span class="apidocSignatureSpan">gulp-notify.extra_api.</span>onError (options, callback)](#apidoc.element.gulp-notify.extra_api.onError)



# <a name="apidoc.module.gulp-notify"></a>[module gulp-notify](#apidoc.module.gulp-notify)

#### <a name="apidoc.element.gulp-notify.logLevel"></a>[function <span class="apidocSignatureSpan">gulp-notify.</span>logLevel (newLogLevel)](#apidoc.element.gulp-notify.logLevel)
- description and source-code
```javascript
logLevel = function (newLogLevel) {
  if (newLogLevel === void 0) return logLevel;
  logLevel = newLogLevel;
}
```
- example usage
```shell
...
    * [options.emitError](#optionsemiterror)
    * [options.message](#optionsmessage)
    * [options.title](#optionstitle)
    * [options.templateOptions](#optionstemplateoptions)
    * [options.notifier](#optionsnotifier)
  * [notify.withReporter(Function)](#notifywithreporterfunction)
  * [notify.onError()](#notifyonerror)
  * [notify.logLevel(level)](#notifyloglevellevel)
* [Disable 'gulp-notify'](#disable-gulp-notify)
* [Examples](#examples)
  * [As jshint reporter](#as-jshint-reporter)
* [License](#license)

<!-- toc stop -->
...
```

#### <a name="apidoc.element.gulp-notify.logger"></a>[function <span class="apidocSignatureSpan">gulp-notify.</span>logger (newLogger)](#apidoc.element.gulp-notify.logger)
- description and source-code
```javascript
logger = function (newLogger) {
  if (!newLogger) return fnLog;
  fnLog = newLogger;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.gulp-notify.on"></a>[function <span class="apidocSignatureSpan">gulp-notify.</span>on (event, fn)](#apidoc.element.gulp-notify.on)
- description and source-code
```javascript
on = function (event, fn) {
  if (!notifier) return;
  return notifier.on(event, function (notifyObject, options) {
    return fn(options);
  });
}
```
- example usage
```shell
...
on each file.

#### options.emitError
Type: 'Boolean'
Default: 'false'

If the returned stream should emit an error or not.
If 'emitError' is true, you have to handle '.on('error')'
manually in case the notifier (gulp-notify) fails. If
the default 'false' is set, the error will not be emitted
but simply printed to the console.

This means you can run the notifier on a CI system without
opting it out but simply letting it fail gracefully.
...
```

#### <a name="apidoc.element.gulp-notify.onError"></a>[function <span class="apidocSignatureSpan">gulp-notify.</span>onError (options, callback)](#apidoc.element.gulp-notify.onError)
- description and source-code
```javascript
onError = function (options, callback) {
  var reporter;
  options = options || {};
  var templateOptions = options.templateOptions || {};
  var callback = callback || function (err) {
    err && logError({
      title: "Error running notifier",
      message: "Could not send message: " + err.message
    }, true);
  };

  if (options.notifier) {
    reporter = options.notifier;
  } else {
    if (options.host || options.appName || options.port) {
      notifier = new notifier.Notification({
        host: options.host || 'localhost',
        appName: options.appName || 'gulp-notify',
        port: options.port || '23053'
      });
    }
    reporter = notifier.notify.bind(notifier);
  }
  return function (error) {
    var self = this;
    report(reporter, error, options, templateOptions, function () {
      callback.apply(self, arguments);
      self.emit && self.emit('end');
    });
  };
}
```
- example usage
```shell
...
    * [options.onLast](#optionsonlast)
    * [options.emitError](#optionsemiterror)
    * [options.message](#optionsmessage)
    * [options.title](#optionstitle)
    * [options.templateOptions](#optionstemplateoptions)
    * [options.notifier](#optionsnotifier)
  * [notify.withReporter(Function)](#notifywithreporterfunction)
  * [notify.onError()](#notifyonerror)
  * [notify.logLevel(level)](#notifyloglevellevel)
* [Disable 'gulp-notify'](#disable-gulp-notify)
* [Examples](#examples)
  * [As jshint reporter](#as-jshint-reporter)
* [License](#license)

<!-- toc stop -->
...
```

#### <a name="apidoc.element.gulp-notify.withReporter"></a>[function <span class="apidocSignatureSpan">gulp-notify.</span>withReporter (reporter)](#apidoc.element.gulp-notify.withReporter)
- description and source-code
```javascript
withReporter = function (reporter) {
  if (!reporter) throw new gutil.PluginError("gulp-notify", "No custom reporter defined.");

  var inner = function (options) {
    options = setOptions(options, reporter);
    return notify(options);
  };

  inner.onError = function (options) {
    options = setOptions(options, reporter);
    return api.onError(options);
  };

  inner.logLevel = api.logLevel;
  inner.logger = api.logger;

  return inner;
}
```
- example usage
```shell
...
  * [notify(options)](#notifyoptions)
    * [options.onLast](#optionsonlast)
    * [options.emitError](#optionsemiterror)
    * [options.message](#optionsmessage)
    * [options.title](#optionstitle)
    * [options.templateOptions](#optionstemplateoptions)
    * [options.notifier](#optionsnotifier)
  * [notify.withReporter(Function)](#notifywithreporterfunction)
  * [notify.onError()](#notifyonerror)
  * [notify.logLevel(level)](#notifyloglevellevel)
* [Disable 'gulp-notify'](#disable-gulp-notify)
* [Examples](#examples)
  * [As jshint reporter](#as-jshint-reporter)
* [License](#license)
...
```



# <a name="apidoc.module.gulp-notify.extra_api"></a>[module gulp-notify.extra_api](#apidoc.module.gulp-notify.extra_api)

#### <a name="apidoc.element.gulp-notify.extra_api.logError"></a>[function <span class="apidocSignatureSpan">gulp-notify.extra_api.</span>logError (options, isError)](#apidoc.element.gulp-notify.extra_api.logError)
- description and source-code
```javascript
logError = function (options, isError) {
  if (!logLevel) return;
  if (logLevel === 1 && !isError) return;

  color = isError ? "red" : "green";
  if (!gutil.colors[color]) return;
  fnLog(gutil.colors.cyan('gulp-notify') + ':',
           '[' + gutil.colors.blue(options.title) + ']',
            gutil.colors[color].call(gutil.colors, options.message)
           );
}
```
- example usage
```shell
...

// Try/catch the only way to go to ensure catching all errors? Domains?
try {
  var options = constructOptions(options, message, templateOptions);
  if (!options) {
    return callback();
  }
  api.logError(options, (message instanceof Error));
  reporter(options, function (err) {
    if (err) return callback(new gutil.PluginError("gulp-notify", err));
    return callback();
  });
} catch (err) {
  return callback(new gutil.PluginError("gulp-notify", err));
}
...
```

#### <a name="apidoc.element.gulp-notify.extra_api.logLevel"></a>[function <span class="apidocSignatureSpan">gulp-notify.extra_api.</span>logLevel (newLogLevel)](#apidoc.element.gulp-notify.extra_api.logLevel)
- description and source-code
```javascript
logLevel = function (newLogLevel) {
  if (newLogLevel === void 0) return logLevel;
  logLevel = newLogLevel;
}
```
- example usage
```shell
...
    * [options.emitError](#optionsemiterror)
    * [options.message](#optionsmessage)
    * [options.title](#optionstitle)
    * [options.templateOptions](#optionstemplateoptions)
    * [options.notifier](#optionsnotifier)
  * [notify.withReporter(Function)](#notifywithreporterfunction)
  * [notify.onError()](#notifyonerror)
  * [notify.logLevel(level)](#notifyloglevellevel)
* [Disable 'gulp-notify'](#disable-gulp-notify)
* [Examples](#examples)
  * [As jshint reporter](#as-jshint-reporter)
* [License](#license)

<!-- toc stop -->
...
```

#### <a name="apidoc.element.gulp-notify.extra_api.logger"></a>[function <span class="apidocSignatureSpan">gulp-notify.extra_api.</span>logger (newLogger)](#apidoc.element.gulp-notify.extra_api.logger)
- description and source-code
```javascript
logger = function (newLogger) {
  if (!newLogger) return fnLog;
  fnLog = newLogger;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.gulp-notify.extra_api.onError"></a>[function <span class="apidocSignatureSpan">gulp-notify.extra_api.</span>onError (options, callback)](#apidoc.element.gulp-notify.extra_api.onError)
- description and source-code
```javascript
onError = function (options, callback) {
  var reporter;
  options = options || {};
  var templateOptions = options.templateOptions || {};
  var callback = callback || function (err) {
    err && logError({
      title: "Error running notifier",
      message: "Could not send message: " + err.message
    }, true);
  };

  if (options.notifier) {
    reporter = options.notifier;
  } else {
    if (options.host || options.appName || options.port) {
      notifier = new notifier.Notification({
        host: options.host || 'localhost',
        appName: options.appName || 'gulp-notify',
        port: options.port || '23053'
      });
    }
    reporter = notifier.notify.bind(notifier);
  }
  return function (error) {
    var self = this;
    report(reporter, error, options, templateOptions, function () {
      callback.apply(self, arguments);
      self.emit && self.emit('end');
    });
  };
}
```
- example usage
```shell
...
    * [options.onLast](#optionsonlast)
    * [options.emitError](#optionsemiterror)
    * [options.message](#optionsmessage)
    * [options.title](#optionstitle)
    * [options.templateOptions](#optionstemplateoptions)
    * [options.notifier](#optionsnotifier)
  * [notify.withReporter(Function)](#notifywithreporterfunction)
  * [notify.onError()](#notifyonerror)
  * [notify.logLevel(level)](#notifyloglevellevel)
* [Disable 'gulp-notify'](#disable-gulp-notify)
* [Examples](#examples)
  * [As jshint reporter](#as-jshint-reporter)
* [License](#license)

<!-- toc stop -->
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
