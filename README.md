## 编辑方法

### 依赖

必须：`Git`，`Hugo`，`VSCode`

可选：`PowerToys`(For Image Resizer)

### 添加文章

复制，重命名已有的md文件到`content/posts/xxxx.md`，修改文件头部的内容并删除文章内容。

或是在命令行执行

`hugo new posts/xxxx.md`

### 添加图片

在`xxxx.md`编辑界面里粘贴图片即可。图片会保存在`static/img/posts/xxxx/*`里，（因为`.vscode/settings.json`里的设置）。然后把生成的图片的url里的`/img/posts/xxxx/*`前面的路径删除。

原图片一般有几MB，最好使用`PowerToys`的`Image Resizer`调整图片大小到适合大小。可以在文章编辑完毕后一起调整并覆盖原图片。

### 测试预览

`Ctrl+Shift+p`执行`Tasks: Run Task`,`Hugo server`。在VSCode的浏览器中打开`http://localhost:1313`

因为直接在markdown preview里查看时无法正确预览图片。

`Ctrl+Shift+p`执行`Tasks: Run Task`,`Hugo build`会在本地的`public`目录下生成静态文件。不常用。

### 部署

Push到GitHub后，Github Action会自动部署到`https://ootori008.github.io/`。`draft: true`的文章不会被部署。

### 更新主题

主题文件是以`submodule`的形式放在`themes/`里的。没有必要不需要更新。很有可能会因为API变更而报错。
