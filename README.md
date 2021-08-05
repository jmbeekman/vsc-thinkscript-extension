# tos-ts README

This is a quick and dirty syntax highlighter for the thinkScript language used by the [Think or Swim](https://www.tdameritrade.com/tools-and-platforms/thinkorswim/desktop.page) trading platform provided by [TD Ameritrade](https://www.tdameritrade.com/home.page).

If you wish to extend this with more features please feel free to [open a pr](https://github.com/jmbeekman/vsc-thinkscript-extension)  (though you'll probably need to dm me on Discord [`Yetzederixx#4364`] to merge/deploy).

## Usage

* Install
  * [VSC Marketplace](https://marketplace.visualstudio.com/items?itemName=LethalArts.tos-ts)
  * Follow the [VSC Quickstart](vsc-extension-quickstart.md) directions after cloning for a direct install.
* Start a new file with a `.tosts` extension and code.

## Reference

* [VSC Language Extensions](https://code.visualstudio.com/api/language-extensions/overview)
* [thinkScript Reference](https://tlc.thinkorswim.com/center/reference/thinkScript)

## Example

![Alt text](/images/example.png)

### Note About Example

**In order to get the same colors as the example, you'll need to add to your user settings something similar to below:**

```json
"editor.semanticTokenColorCustomizations": {
  "[Default Dark+]": {
    "enabled": true,
    "rules": {
      "*.async": { "underline": true, "foreground": "#00FFFF" },
      "*.defaultLibrary": { "bold": true },
      "*.modification": { "italic": true },
      "*.local": { "italic": true },
      "*.readonly.local": { "italic": false  },
      "namespace": { "foreground": "#839dda" },
      "interface": { "foreground": "#a4dbd0" },
      "function": { "foreground": "#E6E1BD" },
      "method": { "foreground": "#f7f2cf" },
      "typeParameter": { "italic": true, "foreground": "#00f7ff",  },
      "variable.local": { "foreground": "#c4e8fd" },
      "variable.readonly.local": { "foreground": "#d2bde8",  },
    }
  }
},
"editor.tokenColorCustomizations": {
  "[Default Dark+]": {
    "textMateRules": [
      { "scope": "constant.other.symbol.hashkey.parameter",                                         "settings": { "foreground": "#cec8fa", "fontStyle": "italic"  } },
      { "scope": "constant.language.symbol.hashkey",                                                "settings": { "foreground": "#5bb5ff", "fontStyle": "italic"  } },

      { "name": "s-namespace",                          "scope": "entity.name.namespace",            "settings": { "foreground": "#839dda"                        } },
      { "name": "s-type",                               "scope": "entity.name.type",                 "settings": { "foreground": "#4EC9B0"                        } },
      { "name": "s-type.defaultLibrary",                "scope": "support.type",                     "settings": { "fontStyle": "bold"                            } },
      { "name": "s-struct",                             "scope": "storage.type.struct",              "settings": {                                                } },
      { "name": "s-class",                              "scope": "entity.name.type.class",           "settings": {                                                } },
      { "name": "s-class.defaultLibrary",               "scope": "support.class",                    "settings": { "foreground": "#4EC9B0"                        } },
      { "name": "s-class.defaultLibrary-2",             "scope": "support.class.builtin",            "settings": { "foreground": "#4EC9B0", "fontStyle": "bold",  } },
      { "name": "s-interface",                          "scope": "entity.name.type.interface",       "settings": { "foreground": "#a4dbd0"                        } },
      { "name": "s-enum",                               "scope": "entity.name.type.enum",            "settings": {                                                } },
      { "name": "s-enumMember",                         "scope": "variable.other.enummember",        "settings": {                                                } },
      { "name": "s-function",                           "scope": "entity.name.function",             "settings": { "foreground": "#E6E1BD",                       } },
      { "name": "s-function.defaultLibrary",            "scope": "support.function",                 "settings": { "foreground": "#fff9cc", "fontStyle": "bold"   } },
      { "name": "s-method",                             "scope": "entity.name.function.member",      "settings": { "foreground": "#f7f2cf",                       } },
      { "name": "s-macro",                              "scope": "entity.name.function.macro",       "settings": { "foreground": "#00FFFF",                       } },
      { "name": "s-var",                                "scope": "entity.name.variable",             "settings": { "foreground": "#ffffff",                       } },
      { "name": "s-variable",                           "scope": "variable.other.readwrite",         "settings": { "foreground": "#c4e8fd",                       } },
      { "name": "s-variable.readonly",                  "scope": "variable.other.constant",          "settings": { "foreground": "#67CAD8",                       } },
      { "name": "s-variable.readonly.defaultLibrary",   "scope": "support.constant",                 "settings": { "foreground": "#67CAD8",                       } },
      { "name": "s-parameter",                          "scope": "variable.parameter",               "settings": { "foreground": "#fad3d6", "fontStyle": "italic" } },
      { "name": "s-property",                           "scope": "variable.other.property",          "settings": { "foreground": "#9CDCFE",                       } },
      { "name": "s-property.readonly",                  "scope": "variable.other.constant.property", "settings": { "foreground": "#8ec9e9",                       } },
      { "name": "s-event",                              "scope": "variable.other.event",             "settings": { "foreground": "#00EEDD",                       } },

      { "scope": "function.punctuation.parenthesis",                                                "settings": { "foreground": "#c7c29f",  "fontStyle": "bold"   } },
      { "scope": "array.indexer.bracket.square",                                                    "settings": { "foreground": "#84b6df",  "fontStyle": "bold"   } },
      { "scope": "support.type.primitive",                                                          "settings": { "foreground": "#4ec996",                        } },
      { "scope": "support.type.builtin",                                                            "settings": { "foreground": "#93C763",                        } },
      { "scope": "support.type.object.module",                                                      "settings": { "foreground": "#FFC4C6",                        } },

      { "scope": "variable.object.array",                                                           "settings": { "foreground": "#c4e8fd",                        } },
      { "scope": "variable.other.ruby",                                                             "settings": { "foreground": "#c5e3f5",                        } },
      { "scope": "variable.other.readwrite.instance",                                               "settings": { "foreground": "#88d1f8",                        } },
      { "scope": "variable.language",                                                               "settings": { "foreground": "#93C763",                        } },
      { "scope": "variable.language.this",                                                          "settings": { "foreground": "#93C763",                        } },
      { "scope": "variable.local variable.other.constant, source.tosts variable.other.constant",    "settings": { "foreground": "#d2bde8",                        } },

      { "scope": "constant.language.undefined",                                                     "settings": { "foreground": "#93C763",                        } },
      { "scope": "constant.language.null",                                                          "settings": { "foreground": "#93C763",                        } },
      { "scope": "constant.numeric",                                                                "settings": { "foreground": "#FFCD22",                        } },

      { "scope": "comment",                                                                         "settings": { "foreground": "#75715E",                        } },
      { "scope": "comment.block.documentation",                                                     "settings": { "foreground": "#807C69",                        } },
      { "scope": "comment.line.double-slash",                                                       "settings": { "foreground": "#5A7B48",                        } },

      { "scope": "string",                                                                          "settings": { "foreground": "#e1a289",                        } },
      { "scope": "string.unquoted",                                                                 "settings": { "foreground": "#FFDEA7",                        } },
      { "scope": "string.quoted.double",                                                            "settings": { "foreground": "#e1b889",                        } },
      { "scope": "string.quoted.double",                                                            "settings": { "foreground": "#FFB342",                        } },
      { "scope": "string.quoted.single",                                                            "settings": { "foreground": "#fabe64",                        } },

      { "scope": "keyword.operator",                                                                "settings": { "foreground": "#F92672",  "fontStyle": "bold"   } },
      { "scope": "keyword.control",                                                                 "settings": { "foreground": "#FF7F7F",  "fontStyle": "bold"   } },
      { "scope": "keyword.operator.new, keyword.control.loop, keyword.control.switch",              "settings": { "foreground": "#93C763",  "fontStyle": "bold"   } },
      { "scope": "keyword.operator.logical",                                                        "settings": { "foreground": "#93C763",  "fontStyle": "bold"   } },

      { "scope": [ "meta.decorator"],                                                               "settings": { "foreground": "#ff00e0",  "fontStyle": "bold"   } },
      { "scope": [ "meta.decorator meta.function-call entity.name.function" ],                      "settings": { "foreground": "#ff00d0",  "fontStyle": "italic" } },
    ]
  },
},
```

## Disclaimer

Not affiliated in any way, shape or form (other than a client of) TD Ameritrade. I stole the icon off the net for use on the marketplace so it wouldn't look stupid.