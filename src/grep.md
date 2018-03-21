# grep

`grep` 是一种强大的文本搜索工具，它能使用正则表达式搜索文本，并把匹配的行打印出来。

## 语法

`grep 功能/参数 文件`

## 参数

- `-r`: 在某一目录下进行搜索；
- `-n`: 显示搜索到的字符串所在的行数；
- `-A n`: 搜索指定字符，输出字符串及其后的 n 行；
- `-c`: 计算搜索到的总数；
- `-i`: 忽略字符大小写的差别；
- `-l`: 列出文件内容符合指定的范本样式的文件名称；
- `-L`: 列出文件内容不符合指定的范本样式的文件名称；
- `-o`: 只输出文件中匹配的部分；
- `-E`: 通过正则表达式来进行搜索；

## 常用命令

### 单个文件搜索文本

```
➜  learn-linux git:(master) ✗ grep "grep" example/grep/example1/example1-1.md
# grep 命令的第一个 example。
```

### 多个文件搜索文本

多个文件之间以空格隔开。

```
➜  learn-linux git:(master) ✗ grep "grep" example/grep/example1/example1-1.md example/grep/example1/example1-2.md
example/grep/example1/example1-1.md:# grep 命令的第一个 example。
example/grep/example1/example1-2.md:# grep 命令的第一个 example。
```

### 单/多目录搜索

```
➜  learn-linux git:(master) ✗ grep -r "grep" example/grep/example1/
example/grep/example1//example1-1.md:# grep 命令的第一个 example。
example/grep/example1//example1-2.md:# grep 命令的第一个 example。

➜  learn-linux git:(master) ✗ grep -r "grep" example/grep/example1/ example/grep/example2/
example/grep/example1//example1-1.md:# grep 命令的第一个 example。
example/grep/example1//example1-2.md:# grep 命令的第一个 example。
example/grep/example2//example2.md:# # grep 命令的第二个 example。
```

### 输出匹配字符串所在行数

```
➜  learn-linux git:(master) ✗ grep -n "grep" example/grep/example1/example1-1.md
1:# grep 命令的第一个 example。
```

### 输出匹配及其后的 n 行

```
➜  learn-linux git:(master) ✗ grep -r -A 2 "grep" example/grep/example1/
example/grep/example1//example1-1.md:# grep 命令的第一个 example。
example/grep/example1//example1-1.md-
example/grep/example1//example1-1.md-# GrEp 命令的第一个 example。
--
example/grep/example1//example1-2.md:# grep 命令的第一个 example。
```

### 统计每个文件搜索到的总数

```
➜  learn-linux git:(master) ✗ grep -rc "grep" example/grep/example1
example/grep/example1/.DS_Store:0
example/grep/example1/example1-1.md:1
example/grep/example1/example1-2.md:1
```

### 不区分大小写搜索

```
➜  learn-linux git:(master) ✗ grep -ri "grep" example/grep/example1
example/grep/example1/example1-1.md:# grep 命令的第一个 example。
example/grep/example1/example1-1.md:# GrEp 命令的第一个 example。
example/grep/example1/example1-2.md:# grep 命令的第一个 example。
```

### 列出内容符合搜索 pattern 的文件名

```
➜  learn-linux git:(master) ✗ grep -rl "grep" example/grep/example1
example/grep/example1/example1-1.md
example/grep/example1/example1-2.md
```

### 列出内容不符合搜索 pattern 的文件名

```
➜  learn-linux git:(master) ✗ grep -rL "grep" example/grep/example1

```

### 只输出匹配的文本

```
➜  learn-linux git:(master) ✗ grep -ro "grep" example/grep/example1
example/grep/example1/example1-1.md:grep
example/grep/example1/example1-2.md:grep
```

### 正则搜索

```
➜  learn-linux git:(master) ✗ grep -rE "[a-z]" example/grep
Binary file example/grep/.DS_Store matches
Binary file example/grep/example1/.DS_Store matches
example/grep/example1/example1-1.md:# grep 命令的第一个 example。
example/grep/example1/example1-1.md:# GrEp 命令的第一个 example。
example/grep/example1/example1-2.md:# grep 命令的第一个 example。
Binary file example/grep/example2/.DS_Store matches
example/grep/example2/example2.md:# # grep 命令的第二个 example。
```
