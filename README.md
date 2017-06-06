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

## Themes
Looking to customize your colors? See the
[Panda Extended](https://marketplace.visualstudio.com/items?itemName=dhedgecock.panda-extended)
theme for examples of available scopeNames.

## Inline Templates
It is currently possible to define your component templates in the component files
using the `layout` property and the `htmlbars-inline-precompile` tool. Welcome to
single file component definitions!

## Emmet
Emmet will not work with this extension without configuration _(The handlebars
language id used by this extension does not activate the Emmet extension tab
completions)_.

The `"emmet.syntaxProfiles"` inside your preferences can be used to notify Emmet to
include `handlebars` in the list of respected syntaxes:

```javascript
// settings.json
{
  "emmet.syntaxProfiles": { "handlebars": "html" }
}
```

You can also configure Emmet to complete using single quotes:
```javascript
// settings.json
{
  "emmet.syntaxProfiles": {
    "handlebars": "html",
    "html": {
      "attr_quotes": "single"
    }
  }
}
```

_See the [Emmet syntaxProfiles](https://docs.emmet.io/customization/syntax-profiles/)
docs for `syntaxProfiles` details. See the
[HTML Language](https://code.visualstudio.com/docs/languages/html#_emmet-snippets)
docs for VSCode preferences details._

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
