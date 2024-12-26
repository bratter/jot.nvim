# A Neovim Plugin Template

![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/ellisonleao/nvim-plugin-template/lint-test.yml?branch=main&style=for-the-badge)
![Lua](https://img.shields.io/badge/Made%20with%20Lua-blueviolet.svg?style=for-the-badge&logo=lua)

A template repository for Neovim plugins.

## Using it

Via `gh`:

```
$ gh repo create my-plugin -p ellisonleao/nvim-plugin-template
```

Via github web page:

Click on `Use this template`

![](https://docs.github.com/assets/cb-36544/images/help/repository/use-this-template-button.png)

## Features and structure

- 100% Lua
- Github actions for:
  - running tests using [plenary.nvim](https://github.com/nvim-lua/plenary.nvim) and [busted](https://olivinelabs.com/busted/)
  - check for formatting errors (Stylua)
  - vimdocs autogeneration from README.md file
  - luarocks release (LUAROCKS_API_KEY secret configuration required)

### Plugin structure

```
.
├── lua
│   ├── plugin_name
│   │   └── module.lua
│   └── plugin_name.lua
├── Makefile
├── plugin
│   └── plugin_name.lua
├── README.md
├── tests
│   ├── minimal_init.lua
│   └── plugin_name
│       └── plugin_name_spec.lua
```

## Roadmap

In general, do the following:

- Doesn't rely on jot, but having jot adds functionality, gated behind vim.executable("jot")
- Taps into Treesitter and Fzf if available to do things like make links easily

- Clean up the plugin folder structure
- Copy to system clipboard as html (requires stdin on jot), both whole buffer and selection
- Render as html live
- Everything in jot
- Toc/navigation per vim markdown; Toc and symbol navigation also exits in marksman
- Test out markmsan features, including wiki links (do they print properly?)
- Spelling is only activated on demand (this can be a command)
- Test link completion in marksman - it should be top of the list
- Quick way to add links to index files (an fzf list of index files)
