Soundy
======

A very simply library using the Audio API (currently only available in Chrome)

An example baked into an Expressjs (nodejs) app can be found here: https://github.com/MRdNk/Soundy-Example

Include soundy
------------

Include soundy.js (my modular approach)
```html
<script type='text/javascript' src='/javascripts/modules/soundy/index.js'>
```

Define the options object to pass into Soundy
---------------------------------------------

```
Options (object)
- Sounds (array of 'sound' objects)
-- filename (name of the file)
-- name (your 'name' for the file)
- Path (the url path to your sounds folder)
```

```javascript

var options = {
  sounds: [
    {
        filename: 'YourSound1.wav',
        name: 'Sound1'
    }
  ],
  path: '/audio/' // Defaults to /audio/
}
```

Load your sounds & other options
--------------------------------

```javascript 
soundy.load(options, function (err, loaded) {
  if (err) {
    console.error(err)
  } else {
    console.log(loaded) // All the sounds have loaded, you're good to go
  }
})
```

Play a sound
------------

To play a sound, you pass the name into the play function, also provided as a sounds object.

NB. This needs to be done, after the ```soundy.load``` call back

Method 1: The object (available via the JavaScript console)
```javascript
soundy.play(soundy.sounds.Sound1)
```

Method 2: Pass a string name
```javascript
soundy.play('Sound1')
```

Get the Soundy Version No.
--------------------

You can get the soundy version no., by calling it in your code, or via a JavaScript console with

```javascript
soundy.version
```


```
The MIT License (MIT)
Copyright (c) 2013 MRdNk

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

