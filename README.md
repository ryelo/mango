# Mango style library

Mango is a style library

## Features

  * Built with Pug-Sass.
  * Easy to deploy your production files
  * Performance optimization: minify and concatenate JavaScript, CSS, HTML and images
  * Live browser reloading with `BrowserSync`
  * Includes:
    * `Sass variables` with with popular color palettes from [Material Design Palette](https://www.materialpalette.com/) and [Flat UI Colors](https://flatuicolors.com/)

## Requirements

* [Node.js](https://nodejs.org)
* [npm](https://www.npmjs.com)
* [Gulp](http://gulpjs.com/)

## Getting Started

After [Node.js](https://nodejs.org/en/download/), [npm](https://docs.npmjs.com/getting-started/installing-node), [Gulp](https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md) and [Bower](https://bower.io/#install-bower)(optional) installation, you can create a new project based on `pug-sass-boilerplate-starter-kit` by doing the following:

### Install From Source

First, clone the project:

```bash
$ git clone
```

Initialize `npm` on `<my-project-name>` directory

```bash
$ cd <my-project-name>
$ npm init
```

Install `Gulp` locally

```bash
$ sudo npm install gulp --save-dev
```

Finally, install `Gulp` required dependencies

```bash
$ sudo npm install gulp-uglify browser-sync gulp-plumber gulp-autoprefixer gulp-sass gulp-pug gulp-imagemin gulp-cache gulp-clean-css gulp-sourcemaps gulp-concat beeper gulp-util gulp-rename gulp-notify --save-dev
```

### Running Your Local Server With Gulp

After the installation of all requirements and its dependencies, your local web development environment is ready to run. Setup your initial files with `gulp setup`. This command is only necessary the first time the project is set or if the build folder is deleted.

```bash
$ gulp setup
```

Now run your local server using the `watch` task

```bash
$ gulp watch
```

This task will open the browser window usually with the URL http://localhost:3000/. Any saved changes made to the project files, will reload automatically the browser.

## Project Structure

The structure presented in this boilerplate is grouped primarily by folder content and file type. Please note that this structure is only meant to serve as a guide, it is by no means prescriptive.

```
.
├── build/                      # Store processed/minified files - your project's deployable output
├── img/                        # Main folder for image files
├── js/                         # Main folder for JS files
│   ├── vendor/                 # Store third part library files (e.g.: jquery, bootstrap)
│   └── main.js                 # Index JS code goes here
├── styles/                     # Main folder for cascade style files
│   ├── modules/                # Store third party modules and initializers (e.g.: normalize, reset)
│   ├── variables/              # Store sass variables files
│   └── main.scss               # Index Sass goes here
├── templates/                  # Main folder for pug template files
├── .bowerrc                    # Change bower library destination path from its default
├── gulpfile.js                 # Setup Gulp tasks
└── index.pug                   # Index pug markup goes here
```

### The build/ Contents

```
.
├── build/
    ├── img/                    # Contains the compressed and optimized image files
    ├── css/                    # Contains the concatenated/minified .css files and .map files
    ├── js/                     # Contains the concatenated/minified/uglyfied .js files and .map files
    │   └── vendor/             # Store third party libraries
    └── index.html              # Minified html index file
```