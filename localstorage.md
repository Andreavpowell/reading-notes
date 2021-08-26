# Past, Present, and Future of local storage for web applicaitons

## Cookies

- included with every HTTP request
  - slows down your web application by needlessly transmitting the same data over and over
  - sends data unencrypted over the internet (unless your entire web app is served over SSL)
- limited to about 4KB of data which is enough to slow down your app, but not enough to be terribly useful

## Local Storage Hacks before HTML5

- during the First Great Browser Wars, Microsoft invented many things and included them in their browser-to-end-all-browser-wars (Internet Explorer)
  - DHTML behaviors
  - userData
- userData allows web pages to store up to 64KB of data per domain in a hierarchical XML-based structure
- Adobe introduced Flash cookies in 2002 - properly known as Local Shared Objects

## Introducing HTML5 Storage

- is a specification named Web Storage which was at one time part of the HTML5 specification proper, but split out into its own specification for political reasons
- a way for web pages to store named key/value pairs locally within the client web browser
- close your browser tab, exit, and it will still exist on the site

## Using HTML5 Storage

- based on key/value pairs
- store data based on a named key, then retrieve that data with the same key
- named key is a string
- data can be any type supported by js (strings, booleans, integers, or floats)
- if you are storing and retrieving anything otther than strings, you will need to use functions like `parseInt()` or `parseFloat()` to coerce your retrieved data into the expected js datatype
- `interface Storage { getter any getItem(in DOMstring key); setter creator void setItem(in DOMString key, in ant data); };`
- calling `setItem()` with a named key that already exists will silently overwrite the previous value
- calling `getItem()` with a non-existent key will return `null` rather than throw an exception
- treat the `localStorage` object as an associative array
- instead of using `getItem()` and `setItem()` methods, use square brackets
  - `var foo = localStorage.getItem("bar"); localStorage.setItem("bar", foo);`
  - `var foo = localStorage["bar"]; localStorage["bar"] = foo;`
- methods for removing the value for a given named key and clearing the entire storage area (deleting all the keys and values at once)
  - `interface Storage { deleter void removeItem(in DOMString key); void clear(); };`
- property to get the total number of values in the storage area and to iterate throough all of the keys by index (to get the name of each key)
  - `interface Storage { readonly attribute unsigned long length; getter DOMString key (in unsigned long index); };`

## Tracking Changes to the HTML5 Storage Area

- to keep track programmatically of when the storage area changes, you can trap the storage event
- the storage event is fired on the `window` object whenever `setItem()`, `removeItem()`, or `clear()` is called and actually changes something. 
  - ex. if you set an item to its existing value or call `clear()` when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area

## StorageEvent Object

- key - string - the named key that was added, removed, or modified
- `oldValue` - any - the previous value (now overwritten), or `null` if a new item was added
- `newValue` - any - the new value, or `null` if an item was removed
- url* - string - the page which called a method that triggered this change

[Home](reading-notes)
