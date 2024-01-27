# cscope-picker

Minimal [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim) extension for [cscope](https://cscope.sourceforge.net/).

Expect cscope database is present in current working directory.
Search for word under cursor.

Supports only:
 - all references to a symbol
 - global definitions
 - functions called by a function
 - functions calling a function

For full-featured cscope plugin see [cscope_maps.nvim](https://github.com/dhananjaylatkar/cscope_maps.nvim)

## Installation

Use your favorite plugin manager, example for [lazy.nvim](https://github.com/folke/lazy.nvim):
```lua
 {
    'sgruszka/cscope-picker',
     dependencies = {
      'nvim-telescope/telescope.nvim',
     }
 }
```

Add to your init.lua file:
``` lua
require('telescope').load_extension('cscope')

```

## Available commands
```viml
Telescope cscope references
Telescope cscope definitions
Telescope cscope called_by_this_function
Telescope cscope calling_this_function
```
## Example key bindings configuration
``` lua
vim.keymap.set('n', '<C-\\>d', require('telescope').extensions.cscope.definitions, { desc = 'Cscope Definitions' })
vim.keymap.set('n', '<C-\\>r', require('telescope').extensions.cscope.references, { desc = 'Cscope References' })
vim.keymap.set('n', "<C-\\>c", require('telescope').extensions.cscope.calling_this_function, { desc = 'Cscope calls to this function' })
vim.keymap.set('n', '<C-\\>f', require('telescope').extensions.cscope.called_by_this_function, { desc = 'Cscope funnction calls by this function' })
```
