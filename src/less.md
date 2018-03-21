# less

`less` 用来浏览文字档案的内容。用 `less` 命令显示文件时，用 PageUp 键向上翻页，用 PageDown 键向下翻页。要退出 `less` 程序，应按 Q 键。

## 语法

`less(选项)(参数)`

## 参数

### 选项

- `-N`: 每一行行首显示行号；
- `-s`：将连续多个空行压缩成一行显示；
- `-S`：在单行显示较长的内容，而不换行显示；

## 常用命令

- 查看显示行号的文件内容

	`less -N example/less/example1/example1-1.md`

- 将多行空格压缩成一行显示

	`less -s example/less/example1/example1-1.md`
	
- 将需要换行的一段文字展示在一行

	`less -S example/less/example1/example1-1.md`
