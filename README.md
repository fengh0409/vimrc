## vim配置

#### 安装最新版本vim
```bash
#Linux
yum install vim

#OS X
brew install vim
brew install macvim --with-override-system-vim
```

#### 安装插件管理工具Vundle
```bash
git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
打开vim，进入插入模式，`:PluginInstall`

#### 安装CMake(YouCompleteMe依赖)
```bash
curl -L https://cmake.org/files/v4.8/cmake-3.8.2.tar.gz -o cmake-3.8.2
cd cmake-3.8.2
./bootstrap
make 
sudo make install

```

#### 编译YouCompleteMe
:PluginInstall安装YouCompleteMe后需要编译
```bash
cd ~/.vim/bundle/YouCompleteMe
./install.py --gocode-completer #安装go自动补全
#./install.py --all #安装全部语言自动补全
``` 

#### vim-go
打开vim执行 `:GoInstallBinaries`。

其中，在安装`golang.org/x/tools/...`这种包文件时会由于网络原因无法安装，这时可以访问其镜像地址[https://github.com/golang/tools](https://github.com/golang/tools)，将源码clone下来后mv 到`golang.org/x/tools/`目录下，然后去编译相应的源码包，如`go install golang.org/x/tools/cmd/goimports`
