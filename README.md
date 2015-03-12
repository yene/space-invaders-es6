# Porting Space Invaders to ES6
Porting [Mary Rose Cook Space Invaders](http://annotated-code.maryrosecook.com/space-invaders/index.html) to ES6.

# Steps
## Install ES6 to ES5 converter
from https://babeljs.io/docs/using-babel/

```
npm install --global babel
```

## run the converter
```
cp space-invaders.js space-invaders-es6.js
babel space-invaders-es6.js > space-invaders.js
``` 

## migration
### 1. Reaplace functions that use outside cope with Arrows
With [Arrows](https://github.com/lukehoban/es6features#arrows) functions can use the same lexical scope as their surrounding code. `function()` becomes `() =>` and
`var self = this;` gets dropped.
### 2. Replace prototype with class
With [Classes](https://github.com/lukehoban/es6features#classes) the prototype code can be put into a class and the object code can be put inside the constructor.
## 3. Replace var with let
I replaced `for( var i..` with `for( let i..` to hide `i` in the function scope (outside the for loop). 

## not used features
In this short example not all features of ES6 could be showcased. Here a few that are very useful: [default parameter values](https://github.com/lukehoban/es6features#default--rest--spread), [Modules](https://github.com/lukehoban/es6features#modules), [Promises](https://github.com/lukehoban/es6features#promises)


# Live Demonstration
A nice use of Modules and Promises is demonstrated in this video: [Javascript in 2015](https://www.youtube.com/watch?v=iukBMY4apvI).

