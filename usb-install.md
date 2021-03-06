## U盘安装 macOS 系统的方法

如果你对系统有洁癖或原本系统已凌乱不堪，那么可能还是希望能格式化「全新安装 macOS」的

不过由于苹果官方只提供了 macOS 的升级程序，并没提供完整 dmg 镜像，想要全新安装的话，只能自己制作一个 macOS Mojave 的U盘启动盘/安装盘了。这样以后给 Mac 重装系统，在没网络的情况下给多台机器装机都方便许多。

### 制作 U 盘启动盘/安装盘

1. 准备一个 8GB 或更大容量的 U盘
2. 下载好 macOS Mojave 正式版的安装程序备用，先不要启动安装
3. 打开 “应用程序 → 实用工具 → 磁盘工具”，将U盘「抹掉」(格式化) 成「Mac OS X 扩展（日志式）」格式、GUID 分区图，并将 U 盘命名为「Mojave」。注意：这个盘符名称必须与后面的命令里的名称一致
4. 打开 “应用程序→实用工具→终端”，将下面的一段命令复制并粘贴进去：

> 如要制作 macOS Mojave 启动盘，U盘名称要改成「Mojave」(必须与下面命令对应)，然后拷贝这段命令：

```
sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /Volumes/Mojave /Applications/Install\ macOS\ Mojave.app --nointeraction
```

> 如要制作 macOS High Sierra 启动盘，U盘名称要改成 HighSierra (要与下面命令对应)，拷贝这段命令：

```
sudo /Applications/Install\ macOS\ High\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/HighSierra --applicationpath /Applications/Install\ macOS\ High\ Sierra.app --nointeraction
```

> 如要制作「旧版本的 macOS Sierra」，U盘名称改成 Sierra，拷贝这段命令：

```
sudo /Applications/Install\ macOS\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/Sierra --applicationpath /Applications/Install\ macOS\ Sierra.app --nointeraction
```


5. 回车并执行该命令，这时会提示让你输入管理员密码，便会开始制作过程了
6. 请耐心等待直到屏幕最后出现 Done. 字样即表示大功告成了！

### 通过 U 盘安装 macOS Mojave / 格式化重装 (抹盘全新安装系统) 方法

> 当你制作好 macOS Mojave 的安装盘 U 盘之后，你就可以利用它来给 Mac 电脑格式化重装 (抹盘安装)了

1. 备份好 Mac 里所有的重要数据
2. 插上制作好的安装U盘，如果系统能识别出来即可，这时我们先关机
3. 按下电源键开机，当听到“噹”的一声时，按住 Option 键不放，直到出现启动菜单选项
4. 这时选择安装U盘 (黄色图标) 并回车，就可以开始安装了，在过程中你可以通过“磁盘工具”对 Mac 的磁盘式化或者重新分区等操作
5. 之后就是一步一步的安装直到完成了

