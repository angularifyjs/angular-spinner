angular-spinner [![Build Status](https://travis-ci.org/angularifyjs/angular-spinner.svg?branch=master)](https://travis-ci.org/angularifyjs/angular-spinner) [![Coverage Status](https://img.shields.io/coveralls/angularifyjs/angular-spinner.svg)](https://coveralls.io/r/angularifyjs/angular-spinner?branch=master)
===============

Spinner directive based on $http interceptor


Usage
---------

## Installing

Download the [Production version](https://raw.githubusercontent.com/angularifyjs/bower-angular-spinner/master/spinner.min.js) or the [Development version](https://raw.githubusercontent.com/angularifyjs/bower-angular-spinner/master/spinner.js).

Or download it with bower: open terminal and run

```
bower install angular-spinner
```

Include js files into your web page:

```html
<script type="text/javascript" src="[...]/angular-spinner[.min].js"></script>
```

Add dependency to your app module:

```javascript
angular.module('your-app-name', [
  'angular-spinner'
]);
```

The `spinner` module is now installed. It exposes the `SpinnerConfig` factory and `spinner` directive into your app.


## Using

#### Directive

``html
<div spinner="">
  <img src="./images/wait_icon.gif" />
</div>
```

```javascript
angular.module('app', [
  'angular-spinner'
]);
```

#### Event listener

```javascript
angular.module('app', [
  'angular-spinner'

]).run(function(){
  $scope.$on(SpinnerConfig['_START_REQUEST_'], function() {
    // To-do
  });
  $scope.$on(SpinnerConfig['_END_REQUEST_'], function() {
    // To-do
  });

});
```

#### SpinnerConfig

##### SpinnerConfig.isSpinning

Type: boolean

Check spinning or not

##### SpinnerConfig.pendingRequests

Type: integer

Number of pending requests


Documentation
-------------
See [Getting started](https://github.com/angularifyjs/angular-spinner/wiki/Getting-started)


Release History
-------------
See [CHANGELOG.md](https://github.com/angularifyjs/angular-spinner/blob/master/CHANGELOG.md)


Contributing
-------------
See [CONTRIBUTING.md](https://github.com/angularifyjs/angular-spinner/blob/master/CONTRIBUTING.md)


License
-------------
MIT - Copyright (c) 2014 Angularfiy.org & HenryTao.



