# cp

`cp` 用来将一个或多个源文件或者目录复制到指定的目的文件或目录。

## 语法

`cp(选项)(参数)`

## 参数

- `-f`: 强行复制文件或目录，不论目标文件或目录是否已存在；
- `-i`: 覆盖既有文件之前先询问用户；
- `-R/r`: 递归处理，将指定目录下的所有文件与子目录一并处理；

## 常用命令

### 将一个文件夹下所有内容复制到另一个文件夹
```
➜  learn-linux git:(master) cp -r example/cp/example1/ example/cp/example2
```