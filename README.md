jQuery Highlight 
----------------

Find some text in the DOM. The difference between this and [other](http://www.gotoquiz.com/web-coding/programming/javascript/highlight-words-in-text-with-jquery/) [Plugins](http://johannburkard.de/blog/programming/javascript/highlight-javascript-text-higlighting-jquery-plugin.html) is that it looks for Text in multiply nodes. It uses [DOMRanges](http://www.w3.org/TR/DOM-Level-2-Traversal-Range/ranges.html) and therefor it only works in Firefox/WebKit/Opera.

## Usage ##

You can find some examples [here](http://fweinb.github.com/jqueryhighlight/) 


### Basic usage: ###

```
$('body').highlight("Search Query");
```

This will search for the text "Search Query" in the whole document will only highlight the first hit. 


### Multiply Occurences ###

To highlight all occurrences of the text you have to pass an option object like this:

```
$('body').highlight("Search Query", {onlyFirst : false});
```

### The 'options' ###

The default options are:

```
{
            onlyFirst : true, 
            idPrefix : '_'
            className : 'jQuery_Highlight',
            callback : function(element){}
}
```

*onlyFirst* : true if only the first occurrence should be highlighted. 
*idPrefix* : the highlighted text will be wrapped in span tags with a id like idPrefix plus an up counting number starting at 1. 
*className* : the className of all highlighted text
*callback* : a callback for each highlighted text, to add Custome data and do some fancy stuff with highlighted text. 





