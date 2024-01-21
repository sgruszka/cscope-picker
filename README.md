# cscope-picker

Telescope extension for cscope

#WIP

:lua require'telescope'.load_extension 'cscope'

:Telescope cscope references
:Telescope cscope definitions
:Telescope cscope called_by_this_function
:Telescope cscope calling_this_function

:lua vim.keymap.set('n', '<C-\\>d', require('telescope').extensions.cscope.definitions, { desc = 'Cscope Definitions' })
:lua vim.keymap.set('n', '<C-\\>r', require('telescope').extensions.cscope.references, { desc = 'Cscope References' })
:lua vim.keymap.set('n', "<C-\\>c", require('telescope').extensions.cscope.calling_this_function, { desc = 'Cscope calls to this function' })
:lua vim.keymap.set('n', '<C-\\>f', require('telescope').extensions.cscope.called_by_this_function, { desc = 'Cscope funnction calls by this function' })
