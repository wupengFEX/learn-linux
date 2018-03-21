# rmdir

`rmdir` 用来删除空目录。

## 语法

`rmdir(选项)(参数)`

## 参数

- `-p`: 删除指定目录后，若该目录的上层目录已变成空目录，则将其一并删除；
- `-v`: 显示命令的详细执行过程；

## 常用命令

### 删除空目录
```
learn-linux git:(master) ✗ rmdir example/rmdir/example1/rmdir
```

### 删除空目录后父文件夹为空则删除父文件夹
```
learn-linux git:(master) ✗ rmdir -p example/rmdir/example1/rmdir
```
