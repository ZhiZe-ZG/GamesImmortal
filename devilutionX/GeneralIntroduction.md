# General Introduction

## Diablo

暗黑破坏神是暴雪的招牌 IP 之一，在各种离奇操作把自己搞得困境重重的时候，暴雪祭出的脱困法宝就是开发暗黑破坏神续作。或许暴雪觉得，只要暗黑 4 大卖，一切都会好起来的。不过，截至写稿的时候，暗黑 4 还没有正式发售，所以一切是否能如暴雪所预计的只能拭目以待。反正知则是被暴雪整得很心累，不会考虑太早入坑暗黑 4。所以，知则把目光投向了过去，投向了 Diablo-like 的元老，初代 Diablo。

这个非常古老的游戏已经被暴雪抛弃，甚至没有做一个高清重制版来圈钱。现在如果想获取这个游戏可以在 GOG 上购买：

* Diablo + Hellfire: <https://www.gog.com/game/diablo>

这个版本不仅包括游戏本体，还包括当初外包制作的资料片 Diablo: Hellfire。Diablo: Hellfire 在原版的基础上对游戏内容做了扩展，但按当时那个时代开发资料片的风格，资料片有一个独立的启动程序，而不是直接覆盖原版启动程序。如果你玩了半天发现没有 Hellfire 增加的内容，请检查一下启动的是不是 Hellfire 版。

## devilutionX

GOG 上售卖的 Diablo 虽然能在 Windows 11 上正常启动，但受限于开发时的技术环境，这个游戏如今玩起来有很多不舒服的地方。例如锁定的低分辨率和画面宽高比。你可以通过非官方的画面补丁之类的来解决这个问题。但由于 Diablo 本身的程序并不开源，这些补丁所能做的比较有限。

知则建议使用 devilutionX 来代替各种非官方补丁。 devilutionX 本身不是一个补丁程序，而是一套能实现 Diablo 玩法的程序源码，其本身并不依赖于原版的 Diablo 可执行程序，而仅仅需要其数据文件。在 devilutionX 项目中，系统适配、画面调整、 bug 修复、 UI 改进、机制更改等都可以通过直接改动源码来解决。所以， devilutionX 比原版的 Diablo 更具灵活性，你可以在 Linux， Mac 甚至 Android 和 iOS 上玩 devilutionX，也可以通过 devilutionX 提供的接口来更方便地制作 mod。

不过注意，由于版权问题， devilutionX 不能直接在其项目中包括 Diablo 的原始素材文件（包括声音和图像文件等）。你首先需要一份 Diablo 的游戏拷贝，然后将其中的数据文件复制给 devilutionX，这样才能使用 devilutionX 体验完整的游戏。

## devilutionX 安装方式

devilutionX 支持多个软硬件平台，而且有的平台还提供了多种安装方式。在其官方的文档中有比较详细的安装说明：

* devilutionX docs Installing: <https://github.com/diasurgical/devilutionX/blob/master/docs/installing.md>

在这一期，我们简单演示 Windows 系统上 devilutionX 的安装方式。

整个过程并不复杂，第一步是打开 devilutionX 的 GitHub 项目页面：

* devilutionX: <https://github.com/diasurgical/devilutionX>

在项目的发布页面选择对应系统版本的程序下载。这里我们下载适用于 64 位 Windows 系统的版本。下载的文件是一个压缩包，解压后启动其中的 `devilutionx.exe` 即可运行，不需要经过什么安装引导程序。不过此时还缺少游戏数据文件，没法正常游戏，所以还需要从 GOG 版 Diablo 中复制游戏数据。

如果你自己在 GOG 上购买了游戏，那么下载安装之后，打开游戏的安装路径，从中复制 `DIABDAT.MPQ` 文件到 devilutionX 的根目录（也就是解压后 `devilutionx.exe` 所在的目录）下。这仅仅是原版游戏主体的数据文件，此外还要从游戏安装路径下的  `hellfire` 文件夹复制以下 4 个文件到 devilutionX 的根目录：

* `hellfire.mpq`
* `hfmonk.mpq`
* `hfmusic.mpq`
* `hfvoice.mpq`

对于使用中日韩翻译的玩家，还需要再下载一个游戏专用的字体数据文件到 devilutionX 文件夹。这个文件叫 `font.mpq` 从以下地址下载：

* devilutionX 的 CJK 字体文件 `fonts.mpq`: <https://github.com/diasurgical/devilutionx-assets/releases/download/v2/fonts.mpq>

此外，还有俄语和波兰语的声音文件可选。需要的玩家可以根据 devilutionX 的安装指南自行安装。

完成上述文件的复制之后，就可以启动 `devilutionx.exe` 进入游戏啦。

## 游戏设置

进入游戏之后，建议先对 devilutionX 进行设置。这里不仅能调整分辨率等画面参数，也能开关 devilutionX 增加的一些改善游戏体验的功能，例如自动捡钱，显示具体的血量、魔量、伤害数值，买卖物品时显示物品图标等。如果需要更多信息可以查看 devilutionX 的文档或者源码。

## 存档和配置备份

如果你不希望自己辛辛苦苦打出来的存档或者配置文件因为换电脑之类的事情丢失，或者如果你需要在多个设备上同步游戏进度，那么可以自己到游戏存档和配置文件的路径备份或者覆盖文件。

Windows 平台上的存档和配置文件默认路径是

```shell
%AppData%\diasurgical\devilution
```

其中的 `%AppData%` 是你的用户应用数据路径。你可以直接在文件浏览器（File Explorer）的地址栏中输入这个路径然后回车确认直接抵达。

如果你喜欢一层一层点击文件夹，那么 `%AppData%` 一般是 `C:\Users\<username>\AppData\Roaming`。其中的 `<username>` 替换成你的 Windows 用户名。

其他操作系统上的存档和配置文件默认路径可以参考官方的百科：

* devilutionX Wiki Configuration Guide: <https://github.com/diasurgical/devilutionX/wiki/DevilutionX-diablo.ini-configuration-guide>

此外还可以通过命令行参数修改存档和配置文件的保存路径，详情参考官方百科：

* devilutionX Wiki Arguments Guide: <https://github.com/diasurgical/devilutionX/wiki/DevilutionX-additional-arguments-configuration-guide>

## 游戏内容百科

devilutionX 的文档主要是对程序的使用说明，并不包括对游戏内容的详细说明。而 Diablo 这些老游戏也很少在游戏内包括系统的说明和新手指导。如果对游戏内容有所疑惑，可以参考如下资料。

* Diablo Hellfire Tomb of Knowledge: <http://www.ladyofthecake.com/diablo/index.html>
* Jarulf's Guide to Diablo and Hellfire: <http://www.bigd-online.com/JG/JGFrame.html>
* 凯恩之角 暗黑1: <https://wiki.d.163.com/index.php?title=%E9%A6%96%E9%A1%B5_%E6%9A%97%E9%BB%911>

其中的 Jarulf's Guide to Diablo and Hellfire 是 devilutionX 开发时的参考，内容说明也很详细，个人比较推荐。
