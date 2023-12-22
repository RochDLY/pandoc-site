---
title: 'Les snippets dans LazyVim'
date: 2023-12-22
---

Aujourd'hui je viens de tester l'utilisation des snippets dans LazyVim (il y
aura un prochain billet sur la configuration de mon environnement d'écriture.).

Pour faire des snippets rien de plus simple !
Il suffit de charger le plugin LuaSnip (merci au fil de
[discussion](https://github.com/LazyVim/LazyVim/discussions/54)) :

```lua
  {
    "L3MON4D3/LuaSnip",
    config = function()
      require("luasnip.loaders.from_lua").load({ paths = "~/.config/nvim/snippets" })
    end,
  },
```

puis d'ajouter les snippets en LUA dans le dossier donné dans le chemin
ci-dessus.

Pour mon premier snippet, j'ai créé un noeud texte pour générer le YAML des
posts de ce blog.

```lua
local ls = require("luasnip")
local s = ls.snippet
local t = ls.text_node

return {
  -- Example of a multiline text node
  s({trig = "@post", dscr = "return yaml for posts on my blog."},
    {
      t({"---", "title: ''", "date:", "---"})
    }
  ),
  }
```
C'est aussi simple que ça !
Il me suffit d'appeler le déclencheur `@post` pour voir apparaître mes 3 lignes
de YAML :-)

![Un petit exemple](/images/snippets.gif)
