---
layout: post
title: "Ubuntu 20.04系统环境配置"
description: "系统bug解决以及软件安装"
categories: [Tech]
tags: [linux, ubuntu]
redirect_from:
  - /2020/11/04/
---

* Kramdown table of contents
{:toc .toc}

# 中文输入法

系统自带的ibus倒是也能用，但是点开chromium就是不能输入中文

最后决定装fcitx

注意，fcitx5装了一下个人感觉对Ubuntu 20.04支持不好，所以还是安装fcitx4比较好

参考博客[如何现在就在 Ubuntu 20.04 用上 Fcitx 5](https://plumz.me/archives/11740/)

以及[在 Ubuntu 20.04 下安装 fcitx 4.2.9.8](https://plumz.me/archives/12018/)

具体安装指令

{% highlight shell %}

sudo add-apt-repository ppa:ikuya-fruitsbasket/fcitx
sudo apt update
sudo apt upgrade
sudo apt install fcitx
sudo apt install fcitx-googlepinyin -y

{% endhighlight %}

话说fcitx官方wiki里面贴的PPA源当前好像还不支持Ubuntu 20.04，但是上面那个PPA源其实也是官方的更新。

另外，我安装的谷歌输入法，其实也可以安装别的，里面上面那个人博客的配置。

{% highlight shell %}

sudo apt install fcitx-module-cloudpinyin fcitx-mozc fcitx-sunpinyin

{% endhighlight %}

关于输入法配置，终端输入`im-config`可弹出窗口，在里面选小企鹅输入法fcitx

之后计算机注销，重登录

右上角图标可以配置，或者`fcitx-config-gtk3`，选谷歌输入法即可


# Proxy SwitchyOmega

发现之前安装的chrome插件不能正常启用，删除重装

仍旧去官方release页面下载crx文件

但是目前不能直接拖动到拓展程序里直接启用了

现将后缀crx改为zip，在合适的路径

`unzip SwitchyOmega_Chromium.zip -d [your path]`

拓展程序页面打开开发者模式，点“加载已解压的拓展程序”，选择解压文件夹

加载成功！