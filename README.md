# AngularJS Seed

> Olive seed for AngularJS - offers you quickly scaffold an AngularJS project with pragmatic defaults and best practices.

## Usage

Install gulp, bower and olive if you haven't already:
```
npm install -g gulp bower olive
```
Create your project from this Angular seed using Olive CLI:
```
mkdir myapp && cd myapp
olive new angular
```
Install npm and bower dependencies:
```
npm install && bower install
```
Start developing:
```
npm start
```
Run test once and generate code coverage reports in `coverage` directory.
```
npm test
```
Build for production:
```
npm run build
```

## Directory Structure

```
├─src/
│ ├─app/
│ │ ├─components/
│ │ │ └─navbar/
│ │ │   ├─navbar.directive.js
│ │ │   ├─navbar.html
│ │ │   └─navbar.scss
│ │ ├─pods/
│ │ │ └─home/
│ │ │   ├─home.controller.js
│ │ │   ├─home.html
│ │ │   └─home.scss
│ │ ├─services/
│ │ │ └─github.service.js
│ │ ├─styles/
│ │ │ ├─_overrides.scss
│ │ │ ├─_type.scss
│ │ │ └─app.scss
│ │ └─app.js
│ ├─assets/
│ │ ├─img/
│ │ ├─fonts/
│ │ ├─apple-touch-icon.png
│ │ └─favicon.ico
│ └─index.html
├─dist/
├─.tmp/
├─bower_components/
├─node_modules/
├─.bowerrc
├─.editorconfig
├─.gitignore
├─.jshintrc
├─bower.json
├─gulpfile.js
├─package.json
└─readme.json
```

File/Directory    | Purpose
------------------|---------
src/              | Contains your Angular application code.
dist/             | Contains the distributable (that is, optimized and self-contained) output of your application. Deploy this to your server!
.tmp/             | Various temporary output of build steps, as well as the debug output of your application.
bower_components/ |	Bower dependencies.
node_modules      | Node modules required for development purpose.
.bowerrc          | Bower configuration.
.editorconfig     | EditorConfig file.
.oliverc          | Olive configuration.
.gitignore        | Git configuration for ignored files.
.jshintrc         | JSHint configuration
bower.json        | Bower configuration and dependency list.
gulpfile.js       | Contains build specification for Gulp.
karma.conf.js     | Karma configuration
package.json      | NPM configuration. Mainly used to list the dependencies needed for asset compilation.

## .oliverc

Default options:
```
{
  "paths": {
    "src": "src",
    "tmp": ".tmp",
    "dist": "dist"
  }
}
```
These default options can be overridden. You can also include additional options from the following:

#### Ports

For example:
```
{
  "ports": {
    "app": 3000,
    "bs": 3001,
    "karma": 3002
  }
}
```
- `app`: The app will be served via this port (i.e. http://localhost:3000)
- `bs`: BrowserSync UI control panel can be accessed via this port (i.e. http://localhost:3001)
- `karma`: Karma tests report page is served via this port (i.e. http://localhost:3002/debug.html)

#### Content Security Policy

For example:
```
{
  "content-security-policy": {
    "development": {
      "default-src": "'unsafe-inline' 'self' data: gap: https://ssl.gstatic.com 'unsafe-eval'",
      "style-src": "'self' 'unsafe-inline'",
      "media-src": "*",
      ...
      "other-directive": "other-source"
    },
    "production": {
      "default-src": "'self' data: gap: https://ssl.gstatic.com 'unsafe-eval'",
      "style-src": "'self' 'unsafe-inline'",
      "media-src": "*"
    },
    "other-env": {
      ...
    }
  }  
}
```
