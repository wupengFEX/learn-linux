# wc

`wc` 用来计算数字。

## 语法

`wc(选项)(参数)`

## 参数

- `-c`: 只显示Bytes数；
- `-l`: 只显示列数；
- `-w`: 只显示列数；

## 常用命令

- 计算文件内容字节数

```
➜  learn-linux git:(master) ✗ wc -c example/wc/example1/example1-1.md
     302 example/wc/example1/example1-1.md
```
	
- 计算行数

```
➜  learn-linux git:(master) ✗ wc -l example/wc/example1/example1-1.md
       8 example/wc/example1/example1-1.md
```

- 计算列数

```
➜  learn-linux git:(master) ✗ wc -w example/wc/example1/example1-1.md
      30 example/wc/example1/example1-1.md
```
