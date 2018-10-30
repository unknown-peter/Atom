

# Atom

Atom默认安装目录 `C:\Users\xxx\AppData\Local`，可以选择官网Other platforms下的 `atom-x64-windows.zip` 解压使用。

## 插件安装

部分插件安装需要科学上网或Visual Studio环境

###



### apm安装

需要预先安装git

1. 添加Path系统环境变量 `C:\Program Files\Atom x64\resources\app\apm\bin`
2. 在git bash中定位到Atom packages目录 `$ cd ~/.atom/packages`
3. `$ apm install <package-name>`

## 常用插件

* markdown-preview-plus (markdown预览 禁用原有markdown-preview插件；为与markdown-scroll-sync兼容，使用apm安装2.4.16版本 `apm install markdown-preview-plus@2.4.16`)
* markdown-scroll-sync (markdown同步滚动)
* markdown-image-paste (markdown图片粘贴)
* markdown-table-editor (markdown表格编辑)
* markdown-toc (markdown目录生成)
* markdown-themeable-pdf (markdown另存为pdf)
* pdf-view (pdf文件预览)
* language-markdown (代码着色及自动生成)
* file-type-icons (文件类型图标)
* activate-power-mode (粒子效果)
