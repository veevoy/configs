# Biome config

`formatter` - global formatting rules across all file types

`linter/rules/nursery/useSortedClasses` - for Tailwind CSS class sorting

`javascript` - specific rules for js, jsx, ts, tsx

inside a monorepo or a project create a folder `.vscode` at the root and inside that a `settings.json` file with the contents:

```json
{
	"prettier.enable": false,
	"editor.formatOnSave": true,
	"editor.codeActionsOnSave": {
		"source.organizeImports": "never",
		"source.fixAll.biome": "explicit",
		"source.organizeImports.biome": "explicit"
	},
	"eslint.rules.customizations": [
		{
			"rule": "style/*",
			"severity": "off",
			"fixable": true
		},
		{
			"rule": "format/*",
			"severity": "off",
			"fixable": true
		},
		{
			"rule": "*-indent",
			"severity": "off",
			"fixable": true
		},
		{
			"rule": "*-spacing",
			"severity": "off",
			"fixable": true
		},
		{
			"rule": "*-spaces",
			"severity": "off",
			"fixable": true
		},
		{
			"rule": "*-order",
			"severity": "off",
			"fixable": true
		},
		{
			"rule": "*-dangle",
			"severity": "off",
			"fixable": true
		},
		{
			"rule": "*-newline",
			"severity": "off",
			"fixable": true
		},
		{
			"rule": "*quotes",
			"severity": "off",
			"fixable": true
		},
		{
			"rule": "*semi",
			"severity": "off",
			"fixable": true
		}
	],
	"editor.defaultFormatter": "esbenp.prettier-vscode",
	"[javascript]": {
		"editor.defaultFormatter": "biomejs.biome"
	},
	"[typescript]": {
		"editor.defaultFormatter": "biomejs.biome"
	},
	"[javascriptreact]": {
		"editor.defaultFormatter": "biomejs.biome"
	},
	"[typescriptreact]": {
		"editor.defaultFormatter": "biomejs.biome"
	},
	"[json]": {
		"editor.defaultFormatter": "biomejs.biome"
	},
	"[jsonc]": {
		"editor.defaultFormatter": "biomejs.biome"
	},
	"[css]": {
		"editor.defaultFormatter": "biomejs.biome"
	},
	"[graphql]": {
		"editor.defaultFormatter": "biomejs.biome"
	},
	"typescript.tsdk": "node_modules/typescript/lib",
	"editor.formatOnPaste": true,
	"emmet.showExpandedAbbreviation": "never"
}
```