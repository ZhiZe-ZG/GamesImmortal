# General Introduction

## Diablo

暗黑破坏神是暴雪的招牌 IP 之一，在各种离奇操作把自己搞得困境重重的时候，暴雪祭出的脱困法宝就是开发暗黑破坏神续作。或许暴雪觉得，只要暗黑 4 大卖，一切都会好起来的。不过，截至写稿的时候，暗黑 4 还没有正式发售，所以一切是否能如暴雪所预计的只能拭目以待。反正知则是被暴雪整得很心累，不会考虑太早入坑暗黑 4。所以，知则把目光投向了过去，投向了 Diablo-like 的元老初代 Diablo。

这个非常古老的游戏已经被暴雪抛弃，甚至没有做一个高清重制版来圈钱。现在如果想获取这个游戏可以在 GOG 上购买：

* Diablo + Hellfire: <https://www.gog.com/game/diablo>

这个版本不仅包括游戏本体，还包括当初外包制作的资料片 Diablo: Hellfire。Diablo: Hellfire 在原版的基础上对游戏内容做了扩展，但按当时那个时代开发资料片的风格，资料片有一个独立的启动程序，而不是直接覆盖原版启动程序。如果你玩了半天发现没有 Hellfire 增加的内容，请检查一下启动的是不是 Hellfire 版。

## devilutionX

GOG 上售卖的 Diablo 虽然能在 Windows 11 上正常启动，但受限于开发时的技术环境，这个游戏如今玩起来有很多不舒服的地方。例如锁定的低分辨率和画面宽高比。你可以通过非官方的画面补丁之类的来解决这个问题。但由于 Diablo 本身的程序并不开源，这些补丁所能做的比较有限。

知则建议使用 devilutionX 来代替各种非官方补丁。 devilutionX 本身不是一个补丁程序，而是重新实现了 Diablo。也就是说，它实际上重写了一个能实现 Diablo 玩法的程序，并开源发布。在 devilutionX 项目中，系统适配、画面调整、 bug 修复、 UI 改进、机制调整等都可以通过直接改动源码来解决。所以， devilutionX 比原版的 Diablo 更具灵活性，你甚至可以在 Linux， Mac 甚至 Android 和 iOS 上玩 devilutionX，也可以通过 devilutionX 提供的接口来更方便地制作 Mod。

不过，由于版权问题， devilutionX 不能直接在其项目中包括 Diablo 的原始素材文件（包括声音和图像文件等）。你首先需要一份 Diablo 的游戏拷贝，然后将其中的数据文件复制给 devilutionX，这样才能使用 devilutionX 体验完整的游戏。在这一期，我们仅仅介绍 Windows 系统上 devilutionX 的安装方式。

整个过程并不复杂，第一步是打开 devilutionX 的 GitHub 项目页面。在这个页面上可以找到详细的安装说明的链接，其中的内容比这期简单的视频要丰富多了。

* devilutionX: <https://github.com/diasurgical/devilutionX>

在项目的发布页面选择对应系统版本的程序下载。这里我们下载适用于 64 位 Windows 系统的版本。下载的文件是一个压缩包，解压后启动其中的 `devilutionx.exe` 即可运行，不需要安装。不过此时还缺少游戏数据文件，没法正常游戏，所以还需要从 GOG 版 Diablo 中复制游戏数据。

如果你自己在 GOG 上购买了游戏，那么下载安装之后，打开游戏的安装路径，从中复制 `DIABDAT.MPQ` 文件到 devilutionX 的根目录（也就是解压后 `devilutionx.exe` 所在的目录）下。这仅仅是原版游戏主体的数据文件，此外还要从游戏安装路径下的  `hellfire` 文件夹复制以下 4 个文件到 devilutionX 的根目录：

* `hellfire.mpq`
* `hfmonk.mpq`
* `hfmusic.mpq`
* `hfvoice.mpq`

对于使用中日韩翻译的玩家，还需要再下载一个游戏专用的字体数据文件到 devilutionX 文件夹。这个文件叫 `font.mpq` 从以下地址下载：

* devilutionX 的 CJK 字体文件 `font.mpq`: <https://github.com/diasurgical/devilutionx-assets/releases/download/v2/fonts.mpq>

此外，还有俄语和波兰语的声音文件可选。需要的玩家可以根据 devilutionX 的安装指南自行安装。

完成上述文件的复制之后，就可以启动 `devilutionx.exe` 进入游戏啦。

进入游戏之后，建议先对 devilutionX 进行设置。这里不仅能调整分辨率等画面参数，也能开关 devilutionX 增加的一些改善游戏体验的功能，例如在血条魔条上显示具体的血量、魔量数值等。如果需要更多信息可以查看 devilutionX 的文档或者源码。

## 游戏内容百科

devilutionX 的文档主要是对程序的使用说明，并不包括对游戏内容的详细说明。而 Diablo 这些老游戏也很少在游戏内包括系统的说明和新手指导。如果对游戏内容有所疑惑，可以参考如下资料。

* Diablo Hellfire Tomb of Knowledge: <http://www.ladyofthecake.com/diablo/index.html>
* Jarulf's Guide to Diablo and Hellfire: <http://www.bigd-online.com/JG/JGFrame.html>
* 凯恩之角 暗黑1: <https://wiki.d.163.com/index.php?title=%E9%A6%96%E9%A1%B5_%E6%9A%97%E9%BB%911>

其中的 Jarulf's Guide to Diablo and Hellfire 是 devilutionX 开发时的参考，内容说明也很详细，个人比较推荐。

