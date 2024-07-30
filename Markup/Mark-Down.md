
## General
* __Markdown__: a lightweight markup language.
	- One of the world's most popular markup languages.
	- Used to add formatting elements to plaintext documents.
	- Created by John Gruber in 2004.
* __Markdown Application__: capable of processing the Markdown file 
* __Markdown Processor__ (parser): take the Markdown-formatted text and output it to HTML format.
## How Does it Work?
*![[markdown-flowchart.avif]]
1. Create a Markdown file using a text editor or a dedicated Markdown application. The file should have an `.md` or `.markdown` extension.
2. Open the Markdown file in a Markdown application.
3. Use the Markdown application to convert the Markdown file to an HTML document.
4. View the HTML file in a web browser or use the Markdown application to convert it to another file format, like PDF.





## Basic Syntax (To make a cheatsheet)
* Header
	* alternative === ----
* paragraph
* line break (2 space then enter) same paragraph
* bold & italic
* blockquote >
	* Blockquotes with Multiple Paragraphs add > on blank
	* Nested >>
	* Blockquotes with Other Elements 
* list
	* ordered: any num but start with 1
		* indent: four spaces or one tab.
	* unordered: -, *, +
		* indent
	* Adding Elements in Lists
		* others: indent 4 spaces / 1 tab
		* code blocks: indent 8 spaces / 2tabs
* code: tick marks
	* escaping: enclose by double tick marks
* codeblock: indent 4 spaces / 1 tab
	* fenced code block: for no indenting
* horizontal rule: ***, ---, ___
* links: [text](url)
	* add titles (as tooltip when hovered) enclose with parenthesis
	* urls & emails to link: enclose with angle brackets
	* formatting (emphasize): add * * 
	* Reference-style Links: like normal links but square bracket instead parenthesis
		* first part: [hobbit-hole][1]
		* second part: [1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"
* images: ![alt text] (link to image "title")
* Escaping characters: \\
## Extended Syntax
* table
* fence code block: \`\`\`, ~~~
	* syntax highlight: add file type after \`\`\` ~~~ (\`\`\`json)
* footnotes
* heading IDs: ### My Great Heading {#custom-id}
	* styling with css
	* linking to heading ID: \[text](#heading-id)
		* Other websites can link to the heading by adding the custom heading ID to the full URL of the webpage (e.g, \[heading IDs](protocol:domain/path#heading-id))
* definition list
	* First Term  
	  : definition of first term here
* strikethrough: \~~word~~ 
* task list: - [ ]
* Automatic URL Linking
	* Disabling Automatic URL Linking \` prevent automatic url\` 
