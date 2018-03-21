# ls

`ls` 用来显示目标列表，在 Linux 中是使用率较高的命令。

## 语法

`ls（选项）（参数）`

## 参数

- `-a`: 显示所有档案及目录；
- `-A`: 显示除文件 “.” 和 “..” 以外的所有文件列表；
- `-l`: 所有输出信息用单列格式输出，不输出为多列；
- `-m`: 用 “,” 号区隔每个文件和目录的名称；
- `-t`: 用文件和目录的更改时间排序；
- `-R`：递归处理，将指定目录下的所有文件及子目录一并处理；

## 常用命令

### 显示当前目录下包括影藏文件在内的所有文件列表

```
➜  learn-linux git:(master) ✗ ls -a
.             ..            .DS_Store     .editorconfig .git          .gitignore    LICENSE       README.md     example       src
```

### 显示除文件 “.” 和 “..” 以外的所有文件列表
```
ls -A
.DS_Store     .editorconfig .git          .gitignore    LICENSE       README.md     example       src
```

### 所有输出信息用单列格式输出
```
➜  learn-linux git:(master) ✗ ls -l
total 16
-rw-r--r--   1 wupeng10  staff  1064  3 20 18:30 LICENSE
-rw-r--r--   1 wupeng10  staff  1526  3 21 19:45 README.md
drwxr-xr-x  11 wupeng10  staff   374  3 21 19:36 example
drwxr-xr-x  14 wupeng10  staff   476  3 21 19:46 src
```

### 用 “,” 号区隔每个文件和目录的名称
```
➜  learn-linux git:(master) ✗ ls -m
LICENSE, README.md, example, src
```

### 用文件和目录的更改时间排序
```
➜  learn-linux git:(master) ✗ ls -lt
total 16
drwxr-xr-x  14 wupeng10  staff   476  3 21 19:46 src
-rw-r--r--   1 wupeng10  staff  1526  3 21 19:45 README.md
drwxr-xr-x  11 wupeng10  staff   374  3 21 19:36 example
-rw-r--r--   1 wupeng10  staff  1064  3 20 18:30 LICENSE
```
### 递归处理
```
➜  learn-linux git:(master) ✗ ls -R example/grep
example1 example2

example/grep/example1:
example1-1.md example1-2.md

example/grep/example2:
example2.md
```
