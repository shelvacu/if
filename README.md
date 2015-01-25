# if
Conditional branching for Javascript

### Installation
```
npm install if
```

### Usage
When requiring `if`, you will have to capitalize your variable name. Javascript reserves the `if` keyword to stay backwards-compatible with the legacy implementation of `if`.
```js
var If = require('if');
```

If the condition is truthy, the handler function passed to `Then` will be called.
```js
If(condition).Then(handler);
```

A handler can be passed to the `Else` method, which will be called if the condition is not truthy.
```js
If(condition).Then(handler)
  .Else(handler);
```

To evaluate more conditions, call `If` after `Else`.
```js
If(condition).Then(handler)
  .Else().If(condition).Then(handler)
  .Else().If(condition).Then(handler);
```

### Example
```js
If(isRobot()).Then(function(){
    console.log('beep');
  }).Else().If(isHuman()).Then(function(){
    console.log('boop');
  }).Else(function(){
    console.log('?')
  });
```

### License
The MIT License (MIT)

Copyright (c) 2015 ᴍᴀᴛᴛ ʙᴇʟʟ

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
