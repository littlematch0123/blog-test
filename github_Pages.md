# 如何使用 GitHub Pages 预览 HTML

#### 建立一个仓库

首先，需要建立一个仓库，并命名为 `username.github.io`，比如 `littlematch0123.github.io`

### 克隆这个仓库

然后，在本地找一个目录用于存储这个项目，使用下列代码来克隆

```
git clone littlematch0123.github.io
```

### 编辑 index.html 文件

进入该目录后，编辑 index.html 文件，并将其内容设置为 'hello world'

```
cd littlematch0123.github.io

echo "Hello World" > index.html

```

### 提交并上传于远程仓库

```
git add index.html
git commit -m 'add index.html'
git push
```

### 查看效果

使用浏览器打开 [littlematch0123.github.io](https://littlematch0123.github.io)，显示 'hello world'

到此，就实现了使用 github Pages 预览 HTML 的功能
