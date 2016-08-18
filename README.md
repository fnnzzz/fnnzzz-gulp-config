# Gulp config for static projects #

My personal gulp config for a quick start of development.

### Under the hood: ###

* Livereload (browser-sync)
* SASS to CSS (with mapssource)
* Minify and concat JS
* JSHint for JS
* Bower
* Compress images (gif, png, jpg, svg)

all source files, with which you'll be working in a folder 'assets/src'

all outputed files will be stored in 'dist' folder*

### Project structure ###

* **assets/dev/images** - for images (gif, png, jpg, svg)
* **assets/dev/js** - for custom scripts (not libs like jquery and etc), these scripts will be minified and checked by JSHint.
* **assets/dev/js.concat** - all scripts, that need be combined into one js-file. In output it will file 'combined.js' in 'assets/dist/js' dir.
* **assets/dev/libs** - all libs (example: jquery, owlslider, hmtl-shiv). In in this folder there Bower, with which you can download libs. Output — 'assets/dist/libs'
* **assets/dev/sass** - for SASS-files.

### How it work? ###

1. Pull this repo.
2. Install gulp globally (npm i gulp -g).
3. Make "npm install" (all packages will be installed from "package.json" list)
4. Then run "gulp" command. All outputed files will be stored in "dist" dir.

ENJOY!


* * * * * * * * * * * * * * *

### How enable livereload? ###

* Open `gulpfile.js`
* End edit *browserSync.init({  proxy: "localhost" });* where write needed url.
* Then open this URL in browser with port written into the console (port 300x), for example: *http://localhost:3005/*
* That's all. Now livereload watchin on all changes in 'src' folder and refresh page if is needed! Enjoy!

* * * * * * * * * * * * * * *

### For production: 'gulp prod' (without watches).
### For cleaning `dist` folder: `gulp clean` (useful to do from time to time).
### Dirs `dist` and `node_modules` into `.gitignore`, so the project should be to rebuild on different machines
