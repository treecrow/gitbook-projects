# mac

## 软件列表

软件         | 功能
---------- | -------
cheetsheet | 显示应用快捷键
tickets    | 打字出声音
Spectacle  | 窗口规范化放置
AppCleaner | 彻底删除应用

--------------------------------------------------------------------------------

## 重装系统后高效配置Mac

作用            | 步骤
------------- | -----------------------------------------
设置轻触单击        | setting-触控板- 轻点来点按
将Dock停靠在屏幕左边  | setting-Dock
全键盘控制模式       | setting-键盘-快捷键-所有控制
快速锁定屏幕（触发角功能） | setting-桌面与屏幕保护程序-屏幕保护程序-触发角-将显示器置入睡眠状态
设置睡眠就需要密码     | setting-安全性与隐私-通用-进入睡眠或开始屏幕保护程序 立即 要求输入密码

--------------------------------------------------------------------------------

## 翻墙

## - [2017 Google hosts 持续更新](https://laod.cn/hosts/2017-google-hosts.html)

--------------------------------------------------------------------------------

## zsh

### 安装步骤

程序                                                                 | 作用
------------------------------------------------------------------ | --------------------
brew install zsh                                                   | 安裝 zsh（这一步可以不执行？）
git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh | 下载一个 .oh-my-zsh 配置
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc              | 创建新配置
chsh -s /bin/zsh                                                   | 把 zsh 设置成默认的 shell
open -e ~/.zshrc,然后添加 source ~/.bash_profile                       | 解决重启terminal后命令无效的问题

### 参考文档

- [mac修改了$path但是每次打开terminal都需要source](https://segmentfault.com/q/1010000002719737)
- [把 Mac 上的 bash 换成 zsh](http://www.cnblogs.com/heiniuhaha/archive/2011/10/18/2216357.html)
- [bash 轉移 zsh (oh-my-zsh) 設定心得](http://icarus4.logdown.com/)
- [zsh 全程指南](http://wdxtub.com/2016/02/18/oh-my-zsh/)
- [zsh 快捷键](http://www.cnblogs.com/zrui513/p/5668610.html)
- [终极 Shell----ZSH](https://zhuanlan.zhihu.com/p/19556676?columnSlug=mactalk)

--------------------------------------------------------------------------------

## 其它

- [Mac技巧之用苹果电脑自带的钥匙串访问（Keychain Access）记录需要密码保护的重要/敏感信息](http://www.mac52ipod.cn/post/mac-keychain-access-password-protected-inportant-info.php)