用命令行打开项目

``` bash
#!/bin/bash

if [ $# == 1 ];
then
    matched_path=$(find -L ${HOME}/TW/psa -maxdepth 1 -type d -iname "*$1*" -print0)
    open -na "Intellij IDEA.app" --args "$matched_path"
else
    open -na "Intellij IDEA.app" --args "$@"
fi
```
