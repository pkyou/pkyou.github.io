# Linux
基本上分为两大类: cat /etc/issue查看linux版本
RedHat 系列： RedHat Centos Fedora等
Debian系列： Debian Ubuntu等
## RedHat 系列
### rpm
RedHat package management
- rpm -ivh PackageName.rpm 
安装软件 -v显示过程 -h指定加密方式为hash
- rpm -e softwareName
卸载软件

### 包管理工具yum

yum install XX
（全称为 Yellow dog Updater, Modified）是一个在baiFedora和RedHat以及SUSE中的Shell前端软du件包管理器。yum提供了查找、zhi安装、删除某一个、一组甚dao至全部软件包的命令。

## Debian系列
- Deb包
dpkg -参数

- 包管理工具 apt-get
apt-get 是ubuntu下的软件安装方式，基于debian。 apt-get install XX

### wget
不是安装方式，而是一个下载工具，类似迅雷。通过http、 https、 ftp三个常见TCP/IP协议下载，并可以使用http代理，名字是World Wide Web”与“get”的结合。
可直接运行 `wget XX`

如果需要先下载后安装的话：
使用wget下载一个 rpm包, 然后用 rpm -ivh xxx.rpm 安装这个软件，嫌麻烦的话，就
可以直接用 yum install sqoop 来自动下载和安装依赖的rpm软件。


#  MAC
##  Homebrew
https://brew.sh/index_zh-cn.html
- brew
`brew serach XX`
`brew install XX`
`brew uninstall XX`
`brew update` --更新 brew本身
`brew upgrade` --更新所有已安装软件
`brew cleanup`
`brew list `
`brew services list`
`brew services start/stop/restart XX`

- brew cask
`brew cask install XX`
`brew cask uninstall XX`

# JS管理工具
yarn npm
Yarn是FaceBook/Google/Exponent/Tilde联合退出的新的JS包管理工具，是为了弥补npm的一些缺陷而出现的。

# python 包管理工具
 pip
 pip3

