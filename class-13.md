# The past, present, and future of local storage for web applications. 
  * Cookies were invented early in th web's history to help with local storage, but they have the following downsides;
    1. Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over.
    1. Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)
    1. Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful
* Didn't realize I missed a war, but somehow I missed the great storage wars.  Microsoft invented and implemented DHTML behaviors and one of them was called userData. 
* userData allows web pages to store up to 64 kb of data per domain, in a heirarchical XML structure.  
* Along came Adobe and introduced a feature in Flash 6, and created a feature known as Local Shared Objects.  It allows Falsh objects to store up to 100 kb of data per domain. 
* Then google launched gears in 2007, an open source plugin browser aimed at providing additional capabilities in browsers.  

## HTML 5 storage
* a specification named Web Storage, which at one point of the HTML 5 specifiaction property, but was split out inot its own specification for political reasons.  But, its a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you.Unlike cookies, this data is never transmitted to the remote web server.
* the following browsers support HTML 5 ; IE (8.0+) Firefox (3.5+) Safari (4.0+) Chrome (4.0+) Opera (10.5+) Iphone (2.0+) Android (2.0+) 
* You can check the HTML server through javascript (of course you can, why wouldn't you be able to)
* HTML5 storage is based on named key/value pairs.  You store data based on a named key, then you can retrieve that data with the same key. The name key is a string.  The data can be any type supported by javascript, including strings, booleans, integers, or floats.  However the data is actually stored on a string.  
* Calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception.
* Like other JavaScript objects, you can treat the localStorage object as an associative array. Instead of using the getItem() and setItem() methods, you can simply use square brackets.

## Tracking changes to HTML5 storage area
* If you decide you want to keep track programmatically of when the storage area changes, you can trap the storage event.  The storage event is fired on the window object whenever setItem(), removeItem(), or clear(), is called and actually changes something.  
* The storage event is supported everywhere the localStorage object is supported. 

* StrorageEvent Object
1. key - string - the named key that was added, removed, or modified
1. oldValue - any - the previous value (now overwritten), or null if a new item was added
1. newValue - any - the new value, or null if an item was removed
1. url - string - the page which called a method that triggered this change

## Limitations in current browsers 
1. 5 megabytes is how much storage space each origin gets by default. 
1. You will get an error of "QUOTA_EXCEEDED_ERR" if you go over your limit. 