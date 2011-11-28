delicious2text
==============

Description
-----------

Super simple script to fetch some delicious links and output them in
text format.

Dependencies
------------

 - [request](https://github.com/mikeal/request) (`npm install request`)
 - [commander](https://github.com/visionmedia/commander.js) (`npm install commander`)

Usage
-----

    $ delicious2text --user username --tags tag1,tag2 --format "%d\n%u\n\n%n" --separator '\n---\n'
    
    Link one
    http://www.link1.com
    
    That site is awesome
    ---
    Link two
    http://www.link2.com
    
    That site is awesome too

Format
------

Delicious JSON API returns object like:
    
    {
        "a": "username",
        "d": "title",
        "n": "comment",
        "u": "http://url.com/",
        "t": ["tag one", "tag two"],
        "dt": "2011-11-25T14:17:41Z"
    }
    
Use %key to insert the corresponding value in the output.
