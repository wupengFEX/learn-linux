# scp

`scp` 在 Linux 下进行远程拷贝文件的命令。

## 语法

`scp(选项)(参数)`

## 参数

- `-r`: 以递归方式复制；
- `-P`: 指定远程主机的端口号；

## 常用命令

### 从远程复制文件到本地目录

	`scp -r work@xx.xx.xx.xx:port/home/work/xx ./home/work/xx`

### 上传本地文件到远程机器指定目录

	`scp -r ./home/work/xx work@xx.xx.xx.xx:port/home/work/xx`
