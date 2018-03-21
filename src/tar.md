# tar

`tar` 是 Linux 中的打包压缩工具。

## 语法

`tar 功能/参数 文件`

## 参数

- `-c`: 创建新的备份文件；
- `-v`: 显示指令执行过程，待 progress 效果；
- `-f`: 指定备份文件；
- `-x`: 解压备份文件；
- `-z`: 使用 gzip 压缩；
- `-j`: 使用 bzip2 压缩；
- `-t`: 列出归档文件内容目录。

## 常用命令

- 创建压缩文件

```
tar -cvf example/tar/example1-1.tar.gz example/tar/example1/
```

- 解压

```
tar -xvf example/tar/example1-1.tar.gz example/tar/example1
```

- 查看压缩文件内容

```
tar -tvf example/tar/example1-1.tar.gz
```
