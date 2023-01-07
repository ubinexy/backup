
create ~/Library/KeyBindings/DefaultKeyBinding.dict


```
{
    "~f"        = "moveWordForward:";                                            /* M-f          Move forward word */
    "~b"        = "moveWordBackward:";                                           /* M-b          Move backward word */
    "~d"        = ("setMark:", "moveWordForward:", "deleteToMark:");             /* M-d          Delete word forward */
    "ƒ"         = "moveWordForward:";                                            /* M-f          Move forward word */
    "∫"         = "moveWordBackward:";                                           /* M-b          Move backward word */
    "∂"         = ("setMark:", "moveWordForward:", "deleteToMark:");             /* M-d          Delete word forward */
    "^w"        = ("setMark:", "moveWordBackward:", "deleteToMark:");            /* Ctrl-w       Delete word backward */
    "^y"        = "yankAndSelect:";                                              /* Ctrl-y       Yank:*/
    "^-"        = "redo:";                                                       /* Ctrl--       Redo:*/
    "^u"        = "deleteToBeginningOfLine:";                                    /* Ctrl-k       Delete To Line Beginning */
    "^k"        = "deleteToEndOfLine:";
    "^p"        = "moveUp:";
    "^n"        = "moveDown:";
}
```


~/.zshrc

```
...

# Custom key binding
bindkey -s "^V" "^A tldr ^J"

# IDE embedded terminal  
if [[ "$TERMINAL_EMULATOR" == "JetBrains-JediTerm" ]]; then
  bindkey -s "∫" "^[b"  # Option-b
  bindkey -s "ƒ" "^[f"  # Option-f
  bindkey -s "∂" "^[d"  # Option-d
  bindkey -s "≥" "^[."  # Option-.
fi
```


## VSCode

setting.json 

``` json
{
    ...
    "terminal.integrated.macOptionIsMeta": true
}
```
