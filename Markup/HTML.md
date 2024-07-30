---
cssclasses:
  - html
---
---
![[Untitled (2).png]]

## Opening
+ drag n drop html file from text editor to browser's address bar
+ right click html file and open up with chosen browser
+ with terminal, type `google-chrome index.html`
## General
- __Hypertext Markup Language__
	- defines _structure_ & _content_ of webpages
	- semantic purpose
	- case insensitive
	- white spaces are ignored 
		- only 1 recognize
	- index.html
	- __Links/hypertext__
		- key feature
		- why called web & hypertext
	- `<html>`
		- represents the root (top-level element) of an HTML document
		- all other elements must be descendants of this element.
- __XHTML__
	- more strict than HTML
	- requires that all tags must be closed
	- case sensitive (must be lowercase)
- __Web Pages__
	- just plain text
	- can view & edit in any text editor.
- __HTML Validator__
	- Ensures markup is correct
- __HTML Encoding__
	- In the header
	+ tells browser what char set to use
		-  ensure text is displayed correctly
+ __HTML Entities__
	+ display reserved html characters 
	+ or characters that don't appear in keyboard
	+ `&gt;` `>` | `&lt;`  `<`
+ __Character Encoding__
	+ determines how chars are represented as bytes
	+ ensure text appears correctly in different platforms
	+ `UTF-8`: represents all in Unicode
	+ `ASCII`: simpler
