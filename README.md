# Language Server Plugin for CodeMirror 6

[![npm version](https://badge.fury.io/js/codemirror-languageserver.svg)](https://www.npmjs.com/package/codemirror-languageserver)

This plugin enables code completion, hover tooltips, and linter functionality by connecting a CodeMirror 6 editor with a language server over WebSocket.

[How It Works](https://hjr265.me/blog/codemirror-lsp/)

## Usage

``` js
import { languageServer } from 'codemirror-languageserver';

var ls = languageServer({
	serverUri: serverUri
	rootUri: 'file:///'
	documentUri: `file:///${filename}`
	languageId: 'cpp' // As defined at https://microsoft.github.io/language-server-protocol/specification#textDocumentItem.
});

var view = new EditorView({
	state: EditorState.create({
		extensions: [
			// ...
			ls(),
			// ...
		]
	})
});
```

## Contributing

Contributions are welcome.

## License

The library is available under the BSD (3-Clause) License.
