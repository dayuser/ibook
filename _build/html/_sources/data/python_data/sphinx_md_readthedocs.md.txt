# 克隆git仓库到本地

```
 git clone https://gitee.com/dayuser/ibook.git
```

## 安装python依赖包 基于python3.7.3

```
pip3 install sphinx sphinx_rtd_theme recommonmark sphinx-markdown-tables sphinxemoji -i https://pypi.tuna.tsinghua.edu.cn/simple

```

## 初始化Sphinx

```
# 进入Git根目录
cd ~/ibook
# 开始快速配置sphinx
sphinx-quickstart

# 选择把源文件和删除文件分开（y）
> Separate source and build directories (y/n) [n]:y
# 项目名称
> Project name: ibook
# 作者姓名
> Author name(s): Tsanfer
# 版本号
> Project release []: 0.2
# 语言
> Project language [en]: zh_CN

```

# 验证配置是否正确：

```
cd ~/ibook
make html
```

> 浏览器打开`./build/index.html`查看

## 配置Sphinx主题，插件

> 配置`./source/conf.py`配置文件：

```
# -- General configuration ---------------------------------------------------

# Add any Sphinx extension module names here, as strings. They can be
# extensions coming with Sphinx (named 'sphinx.ext.*') or your custom
# ones.

extensions = [
        'recommonmark',
        'sphinx_markdown_tables',
        'sphinxemoji.sphinxemoji',
]

# -- Options for HTML output -------------------------------------------------

# The theme to use for HTML and HTML Help pages.  See the documentation for
# a list of builtin themes.
#
html_theme = 'sphinx_rtd_theme'

# The master toctree document.
master_doc = 'index'
```

