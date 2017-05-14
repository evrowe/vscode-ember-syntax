# VSCode Ember Syntax
Syntax highlighting for Ember template files AND syntax highlighting for inline
template definitions with tagged templates! The package currently includes patterns
matching htmlbars syntax only, but patterns for the new Glimmer components are on
the way.

## Usage
Grammars exported:
- Glimmer
- JavaScript (Extended)
- TypeScript (Extended)

![Screenshot](https://raw.githubusercontent.com/healthsparq/vscode-ember-syntax/master/Example.png)

## Inline Templates
It is currently possible to define your component templates in the component files
using the `layout` property and the `htmlbars-inline-precompile` tool. Welcome to
single file component definitions!

## Contributing
Contributions are welcome! Notes below are intended to help contributers become
familiar with the repo.

**Grammar Sources**: Grammar files are built in the
[glimmer-syntax-patterns](https://github.com/healthsparq/glimmer-syntax-patterns)
repository, any updates or issues with the grammar patterns should be submitted
there. All VSCode specific configurations are handled in this repository.

**Embedded Language**: VSCode must be notified when a language is embedded into
another language. This is done in the `package.json` grammars configs. This is how
the editor knows to insert Handlebars scoped comments and snippets inside tagged
templates in JS files.

## Resources
- https://marketplace.visualstudio.com/items?itemName=ms-vscode.typescript-javascript-grammar
- https://code.visualstudio.com/docs/extensions/themes-snippets-colorizers
- https://github.com/sheetalkamat/TypeScript-TmLanguage-VsCode
