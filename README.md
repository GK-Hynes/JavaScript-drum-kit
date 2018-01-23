# [JavaScript Drum Kit](https://gk-hynes.github.io/javascript-drum-kit/)

A drum kit built using vanilla JavaScript. Built for Wes Bos' [JavaScript 30](https://javascript30.com/) course.

[![JavaScript drum kit screenshot](https://res.cloudinary.com/gerhynes/image/upload/v1516744698/Screenshot-2018-1-23_JS_Drum_Kit_ta1tii.png)](https://gk-hynes.github.io/javascript-drum-kit/)

## Notes

Each key has a unique keycode.

Data attributes let you add new non-standard attributes, such as `data-key`.

Add an event listener to the keys to listen for keydown.

Use `audio[data-key="${e.keyCode}"]` and `audio.play()` to play each key's specific audio.

If you call `.play()` on an element that is already playing, it won't play again. So use `audio.currentTime = 0` to rewind it to the start.

When a key is clicked on a `playing` class is added using `key.classList.add('playing')`. This scales up the key and adds a border and box shadow.

Instead of using `SetTimeout()` to remove the class, use a transitionend event. You cannot listen on all the elements in a NodeList so use `forEach()` to add an eventListener to each of them.

Instead of attaching a function directly to the key, use a separate function `playSound()` which you call upon keydown.
