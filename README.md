# jquery-dictate

jquery-dictate provides simple English dictation interface.

[http://hitsujiwool.github.com/jquery-dictate/](http://hitsujiwool.github.com/jquery-dictate/)

## Basic Usage

    $('#target').dictate('Sentence comes here');    
    $('#target').dictate('Sentence comes here', 'Second sentence comes here', '... There can be any numbers of sentences');
    
## Options
    
    $('#target').dictate('Sentence comes here', {
      exposed: ".?'" // characters not to be hidden
      caseInsentive: true // default is false
      accept: function() { // overwrite callback triggered when the input is accepted }
      reject: function() { // overwrite callback triggered when the input is rejected }
      complete: function() { // overwrite callback triggered when the all characters are exposed }
      afterAccept: function() { // triggered after accept callback }
      afterReject: function() { // triggered after reject callback }
      afterComplete: function() { // triggerd after complete callback }
    })
    
## API

    var api = $('#target').data('dictate');
    api.start(); // start dictation
    api.showNextChar(); // show next character by force
    api.showNextWord(); // show next word by force
    api.giveup(); // show all
    api.getStats(); // some information (see below)

## Stats

You can get some information via `api.getStats()`, which returns simple object.

* characters: number of characters
* accepted: number of accepted characters
* opened: number of characters shown by force
* errors: number of input errors
* giveup: whether `api.giveup()` was called or not

## License

(The MIT License)

Copyright (c) 2012 hitsujiwool &lt;utatanenohibi@gmail.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
