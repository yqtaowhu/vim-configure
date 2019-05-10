# vim-configure
*Author:taoyanqi*   

## 1. vim-8 安装
```
git clone https://github.com/vim/vim.git
# vim支持python,同时指定python config路径，和安装的目录
./configure --enable-pythoninterp --with-python-config-dir=/usr/lib/python2.7/config --prefix=/home/xxx
make && make install
# 配置环境变量,使用编译的vim
export PATH="/home/xxx/bin/$PATH"
```
### 常用命令
- `vim --version`查看vim版本
- `vim --version | grep "python" `查看vim是否支持python环境,+代码支持，-不支持

## 2. vim-plug 极简的插件管理器
vim可以通过安装插件获得非常丰富的功能，当没有插件管理器时，Vim 用户必须手动下载 tarball 包形式的插件，并将它们解压到 ~/.vim 目录中。在少量插件的时候可以。但当他们安装更多的插件时，就会变得一团糟。

Vim-plug 是一个自由、开源、速度非常快的、极简的 vim 插件管理器。操作非常的简单,就可以轻松的安装和删除你的插件

### 安装vim-plug
下载到`~/.vim`目录下
`curl -fLo ~/.vim/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim`

如果需要安装一个高亮显示的插件，则直接在`~/.vimrc`文件下写入:
```
call plug#begin('~/.vim/plugged')
Plug 'itchyny/lightline.vim'
call plug#end()
```
插件安装的格式为 `Plug 'xxx/xxx'` 其中后面的为github中开源的插件<br>
写入文件后，重新打开，即可执行安装步骤：
-   查看插件状态: 在vim Normal 模式下 :PlugStatus
-   安装插件:在vim的Normal模式下 :PlugStatus
-   更新 :PlugUpdate 
-   删除一个插件删除或注释掉你以前在你的 vim 配置文件中添加的 plug 命令。然后，运行 :source ~/.vimrc 或重启 Vim 编辑器,执行:PlugClean
-   升级vim-plug :PlugUpgrade

Vim-plug 简化了插件管理,极大的方面了我们后续的安装插件过程，给vim带来了更多应用的可能。

## 3. vim 基本配置

