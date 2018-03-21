# cut

`cut` 命令用来显示行中的指定部分，删除文件中指定字段。

## 语法

`cut(选项)(参数)`

## 参数

-d：指定字段的分隔符，默认的字段分隔符为“TAB”；
-f：显示指定字段的内容；
-c：仅显示行中指定范围的字符；

## 常用命令

### 显示以 '' 分割的第 2, 3 行
```
➜  learn-linux git:(master) ✗ cut -f2,3 -d" " example/cut/example1/example1-1.md
Name Mark
tom 69
jack 71
alex 68
```

### 显示 1-5 之间的字符串
```
➜  learn-linux git:(master) ✗ cut -c1-5 example/cut/example1/example1-1.md
No Na
01 to
02 ja
03 al
```
