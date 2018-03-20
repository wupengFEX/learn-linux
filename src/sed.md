# sed

`sed` 是一种流编辑器，它是文本处理中非常中的工具，能够完美的配合正则表达式使用。

## 语法

`sed [options] 'command' file(s)`

## 参数

### 选项

- `-n`: 仅显示script处理后的结果；
- `-e<script>: 以选项中的指定的script来处理输入的文本文件；
- `-f<script>: 以选项中指定的script文件来处理输入的文本文件；

### 命令

- `d`: 删除，删除选择的行；
- `s`: 替换指定字符；
- `g`: 获得内存缓冲区的内容，并替代当前模板块中的文本;
- `r file`: 从 file 中读行；
- `w file`: 写并追加模板块到file末尾；
- `W file`: 写并追加模板块的第一行到file末尾；

## 常用命令

- 替换文本中的字符串

	`sed 's/examples/example/' example/sed/example1/example1-1.md`

- 替换文本并写入到文件

	`sed -i 's/examples/example/' example/sed/example1/example1-1.md`

	注：MAC 下需要指定变量暂存替换字符串，如不需要则指定为空，`sed -i "" 's/examples/example/' example/sed/example1/example1-1.md`

- 替换第 n 个匹配到的字符串

	`echo "examplesexamplesexamples" | sed "s/examples/EXAMPLES/2"`
	`echo "examplesexamplesexamples" | sed "s/examples/EXAMPLES/3"`

- 删除第 n 行

	`sed "2d" example/sed/example1/example1-1.md`
	`sed "3d" example/sed/example1/example1-1.md`

- 删除符合某个正则的字符串所在的行

	`sed '/examples/'d example/sed/example1/example1-1.md`

- 组合多个表达式

	`echo "examplesexamplesexamples" | sed "s/examples/EXAMPLES/1" | sed "s/examples/EXAMPLES/2"`

- 在第 n 行后插入文本

	`sed -i '' '2a\ this is a pen' example/sed/example1/example1-1.md`

	注意：MAC 下 `a\` 后需要进行换行。

- 在第 n 行前插入文本

	`sed -i '' '2i\ this is a pen' example/sed/example1/example1-1.md`
