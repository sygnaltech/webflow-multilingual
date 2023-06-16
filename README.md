# webflow-multilingual
A simple multilingual support library for WebFlow

This library is based on the ideas and work of *@angro*, *@donaldev*, and *@memetican* in this WebFlow [forum post](https://forum.webflow.com/t/tutorial-full-multi-language-site-easy-to-set-up-and-to-use/67398).


## Capabilities

This library is designed to provide simple switchable language support that is compatible with the Webflow hosting design, designer canvas, and editor tools.

It provides...

1. An easy way to specify and edit short language-specific strings for labels, headings, and instructional text. 
2. Easy support for switching out rich-text objects
3. Support for swapping other localized elements such as image and video elements 
4. Auto-detection for a user's language preferences 
5. Easy ability to create custom-style language-selector buttons 
6. Ability to override any langua
7. Ability to remember the language setting across browser sessions ( if local storage is supported ) 


## Known Limitations

There are three primary known limitations-

+ Support for SUBMIT button text
+ Support for INPUT placeholder text
+ Support for UC Browser (Chinese)

See **Issues** for further details. 

## How to Use

First add a reference to this library to your site-wide custom Footer code. 
You can do this using a CDN reference through jsDelivr;

~~~~
<script src="https://cdn.jsdelivr.net/gh/sygnaltech/webflow-multilingual@0.2.0/dist/webflow-multilingual.min.js"></script>
~~~~

Decide on the languages you want to support, and find their 2-letter ISO codes.

[ISO 639-1 Language Codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)

We'll use `en` (for English) and `zh` (for Chinese) in our examples.

In any text string you want to make multilingual, codify it as follows;

`[[en]]Some Title[[zh]]CHINESE TEXT`

Strings will be tokenized by the language labels, and displayed only when the specified language is selected.

For RichText elements and images, add a custom attribute indicating the language that element represents. When this is specified, it will only show the element when the language matches the currently specified language;

**attribute**: `autolang`  
**value**: `en`

To create custom buttons, create a the element you want and add a custom attribute, e.g.

**attribute**: `whenClick`  
**value**: `setLang('en');`


## Further Notes

None at present.



