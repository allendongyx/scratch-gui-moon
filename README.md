# scratch-gui-moon

针对Scratch 3.0的 二次开发经验，代码分析

### 开发目标
1. 色调、布局二次开发；
2. 插件，（人脸识别、语音识别）二次开发；
3. 引入自定义资源（角色、背景、声音）(Spirte，Backdrop, Sound)，由后台控制；
4. 微信分享游戏，支持触摸屏及虚拟按键；
5. 接入自身用户体系；
6. 项目案例；
...


### 关于Scratch 3.0 架构

之前2.0 是运行的flash之上的，3.0 是基于React + Redux做的，所以想要二次开发需要相关经验；



3.0 所有的代码都开源在了 Github上，之前一直是开发版本，19年初算是正式发布了，相对来说也稳定了很多；

然后积木那块核心用的是Google的Blockly项目，这个项目本身是开源了，主要是做可视化代码编程（积木代码）
地址：https://developers.google.cn/blockly/
很多做类似编程的公司，都在基于Blockly来做，国内的编程猫也是的，国外的Codecombat，CodeMonkey貌似都是；

新版的Scratch把代码基于不同项目业务做了拆分，包括国际化、VM、Sound、Canvas这部分的项目都拆了出来

- scratch-gui 这是Scratch的展示层项目，主要由React构建
- scratch-vm 这是Core项目，主要是一些底层处理
- scratch-audio 这个主要是处理音频
- scratch-blocks 基于Google Blockly开发的Scratch积木块
- scratch-l10n 国际化的
- scratch-svg-renderer PNG转SVG、SVG编辑等等
... 还有其他的，具体可以到 Scratch的Git主页去看
https://github.com/LLK

这样的好处在于项目分拆后本身不会存在依赖，简单理解就是你其实在对技术有信心的情况下，完全可以使用vm\audio\blocks这部分代码，重做一些自己的Gui项目

### Scratch还在更新，如何更优雅、低侵入的同步最新代码，开发自己的功能？

Scratch 这个项目本身还特么在更新，比如你现在拉下来最新一份Scratch-Gui，然后针对性的二次开发，但是会改到源码部分，造成很强的代码侵入，后续官方发布的Scratch-Gui项目的Fixed和更新，不太容易Pull，很容易代码冲突，不然就一行一行代码比较，Merge是一件很痛苦的事情；

我们目前的解决方式是...

### 

持续更新中....
