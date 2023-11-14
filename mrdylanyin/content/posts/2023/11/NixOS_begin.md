+++
title = "NixOS 初尝试"
date = 2023-11-14T16:48:00+08:00
lastmod = 2023-11-14T16:59:36+08:00
tags = ["nixos"]
categories = ["linux"]
draft = false
toc = true
+++

久仰 NixOS 大名挺久的了，但是一直没有装，今天心血来潮在虚拟机下面尝试了一下，总的来说不难，但是配置 hyprland 一直有问题，看 github issue hyprland 似乎对虚拟机支持并不是很好，尝试了 utm, tart, vmware fusion 之后终于放弃了 NixOS 下 hyprland 环境了。其实最接近的是 utm, 可以进入 hyprland 但是 kitty 无法打开，还是先尝试普通桌面环境吧，然后配置的差不多了，以后有机会在实体机上面装 NixOS 。

NixOS 系统的理念我还是非常喜欢的，一套配置然后就可以在不同的机器下面创建出一套一样的系统，并且后面维护这一个配置就好了。一般的系统，经常是玩一个项目，然后装一堆依赖，然后后面可能就忘了卸载，系统这样越用越大，之后无奈只能重装，然后又是重新配置环境，如此往复。
