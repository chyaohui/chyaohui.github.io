
![](http://yp.3yi.ink/s/6f41e553dba88f4e6badd471e9fe3bdb)

<div align='center' >flutter 爱好者的每周简报</div>

## Flutter 周刊 #002

这里记录每周值得分享的flutter内容, 每周五发布。


### 文章和教程

[Ripple Animation In Flutter](https://medium.com/flutterdevs/ripple-animation-in-flutter-3421cbd66a18 "Ripple Animation In Flutter")
![](https://imgkr.cn-bj.ufileos.com/853cde7b-e26a-490c-9db1-c4b017aab910.gif)

引入Ripple动画，会使按钮点击效果眼前一亮。上文详细介绍了Ripple的用法，全部源码可查看[Github](https://github.com/flutter-devs/flutter_ripple_animation_demo "Github")

```
Widget _button() {
  return Center(
    child: ClipRRect(
      borderRadius: BorderRadius.circular(widget.size),
      child: DecoratedBox(
        decoration: BoxDecoration(
          gradient: RadialGradient(
            colors: <Color>[
              widget.color,
              Color.lerp(widget.color, Colors.black, .05)
            ],
          ),
        ),
        child: ScaleTransition(
            scale: Tween(begin: 0.95, end: 1.0).animate(
              CurvedAnimation(
                parent: _controller,
                curve: const PulsateCurve(),
              ),
            ),
            child: Icon(Icons.speaker_phone, size: 44,)
        ),
      ),
    ),
  );
}
```



[Taking Flutter Animations for a Test Rive](https://dev.to/glsolaria/taking-flutter-animations-for-a-test-rive-g46 "Taking Flutter Animations for a Test Rive")
![](https://imgkr.cn-bj.ufileos.com/eb0bd845-5011-49bb-be56-d06bd93f6d21.gif)


Rive（曾用名Flare）：一个创建Flutter动画的工具和一个运行这些动画的库。这套完整的工具链可以让你在flutter上运行复杂的动画。
![](https://imgkr.cn-bj.ufileos.com/4841ea15-b46a-431e-9d75-605214964619.gif)

[How to improve your Flutter application with gradient designs](https://medium.com/flutter-community/how-to-improve-your-flutter-application-with-gradient-designs-63180ba96124 "How to improve your Flutter application with gradient designs")

渐变是美丽的设计元素，在设计界正经历着复兴。包括Hulu和Spotify在内的大公司经常在他们的产品中使用这种设计。本文将教你如何在Flutter应用中添加和定制这些渐变设计。
![](https://imgkr.cn-bj.ufileos.com/52372236-8c1d-41ca-8380-ba260e861823.png)

```
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        title: 'Flutter Gradient Demo',
        home: Scaffold(
          appBar: AppBar(
            title: const Text('Flutter Gradient Demo'),
          ),
          body: Center(
            child: Container(
              decoration: BoxDecoration(
                gradient: SweepGradient(
                  colors: [Colors.yellow,Colors.green, Colors.blue],
                ),
              ),
            ),
          ),
        ));
  }
}
```



### 开源项目

[Flokk – A Desktop App built with Flutter!](https://github.com/gskinnerTeam/flokk "Flokk – A Desktop App built with Flutter!")

这周最激动人心的开源项目必须要数Flokk了。gskinner团队联合谷歌Flutter团队发布了可在MacOS,Linux,Windows上使用的桌面应用，这是一个整合了GitHub和Twitter的联系人管理软件，具体介绍可以看[官方blog](https://blog.gskinner.com/archives/2020/07/introducing-flokk-a-desktop-app-built-with-flutter.html "官方blog")

![](https://imgkr.cn-bj.ufileos.com/5981df54-b95d-4b86-a2a3-a51a25a145fd.png)


[HatFeather/flutter_dough](https://github.com/HatFeather/flutter_dough "HatFeather/flutter_dough")

这个包提供了一些可拖动的UI小部件，让你的应用不再沉闷。

![](https://imgkr.cn-bj.ufileos.com/dc0b6492-c118-4e06-b5a5-2b65ffbe9b2d.gif)

![](https://imgkr.cn-bj.ufileos.com/02221bba-56c9-49a6-95f8-14e658e22272.gif)



[Abiri99/elastic-widgets](https://z.flutter.gallery/docs/modeling/ "Abiri99/elastic-widgets")

一套使用物理学动画构建的Flutter小部件。
![](https://imgkr.cn-bj.ufileos.com/3566a889-11b8-42cf-8c0c-30ba600ec9f6.gif)
![](https://imgkr.cn-bj.ufileos.com/ce2664de-8543-4332-8d09-5d4086fee9cb.gif)


### 订阅

感觉这期完全是动画专题呢。在应用中增加适当的动效，会使应用跟用户的距离拉近，更容易引起用户的情感共鸣。

这个周报每周五发布，同步更新在[个人博客](https://chyaohui.github.io/ "个人博客")和微信公众号。

微信搜索 “搞IT的陈爸爸” 或者扫描二维码，即可关注。

![](http://yp.3yi.ink/s/6b73fcf6f5790be13c4e75b8926d0c57)