+ __Replaced elements__
	+ an element whose content is 
		+ not directly represented in the html but instead replaced by external content
		+ outside the scope of the CSS formatting model
		+ `audio`, `canvas`, `embed`, `iframe`, `img`, `input`, `object`,  `video`
	+ __inline-replaced elements__
		+ behave like inline elements
		+ `img`, `input`
	+ __block-replaced elements__
		+ behave like block elements
		+ `<video>`, `iframe`
	+ __Anonymous replaced elements__
		+ objs inserted via css `content` property`
		+ they don't exist in the html markup
	+ CSS properties that apply only to replaced elements
		+ `object-fit`
		+ `object-position`
+ __Non-replaced elements__
	+ element whose content is directly represented in the html
	+ contain and display their content directly within the HTML
+ __Void elements__ 
	+ only have a start tag
	+ cannot have any child nodes.
## Anatomy
+ __Content__: inside tags
- __Elements__: unit of content
	- object in page
	- complete constructs that include the tags, content, and attributes
	- __Nested Elements__
		- __Hierarchy__: child/parent elems relationship
		- child elems can inherit parent elems' _styling_ & _behavior_
- __Tags__: provide instructions about page
    - enclosed in _angle brackets: `< >`_
    - case insensitive
    - specific part of an HTML element
    - tags are not elements
	    - meant to delimit the start and end of elements
    - usually travel in pairs
	    - __opening tag__
	    - __closing tag__
	    - __self-closing tags__: only have start tag
		    - _void elements, singleton tags, empty tag,
		      empty element, non-container tags_, _stand-alone elements_,
		      _unpaired elements_
		    + `/` understood as not needed
		    + void element
			    + meaning that it has no content and does not have a closing tag
* __Attributes__: gives add info to element
	* qualities that describe that element
	* __name__
	* __value__
	* __Boolean Attribute__: present means true/false
		* never takes a value
## Boilerplate 
+  __HTML Boilerplate__  _(basic template)_
	+ `<!DOCTYPE html>` doctype declaration
		+ tells browsers what html version to use to render document
	+ `<html lang=’en-US’> </html>` language attribute
		+ specifies the language of the content
	+ `<head>` head element
		+ info about page
		+ not displayed
		+ to render page correctly
		+ contains __metadata__
			+ data that describes data
			+ contains information about the page
	- `<body>` body element
		+ content
+ **Head Contents**
	+ **Open Graph Data**: made by meta
		+ the link appears with img/desc
		+ appears when linked in fb
		+ `og:image` `og:description` `og:title`
	- `<title>`
		+ title of overall html
		+ bookmark suggested name
	+ `<meta>`
		+ represents metadata that cannot be represented by other html meta related elements (title, link)
		+ Types
			+ __Name__: provides metadata that applies to the entire document.
				+ __name attribute__: what type of meta element it is; what info it contains
				+ __content attribute__: actual meta content
				+ sample: _author, description, keywords (used in search engine)_
			+ __http-equiv__: acts like an HTTP header and can be used to define certain behaviors of the web page
				+ `<meta http-equiv="refresh" content="30">`
			+ __charset__: specifies the character encoding for the HTML document.
				+ ensures that the document is rendered correctly
			+ __itemprop__: provide custom metadata about a specific element
				+ used in conjunction with the `itemscope` and `itemtype`
				+ helps SEO understand the content.
				+ `microdata`
	- `<script>`
		+ instructs browser to fetch and execute the JS code found in `src`
		+ `defer`: instruct browser to load js after html is finished parsing
	-  `<link>`
		+ used for specifying relationships between the current document and external resources
		+ JS not allowed
		+ `rel` = (no default behavior)
			+ `preload`: load a resource asap as it is needed for current page
			+ `prefetch`: load a resource for a future nav
			+ `stylesheet`: load and apply immediately to style page
			+ `icon`: use first/most supported favicon it encounters
			+ `dns-prefetch`: browser resolves the DNS in advance to speed future connections
				+ used for external resources
				+ resource: script, stylesheet, font
			+ `preconnect`: establishes early connection to servers
				+ reduce latency for future request
+ __`src` vs `href`__
	+ **src** (obtaining): _fetches_ and _embeds_ resources directly into the document
		+ browser expects to load and display/execute the resource.
		+ Examples: JS, imgs, vids, audios.
	+ **href** (pointing): _points_ to the location of external resources
		+ browser will navigate to or process the resource as a reference
		+ Examples: Stylesheets, icons, alter docu ver
	
## [Accessibility & Aria](A11y%20&%20Aria.md)
## [Forms](Forms)

## Semantic HTML
+ using appropriate tags that describes the meaning and structure of content
+ HTML should be coded to represent the _data_ that will be populated
	+ and not based on its default presentation styling
	+ roughly 100 semantic [elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) available
+ __Semantics__: In programming, Semantics refers to the _meaning_ of a piece of code
	+ what effect does running that line of JavaScript have?
	+ what purpose or role does that HTML element have
+ __Semantic Tags__:
	+  tags provide meaningful information about the content
+ __non-Semantic tags__: 
	+ tags do not convey any meaning about the content they enclose
+ Benefits
	+ Leads to better accessibility, SEO
	+ SEO: content as keywords, influence page ranking
+ __Landmark elements__
	+ Improve _accessibility_ by defining regions of a page with specific roles (e.g., `<header>`, `<nav>`, `<main>`, `<aside>`, `<footer>`)
	+ mainly for _accessibility technology_
+ __Content Sectioning elements__: 
	+ Organize the content into _hierarchical sections_ and _outline the document's structure_
	+ **`header`** introductory content
	- **`nav`** navigation
	- **`main`** dominant content
	- **`footer`** nearest ancestor
	- **`section`** generic section requires heading
	- **`article`** independently distributable reusable
	- **`aside`** indirectly related
	- **`address`**
	- **`hgroup`** secondary content
	- **`search`** contain form controls for search/filter operation
## Others
+ _`&nbsp`_ (non-breaking space) for empty cells
+ If `<title>` not included, title would default to file name
+ `<head>` _general rule_
	+ meta tags:  browsers apply the last occurrence of duplicate meta tags.
	+ favicon: browsers use the first supported `<link rel="icon">` they encounter
	+ stylesheets: browsers apply all stylesheet links in the order they appear
	+ links: All `<link>` tags are processed
+ `::before` `::after` doesn't work on _replaced elements_ like `imgs`
+ default size for `iframe` `object` is _300x150px_
+ when `img` is rendered its replaced element
	+ when `alt` is shown its void element
+ `inputs` with `image` type attributes are replaced elements similar to `img`.
+ Each browser has its own default styles for form controls. 
	+ Text-based form controls - Easy to Style
+ Form
	+ input with no name is ignored
	+ `min` `max` are inclusive
	+ `appearance`: none
	+ selection: if not checked, nothing is sent, not even name
		+ if checked but no value, name="on" is sent
	+ when label is clicked, it will focus to the associated element
	+ can associate multiple label but not good idea with assistive tech
+ A11y & ARIA
	+ In cases where HTML5 elements don’t have accessibility support, add both the HTML5 element and the ARIA role in order to cover those gaps in support
	+ landmark elements have built-in implicit ARIA roles, no need to duplicate them
	+ add `tabindex="0"` for elements that don't normally receive keyboard focus (div, span etc) to add it to the logical tab order 
	+ Adding `role="button"` to a link, expecting it to work as a button
		+ how Assistive Tech handles `a` and `button`
			+ a: activated by enter/return
			+ button: activated by spacebar
		+ if use link with role=button, the AT detects it as button but the user can become confused when they try to press spacebar with no result
	+ don't add scripting in links, that's for buttons
	+ don't forget href for links
	+ add `inert` to the `<main>` landmark to trap focus to modal
## Best Practice
- HTML convey semantics
	- Styling is for CSS.
* have consistent capitalization: lower case
- avoid spaces
	- use hypen
* `<strong>` and `<em>` over `<b>` and `<i>` tags
	* they lack semantic meaning
- keep `<h1>` one per page
- span & div for purely visual need
- semantics
	- semantics in js: appropriate function name
	- semantics in css: use of class name over nested element selectors
	- semantics in html: code based on data that will be populated over style
- Presentation (how it should look), is the sole responsibility of CSS.

### Tools
- https://www.html5accessibility.com/
- https://devdocs.io/html-elements/