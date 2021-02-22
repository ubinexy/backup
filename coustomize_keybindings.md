
~/Library/KeyBindings/DefaultKeyBinding.dict


```
{
    "~f"        = "moveWordForward:";               /* M-f          Move forward word */
    "~b"        = "moveWordBackward:";              /* M-b          Move backward word */
    "~d"        = ("setMark:", "moveWordForward:", "deleteToMark:");             /* M-d          Delete word forward */
    "^w"        = ("setMark:", "moveWordBackward:", "deleteToMark:");            /* Ctrl-w       Delete word backward */
    "^y"        = "yankAndSelect:";                          /* Ctrl-y       Yank:*/
    "^-"        = "redo:";			    /* Ctrl--       Redo:*/
    "^u"        = "deleteToBeginningOfLine:";      /*               deleteToBeginningOfLine */
    "^k"        = "deleteToEndOfLine:";
    "^p"        = "moveUp:";
    "^n"        = "moveDown:";
}
```
