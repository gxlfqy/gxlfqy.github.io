# MkDocs

参考内容：https://cyent.github.io/markdown-with-mkdocs-material/

操作系统：Window 10

## 安装MkDocs

```shell
pip install mkdocs
```

建议翻墙下载，网速会好点

### 错误信息

```shell
ERROR: Cannot uninstall 'tornado'. It is a distutils installed project and thus we cannot accurately determine which files belong to it which would lead to only a partial uninstall.
```

### 解决方法

```
pip install --ignore-installed mkdocs
```

输入上面的指令之后出现的信息

```shell
ERROR: tensorflow 1.12.0 has requirement protobuf>=3.6.1, but you'll have protobuf 3.6.0 which is incompatible.
ERROR: tensorflow-gpu 1.12.0 has requirement protobuf>=3.6.1, but you'll have protobuf 3.6.0 which is incompatible.
```

### 错误原因

- 本人安装了tensorflow模块。tensorflow模块要求protobuf模块的版本为3.6.1，但MkDocs要求protobuf模块的版本为3.6.0。发生冲突

## 使用MkDocs

### 确认是否安装正确

```bash
mkdocs --version
```

### 创建一个Wiki

在E盘中创建一个wiki的文件夹，在该文件夹内创建一个mkdocs的文件夹

执行以下命令，创建一个名为`my-wiki`的wiki

```
e:
cd e:\wiki\mkdocs\
mkdocs new my-wiki
```

### 启动wiki

```
cd my-wiki
mkdocs serve
```

访问MkDocs：http://127.0.0.1:8000/

## 小技巧

- 如果使用Typora编辑Markdown文件时注意一点，Typora会把文件保存在目录```.assets```中。而该目录会被Mkdocs识别为隐藏目录被跳过，导致图片无法显示。所以应该将Typora的图片默认保存目录改为```./${filename}.assets/```