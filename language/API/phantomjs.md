# PhantomJS

## About

[PhantomJS](http://phantomjs.org/) - PhantomJS is a headless WebKit scriptable with a JavaScript API. It has fast and native support for various web standards: DOM handling, CSS selector, JSON, Canvas, and SVG.

## Installing PhantomJS

To install from package manager:
```
sudo apt-get install phantomjs
```

## Executing a PhantomJS File

To execute ```myscript.js``` having arguments ```args1, args2...```:
```
phantomjs myscript.js args1 args2 ...
```

## Opening a Page

To open a page, in ```myscript.js```, write:
```
var webpage = require('webpage');
var page = webpage.create();

page.open('myurl', function(status) {
  if(status === 'success'){
    // do foo
  }
  // do bar
  phantom.exit();
});
```

## Rendering a Page

To render a page at url ```myurl``` as ```output.png```:
```
page.open('myurl', function(status){
  if(status === 'success') {
    page.render('output.png');
  }
  phantom.exit();
});
```

## Setting Wait Time

To wait for ```time_in_milli``` time after a page loads:
```
var system = require('system');

setTimeout(function(){
  // do foo
}, time_in_milli);
```

## Evaluating an Element in Page

To evaluate an element inside the loaded page:
```
page.open('myurl', function(status){
  if(status === 'success'){
    var element = page.evaluate(function(err){
      if(err){
        return err;
      }
      return document.title;
    });
  }
  phantom.exit();
});
```

### jQuery

To use jquery to say, click a button:
```
page.includeJs("http://ajax.googleapis.com/ajax/libs/jquery/1.6.1/jquery.min.js", function() {
  page.evaluate(function() {
    $("button").click();
  });
  phantom.exit();
});
```

### querySelector

#### Query Element by Attribute

To query contents of an element of type ```div``` by ```class="myinputclass"```:
```
var result = document.querySelector('input[class="myinputclass"]').innerHTML;
```

#### Query Element by Attribute Prefix

To query element with attibute ```href``` and prefix pattern ```myprefix```:
```
var result = document.querySelector('[href^="myprefix"]');
```

## Obtaining Cookies

To obtain cookies stored in page with url ```myurl```:
```
page.open('myurl', function(status){
  if(status==='success') {
    var result = page.cookies;
    // do foo
  }  
  phantom.exit();
});
```

## Loading Cookies

To load cookies from file ```cookiefile.json```:
```
var fs = require('fs');
var cookies = JSON.parse(fs.read('cookiefile.json'));
phantom.addCookie(cookie);
```

## Page Handlers/Callbacks

### page.onLoadFinished

To run a function after page is loaded:
```
page.open('myurl');
page.onLoadFinished = function() {
  // do foo
}
```

### page.onConsoleMessage

To display messages from webpage console:
```
page.onConsoleMessage = function(msg) {
  console.log(msg);
}
```
