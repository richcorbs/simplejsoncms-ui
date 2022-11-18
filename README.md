# Welcome to Simple JSON CMS UI

In short, this is a single-page CMS using data stored on https://simplejsoncms.com.

## To use Simple JSON CMS UI

0. Create a data object at simplejsoncms.com and save it using a password.
1. Open the CMS web page. You can run the CMS page locally if you are the only one needing access. Or you can add the CMS page to any web site and then anyone who has the key and password can access and update the data.
2. Enter in the "key" from simplejsoncms. Because of the way it is built you can see any data from simplejsoncms for which you have the key. The key is stored in the browser's local storage. When you change the key the page will retrieve the data for that key if it exists.
3. Make changes to your data: lists, things, attributes.
4. Assuming you saved your simplejsoncms data with a password, you can use that password on this page to save updates to your data.
5. You can read your data via the simplejsoncms api URL. You could use that URL in your build/dev process to retrieve your data as you build your site.

The data structure is as follows:

- **Lists**. A list is a collection (array) of things (objects) that all have the same attributes. Nested objects are not supported. You might use lists for collections of pages or anything else you have more than one of.
- **Things**. A thing is an object with any number of attributes. You might use a thing for storing a single instance object like a configuration. There is only one level of attributes. Nested objects are not supported.
- **Attributes**. Attributes have a name and a value. In lists each thing has the same attributes. If you add an attribute to a list then the attribute is added to all of the things that are in the list. Likewise, if you delete an attribute from a list it is deleted from all the things in the list.

It is written in HTML, CSS, and javascript. It relies on UnoCSS from a CDN for real-time styling via Tailwind classes. The interactivity is implemented using AlpineJS from CDN. There is no build process. The CMS page should work in any modern browser.