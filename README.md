expressjs-requirejs
===================

# Note: Work in progress, motherfuckers.#

Example of using ExpressJS in conjunction with RequireJS to share your client-side code with the server side.



### Steps ###

#### Install Express ####

```
npm install -g express
```

#### Creating the Skeleton Application ####
Create a basic Express application with the steps they describe in http://expressjs.com/guide.html#executable .

For this tutorial I ran 
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

Also, check out its starting guide if you're not familiar with it yet, found
at http://requirejs.org/docs/start.html .

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

#### Adding jQuery et. al. ####
For this example I'll be linking in jQuery and Bootstrap, since it's such a 
common combination.

#### Setting up RequireJS ####

In `./public/javascripts` create a file `main.js`. This is the entry point for
require.js on the **client-side** (we haven't changed anything server-side).

Its contents

#### A Few Good Modules ####

Create a file in `./public/javascripts/
```
define(['jquery', 'bootstrap'], function($, Bootstrap) {

    

});

#### Normal Case: Using Client-side Modules Client-side ####

#### New Case: Using Client-side Modules Server-side ####

Here's the fun part, where start getting all share-ey.

**Up to this point we haven't don't anything out of the ordinary as far as
using require.js goes.**

We're going to do two things
* Convert `app.js` to use require.js for looking up modules before using the
NodeJS `require()`
* Include a client-side module on the server side and do something with it.

#### Current Issues & Different Strategies ####

Depending on who you talk to, some people like to concatentate whatever version
of jQuery they're using with require.js to make sure it's always available. I
can see the benefit of this, but in this example I stick to keeping it
separate. It's up to your personal preference in the end and what you want to
support in your build process.

