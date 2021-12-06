用命令行打开项目

``` bash
#!/bin/bash

PROJECT_DIRS="..."
if [ $# == 1 ];
then
    if [ -e $1 ]; then
        open -na "Intellij IDEA.app" --args "$1"    
    else
        get_path_from_recents=$(find -L ${PROJECT_DIRS} -maxdepth 1 -type d -iname "*$1*" -print0)
        open -na "Intellij IDEA.app" --args "$get_path_from_recents"
    fi
else
    open -na "Intellij IDEA.app" --args "$@"
fi
```

加x执行权限，放到 /usr/local/bin

usage:

``` bash
$ idea [dir_name_of_target_project or target_project_path]
```
