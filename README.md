expressjs-requirejs
===================

Example of using ExpressJS in conjunction with RequireJS to share your client-side code with the server side.

### Steps ###


#### Creating the skeleton application ####
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

#### Acquire Require.js ####

If you don't have a copy handy, go to http://requirejs.org

Also, check out its starting guide if you're not familiar with it yet, found at http://requirejs.org/docs/start.html .

Place `require.js` into the `./public/javascripts` directory. 
```
expressjs-requirejs/
  |-- node_modules/
    |-- (lots of stuff here, not important to list)
  |-- public/
    |-- images/
    |-- javascripts/
      |-- require.js
    |-- stylesheets/
      |-- style.less (or style.styl for stylus)
  |-- routes/
    |-- index.js
  |-- views/
    |-- index.ejs
  |-- app.js
  |-- package.json
```


#### Setting up RequireJS ####

#### Definiing a Module ####

#### Normal Case: Using Client-side Modules Client-side ####

#### New Case: Using Client-side Modules Server-siode ####



