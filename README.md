# kMacOSX
MacOS X 个人使用总结

以下是本人使用 MacBook Pro 的一些高效操作总结和心得，不足之处欢迎指正，email：kennyallen0520@gmail.com

1.spotlight 搜索

用于快速打开 MacBook Pro 中的应用，后面会讲到用 Alfred 代替 spotlight

control＋空格 快速打开 spotlight 搜索框，如快捷打开 terminal，可在 spotlight 搜索框中输入ter，回车即可，是不是非常方便呢。

2.创建用户

在 spotlight 搜索框中输入 pre，打开系统偏好设置，创建属于自己的用户（管理员用户），选择用户和群组，点按锁按钮以进行更改，输入管理员用户名和密码后，点击登录选项下的＋，使用单独密码创建一管理员用户，登录这个用户。


登录后，使用 spotlight 再次打开系统偏好设置
以下是我个人的系统偏好设置（仅供参考）：


通用
关闭文稿时要求保存更改


Dock

大小：自己看得舒服顺眼就行

位置：屏幕左边

最小化窗口：全选

桌面与屏幕保护程序

桌面：选自己顺眼的就行

屏幕保护程序：同上

触控板
光标与点按：全选，跟踪速度调至最快

滚动缩放：全选

更多手势：全选

（我的愚见：虽然触控板很强大，但也别把鼠标扔了，有些操作还是用鼠标更加快捷更加精确，比如精确点选，截图，选中等）

网络

连接wifi或是有线网络

3.常用快捷键（不用死记，用到的时候速查，熟能生巧）

系统快捷键

command＋F3                显示桌面

shift＋command＋3          全屏截图

shift＋command＋4          区域截图

command＋delete            删除文件

command＋c			            复制

command＋v		    	        粘贴

command＋z			            撤销

command＋x			            剪切

command＋a			            全选

command＋s			            存储

command＋h			            隐藏当前窗口

command＋m			            当前窗口最小化

command＋n			            新建窗口

command＋w		            	关闭当前窗口

command＋q			            退出当前应用程序

command＋tab			          快速切换应用程序

command＋option＋shift＋q	注销当前用户

terminal 快捷键

tap		命令自动补全

control＋u	删除当前行

control＋a	光标移动到当前行最左

control＋e	光标移动到最右

⬆️		上一个历史命令

⬇️		下一个历史命令

vi/vim编辑器快捷键

命令模式下
i					光标处插入

o					光标处下一行插入

dd					删除光标所在行

x					删除光标所在字符

num＋dd					删除光标所在行及以下 num－1 行

0					光标移动到行首

$					光标移动到行尾

G					光标移动到尾行

gg					光标移动到首行

num＋G					光标移动到 num 行

/regex					向下查找regex匹配文本，按n下一个

?regex					向上查找regex匹配文本，按n上一个

:set ignorecase				搜索时忽略大小写

:set noigorecase			搜索时区分大小写

:set hlsearch				搜索时高亮显示匹配文本

:set number				显示行号

:num1,num2/string/replacement/g		将num1到num2行的所有string替换为replacement

:%s/string/replacement/g		全文替换string为replacement

:q!					退出不保存

:wq					退出并保存

:w					保存

4.homebrew ＋ homebrew cask

homebrew 是 macOS 的安装包管理工具，类似于 CentOS 的 yum，官网：https://brew.sh

安装命令：/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

检查 homebrew 是否安装成功

brew --version

更新 homebrew 安装包

brew update

搜索 homebrew 安装包

brew search 包名

homebrew cask 是 homebrew 的扩展（加强）版，免去了下载应用安装包后拖动到文件夹的重复操作，官网：http://caskroom.github.io

安装 homebrew cask 命令：brew tap caskroom/cask

使用 homebrew cask 安装

chrome 浏览器，brew cask install google-chrome

网易云音乐，brew cask install neteasemusic

安装完成后在桌面就可以找到了

5.lantern

lantern 是一款翻墙神器，google 必备

安装命令：brew cask install lantern

6.iTerm2

iTerm2 是 macOS 的 Terminal 取代品，是一款非常强大的命令窗口，官网：http://www.iterm2.com

安装命令：brew cask install iterm2

常用快捷键

上下分屏	command＋shift＋d

左右分屏	command＋d

切换窗口	command＋num

推荐像素等宽字体 PowerLine，github：https://github.com/powerline/fonts

安装命令：
git clone https://github.com/powerline/fonts.git

cd fonts

./install.sh

cd ..

rm -rf fonts

安装完成后，在 iTerm2 窗口下按 command＋,，设置字体为 PowerLine Family，本人使用的是 Meslo LG S DZ Regular for Powerline，字体大小14pt

7.zsh ＋ oh my zsh

zsh 是非常强大的 shell 工具，更高效，更好的自动补全，更好的文件名展开等，可以自定义别名命令，如 ll="ls -l"，官网：http://www.zsh.org/

安装命令：brew install zsh zsh-completions

安装好后，设置 shell 解释命令为zsh，chsh -s /bin/zsh

oh my zsh 是一款开源的框架，用于管理 zsh 配置，配置文件 .zshrc，官网：http://ohmyz.sh/

安装命令：sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

编辑 .zshrc 配置文件

ENABLE_CORRECTION="true"

ZSH_THEME="candy" 主题可自定义，不知道选什么可以设置为random

8.autojump

autojump 记录目录索引，下次进入目录时，可直接索引到绝对目录，无需一级一级地补全进入，使用起来非常爽

安装命令：brew install autojump

修改 .zshrc 配置文件

[[ -s $(brew --prefix)/etc/profile.d/autojump.sh ]] && . $(brew --prefix)/etc/profile.d/autojump.sh

查看 autojump 版本信息 j --version

j 目录名，快速跳转

9.Alfred

Alfred 快速启动和搜索引擎，可代替 spotlight，除了快速启动应用之外，还能当搜索引擎使用，去除了打开浏览器的重复操作，官网：

https://www.alfredapp.com/

安装命令：brew cask install alfred

修改快捷键为 command＋command，连按两下打开 Alfred 搜索框

更新待续。。。
