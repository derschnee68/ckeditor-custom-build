# How to Build

## Plugins

Add the following plugins when using https://ckeditor.com/ckeditor-5/online-builder/.
Start with the selection "Classic". Make sure that the following plugins are activated:
- Block quote
- Bold
- Code
- Code block
- Heading
- Horizontal line
- Italic
- Link
- List
- Remove format
- Strikethrough
- Subscript
- Superscript
- Table
- Underline

Then pick the items so they are included in the toolbar:
- Heading
- Bold
- Italic
- Link
- Bulleted List
- Numbered List
- Block Quote
- Insert Table
- Undo
- Redo  
- Code
- Code Block
- Horizontal Line

Remove other items not contained in this list.
	
`src/ckeditor.js` `Editor.builtinPlugins` should now look like:	
- Autoformat,
- BlockQuote,
- Bold,
- CKFinder,
- CKFinderUploadAdapter,
- Code,
- CodeBlock,
- Essentials,
- Heading,
- HorizontalLine,
- Image,
- ImageCaption,
- ImageStyle,
- ImageToolbar,
- ImageUpload,
- Indent,
- Italic,
- Link,
- List,
- MediaEmbed,
- Paragraph,
- PasteFromOffice,
- RemoveFormat,
- Strikethrough,
- Subscript,
- Superscript,
- Table,
- TableToolbar,
- TextTransformation,
- Underline
	
## Package.json
    
Remove the following line:
```json
private: true
```

Add the following lines to `package.json`:
```json
"files": [
"build"
],
"main": "build/ckeditor.js",
```  

## Publish

To publish just commit your changes to GitHub.

Integrate the build in your application's `package.json`'s dependencies like this:
`"ckeditor5-custom-build": "github:dasch-swiss/ckeditor_custom_build"`
