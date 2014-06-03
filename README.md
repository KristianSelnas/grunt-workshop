Kantega Grunt workshop - Del 1
==============

Installasjon
------------
Installer Grunt-runtime globalt:
> npm install -g grunt-cli

Opprett `package.json`:
> npm init

Legg til grunt-plugin i prosjektet
> npm install grunt –save-dev

Gruntfile
---------

Opprett `Gruntfile.js`
> touch Gruntfile.js

Åpne filen og legg inn
> module.exports = function(grunt) {
>  
>   grunt.initConfig({
>  
>   });
> };

Uglify
------
Legg til Uglify-plugin:
> npm install grunt-contrib-uglify –-save-dev

Last uglify-task (Gruntfile.js)
> module.exports = function(grunt) {
  
>   grunt.initConfig({
  
>   });
>   grunt.loadNpmTasks("grunt-contrib-uglify");
> };

Konfigurer uglify-tasken:
> module.exports = function(grunt) {
> 
>   grunt.initConfig({
>   	 uglify:  {
>   	 	minify: {
>   	 		files: {
>   				'dist/out.js': ['src/*.js']
>   			}
>   		} 
>   	 } 
>   });
>   grunt.loadNpmTasks("grunt-contrib-uglify");
> };

Kjør Grunt
> grunt uglify
