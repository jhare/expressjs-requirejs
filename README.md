expressjs-requirejs
===================

Example of using ExpressJS in conjunction with RequireJS to share your client-side code with the server side.


Create a basic Express application with the steps they describe in http://expressjs.com/guide.html#executable .

I executed the statements 
```
express --sessions -css less expressjs-requirejs &&
cd expressjs-requirejs &&
npm install
```


After doing so, your directory structure will look something like
```
expressjs-requirejs/
  |-- node_modules/
    |-- (lots of stuff here, not important to list)
  |-- public/
    |-- images/
    |-- javascripts/
    |-- stylesheets/
      |-- style.less (or style.styl for stylus)
  |-- routes/
    |-- index.js
  |-- views/
    |-- index.ejs
  |-- app.js
  |-- package.json
```


