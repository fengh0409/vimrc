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
./bootstrap
make 
sudo make install

```

#### 安装YouCompleteMe
YouCompleteMe安装后需要编译
```bash
cd ~/.vim/bundle/YouCompleteMe
./install.py --gocode-completer #安装go自动补全
#./install.py --all #安装全部语言自动补全
``` 
