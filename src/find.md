# find

`find` 用来在指定目录下查找文件。

## 语法

`chmod(选项)(参数)`

## 参数

- depth：从指定目录下最深层的子目录开始查找；

## 常用命令

### 查看当前目录下所有文件

```
➜  learn-linux git:(master) ✗ find example/find
example/find
example/find/example1
example/find/example1/example1-1.md
```

### 查看以某个后缀结尾的文件

```
➜  learn-linux git:(master) ✗ find example/find -name "*.md"
example/find/example1/example1-1.md
```

### 匹配文件路径或者文件

```
➜  learn-linux git:(master) ✗ find example -path "*find*"
example/find
example/find/example1
example/find/example1/example1-1.md

```

### 基于正则表达式匹配文件路径

```
➜  learn-linux git:(master) ✗ find example/find -regex ".*\.md"
example/find/example1/example1-1.md
```
