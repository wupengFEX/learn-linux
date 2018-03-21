# diff

`diff` 比较给定的两个文件的不同。

## 语法

`diff(选项)(参数)`

## 参数

-c: 显示全部内容，并标出不同之处；
-i: 不检查大小写的不同；
-q: 仅显示有无差异，不显示详细的信息；

## 常用命令

### 使得文件夹具有递归修改权限

```
➜  learn-linux git:(master) ✗ diff -c example/diff/example1/example1-1.md example/diff/example1/example1-2.md
```
