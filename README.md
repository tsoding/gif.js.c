# gif.js.c

**WARNING! The project is in active development. Nothing is finished. Anything can break at any moment without any notice.**

A fork and rewrite of [gif.js] library. The idea is to rewrite majority of the code of [gif.js] in C and compile it down to [WebAssembly] using [Clang without Emscripten](https://depth-first.com/articles/2019/10/16/compiling-c-to-webassembly-and-running-it-without-emscripten/).

This is needed for our secret project [emoteJAM](https://gist.github.com/rexim/c5c32fb92ef61d0292e543dfb7a064a5). I think GIF rendering process is a bit slow for what it's doing and I think we can speed it up by moving all of the number crunching to [WebAssembly].

## Why not just [Emscripten] the [giflib] library?

[Emscripten] adds unnecessary complexity to our simple project and [giflib] is doing way more than what we need. [gif.js] hits the sweetspot between the complexity and the functionality. It's perfect for [Our Project][emoteJAM]. I just want it to be faster.

## `<My Favorite Lang>` can also compile to WebAssembly. Why not just use `<My Favorite Lang>` instead of C?

For the same reason I don't wanna use [Emscripten]. I would even prefer to program this directly in [WAT], but unfortunately I don't have that much time.

[gif.js]: https://jnordberg.github.io/gif.js
[WebAssembly]: https://webassembly.org/
[Emscripten]: https://emscripten.org/
[giflib]: http://giflib.sourceforge.net/
[emoteJAM]: https://gist.github.com/rexim/c5c32fb92ef61d0292e543dfb7a064a5
[Rust]: https://www.rust-lang.org/
[WAT]: https://developer.mozilla.org/en-US/docs/WebAssembly/Understanding_the_text_format
