# grunt-tomcat-deploy-with-https

This is a [grunt](https://github.com/gruntjs/grunt) task for code deployment over the Tomcat Admin Web Application.



## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-tomcat-deploy-with-https --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-tomcat-deploy-with-https');
```

## The "tomcat_deploy" task

### Overview
In your project's Gruntfile, add a section named `tomcat_deploy` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  tomcat_deploy: {
    host: 'localhost',
    login: 'xxxxx',
    password: 'yyyyy',
    path: '/myapp',
    port: 443,
    dist: 'dist',
    deploy: '/manager/text/deploy',
    undeploy: '/manager/text/undeploy',
  },
})
```
### Options
Additional options are available for deploy tasks.

If a war file is already created by your build process you can use that file istead of having this task archive the project.
```js
grunt.initConfig({
  tomcat_deploy: {
    ...
    war: 'app.war',
    ...
  },
})
```

### Other tasks
The task "tomcat_redeploy" will check if the app is deployed and removes it. It will then deploy a new version of the app.


## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
_(Nothing yet)_
