---
layout: post
title:  flutter loading 
tag: [flutter, Loading, Widgets]
date: 2019-07-07
---

 


## [立即下载 ️⬇️ ](https://codeload.github.com/CaiJingLong/flutter_load_widget/zip/master) 


 
![](https://flutterawesome.com/content/images/2019/06/flutter_load_widget.jpg)
 
>
> 全局加载插件，可通过简单配置使用。
>

 
# load

[![pub package](https://img.shields.io/pub/v/load.svg)](https://pub.dartlang.org/packages/load) [![GitHub](https://img.shields.io/github/license/Caijinglong/flutter_load_widget.svg)](https://github.com/caijinglong/flutter_load_widget)

Global loading widget, which can be used through simple configuration.

Pure flutter library, not use native code.

It is similar to [OKToast](https://pub.dev/packages/oktoast) in use.

- [load](#load)
  - [ScreenShot](#screenshot)
  - [Usage](#usage)
  - [Advanced Usage](#advanced-usage)
    - [Custom Loading Widget](#custom-loading-widget)
    - [Custom some config](#custom-some-config)

## ScreenShot

![Screenshot_2019-05-21-14-08-42-731_com.example.ex.png](https://raw.githubusercontent.com/kikt-blog/image/master/img/Screenshot_2019-05-21-14-08-42-731_com.example.ex.png)

## Usage

- install

Add to yaml

version is ![pub package](https://img.shields.io/pub/v/load.svg)

```yaml
dependencies:
  load: $latest_version
```

- import

```dart
import 'package:load/load.dart';
```

- wrap your application

```dart
void main() {
  runApp(
    LoadingProvider(
      child: MyApp(),
    ),
  );
}

or

LoadingProvider(
  child: MaterialApp(),
);
```

see example/lib/main.dart

- show or hide dialog

```dart
showLoadingDialog();
showCustomLoadingWidget(Container()); // custom dialog
hideLoadingDialog();
```

## Advanced Usage

### Custom Loading Widget

Using `LoadingThemeData` and `loadingWidgetBuilder`

```dart
LoadingProvider(
    loadingWidgetBuilder: (ctx, data) {
    return Center(
        child: SizedBox(
        width: 30,
        height: 30,
        child: Container(
            child: CupertinoActivityIndicator(),
            color: Colors.blue,
        ),
        ),
    );
    },
    child: MyApp(),
),
```

![image](https://i.loli.net/2019/05/21/5ce3acaed3a8d92031.png)

### Custom some config

All params is optional

| Params                 | Type       | Default Value               | Desc                                           |
| ---------------------- | ---------- | --------------------------- | ---------------------------------------------- |
| backgroundColor        | Color      | Colors.black54              | Background transparent mask                    |
| tapDismiss             | bool       | true                        | Will it close when touching the background?    |
| loadingBackgroundColor | Color      | Colors.white                | Background color for the center Loading Widget |
| loadingPadding         | EdgeInsets | EdgeInsets.all(8.0)         | Padding for the center Loading Widget          |
| loadingSize            | Size       | Size(55,55)                 | Size for the center Loading Widget             |
| animDuration           | Duration   | Duration(milliseconds: 300) | Show/Hide Time Duration                        |

## Github主页 👉[CaiJingLong/flutter_load_widget](http://github.com/CaiJingLong/flutter_load_widget)