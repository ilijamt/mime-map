Mime Map
========

A list of mime types

Generated from: http://www.freeformatter.com/mime-types-list.html

Using the following method:

```javascript
var mimeTypes = [];
$("#mime-types-list table tbody tr td:first-child").each(function(key, value) {
    if ( typeof mimeTypes[key] === "undefined" ) {
       mimeTypes[key] = {};
    }
    mimeTypes[key]['description'] = $(value).html();
});

$("#mime-types-list table tbody tr td:nth-child(2)").each(function(key, value) {
    if ( typeof mimeTypes[key] === "undefined" ) {
       mimeTypes[key] = {};
    }
    mimeTypes[key]['type'] = $(value).html();
});

$("#mime-types-list table tbody tr td:nth-child(3)").each(function(key, value) {
    if ( typeof mimeTypes[key] === "undefined" ) {
       mimeTypes[key] = {};
    }
    mimeTypes[key]['extension'] = $(value).html().replace(".", "");
});
```

