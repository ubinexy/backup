用命令行打开项目

``` bash
#!/bin/bash

PROJECTS_DIR="..."
if [ $# == 1 ];
then
    matched_path=$(find -L ${PROJECTS_DIR} -maxdepth 1 -type d -iname "*$1*" -print0)
    open -na "Intellij IDEA.app" --args "$matched_path"
else
    open -na "Intellij IDEA.app" --args "$@"
fi
```

加x执行权限，放到 /usr/local/bin

usage:

``` bash
$ idea [dir name_of_target_project]
```
