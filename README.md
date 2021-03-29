
## Getting Started
Make sure these are installed first.

- [Node.js](http://nodejs.org)
- [Gulp Command Line Utility](http://gulpjs.com) `npm install --global gulp-cli`

*__Note:__ if you've previously installed Gulp globally, run `npm rm --global gulp` to remove it.*

### Quick Start

1. In bash/terminal/command line, `cd` into your project directory.
2. Run `npm install` to install required files and dependencies.
3. When it's done installing, run one of the task runners to get going:
	- `gulp` manually compiles files into `/public/` directory
	- `gulp watch` automatically compiles files and applies changes using [BrowserSync](https://browsersync.io/) when you make changes to your source files.

### How it works

Add your source files to the appropriate `src` subdirectories. Gulp will process and and compile them into `public`.

- JavaScript files in the `src/js` directory will be compiled to `public/js`. Files in subdirectories under the `js` folder will be concatenated.
- CSS files in the `src/sass` directory will be compiled to `public/css`.
- SVG files placed in the `src/svg` directory will be optimized with SVGO and compiled into `public/svg`.
- Files and folders placed in the `copy` directory will be copied as-is into the `public` directory.

*__Note:__ `devDependencies` are the dependencies Gulp uses. Don't change these or you'll break things.*

### Where to put and edit files
- The `package.json` file holds all of the details about your project. Some information is automatically pulled in from it and added to a header that's injected into the top of your JavaScript and CSS files.
- Put your JavaScript files in the `src/js` directory. Files placed directly in the `js` folder will compile directly to `public/js` as both minified and unminified files. Files placed in subdirectories under `src/js` will also be concatenated into a single file.
- Put your [Sass](https://sass-lang.com/) files in the `src/sass` directory. Gulp generates minified and unminified CSS files. It also includes [autoprefixer](https://github.com/postcss/autoprefixer), which adds vendor prefixes for you.
- Place SVG files in the `src/svg` directory.
- SVG files will be optimized with [SVGO](https://github.com/svg/svgo) and compiled into `public/svg`.
- Files and folders placed in the `src/copy` directory will be copied as-is into `public`. This is a great place to put HTML files, images, and pre-compiled assets.

### Features
- Concatenate, minify, and lint JavaScript.
- Compile, minify, autoprefix, and lint Sass.
- Optimize SVGs.
- Copy static files and folders into your `public` directory.
- Automatically add headers and project details to JS and CSS files.
- Create polyfilled and non-polyfilled versions of JS files.
- Watch for file changes, and automatically recompile build and reload webpages.
