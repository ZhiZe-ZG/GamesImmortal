# 游戏可扩展性

## 引言

一款游戏想要获得长久的生命力，仅仅能在新的计算机平台上运行是远远不够的。如果它的游戏内容枯燥无味，那么即便它能在所有计算机平台上运行，也不一定会有多强的生命力。

从游戏开发的初期来看，游戏的作者是游戏内容的主要制作者。但长期来说，有玩家社区参与的游戏才真正在游戏内容上具有持久的生命力。所以游戏程序的可扩展性也是游戏生命力的一个重要指标。

## 数据扩展

游戏的扩展也可以大致分为数据和行为两个层面。一般来说，利用已有的机制增加一张新地图或者一种新怪物就属于数据扩展。这类扩展一般通过修改或扩展游戏的数据文件就能做到。但实际当中，可能会有很多困难。例如，由于游戏框架的设计问题，导致一些数据信息直接写死在了游戏行为文件中，那么自然就没法通过数据文件修改来实现相应的扩展或更改。

以 RTS 游戏为例，很多 RTS 游戏都提供地图编辑器让玩家自己编辑地图数据，但是兵种信息则更多地写死在行为文件中。所以想做个地图很容易，但是想做个新兵种就没那么简单了。

此外还有可能游戏框架设计问题导致某些数据只能修改没法扩展。例如一些 RTS 游戏中阵营个数是预先在行为文件中定死的，即便你完整做出来一个阵营的数据文件也只能做替换，而没法直接做添加。

另一方面，数据扩展也有功能十分强大的时候。例如对于采用了虚拟机技术的游戏框架来说就是如此。因为游戏当中的大多数行为已经通过这一技术转换为了数据文件。对于没有采用虚拟机的游戏来说，修改伤害的结算方式可能需要通过修改行为文件实现，但对于使用虚拟机的游戏框架来说，可能只是改改数据脚本的事情。

所以数据扩展能对一款游戏做什么以及做到什么程度，和游戏最初的框架设计有很大关系。

## 行为扩展

通过修改数据文件做不到的改动可以通过修改行为文件实现。而行为的扩展又细分两种情况：

一种是直接修改行为文件本身。这种方法最根本，但是相对来说比较麻烦。如果游戏本身不提供源码的话，这种修改就困难重重。

另一种则是游戏框架的行为文件本身预留了一些扩展接口。通过这些接口来对游戏行为进行扩展或修改。如果接口预留得当，那么这种方法的扩展能力不会比直接修改原始的行为文件差多少，同时却更加方便安全且不需要源码。而代价同样是需要在游戏设计之初就做好规划和预留。
