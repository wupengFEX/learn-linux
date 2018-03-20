# tail

`tail` 用于输入文件中的尾部内容，默认展示最后 10 行。

## 语法

`tail(选项)(参数)`

## 参数

- `-c`: 输出文件尾部的 N（N 为整数）个字节内容；
- `-n`: 输出文件的尾部 N（N 位数字）行内容；
- `-q`: 当有多个文件参数时，不输出各个文件名；


## 常用命令

- 输出后 20 个字节内容

	`tail -c 20 example/tail/example1/example1-1.md`

- 输出后 10 行内容

	`tail -n 10 example/tail/example1/example1-1.md`

- 多个文件时，输出不带文件名的结果

	`tail -q example/tail/example1/example1-1.md`
