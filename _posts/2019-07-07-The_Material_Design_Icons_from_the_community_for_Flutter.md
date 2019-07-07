---
layout: post
title:  Flutter社区的Material Design Icons
tag: [flutter, Icons, Material Design]
date: 2019-07-07
---

 


## [立即下载 ️⬇️ ](https://codeload.github.com/ziofat/material_design_icons_flutter/zip/master) 


 
![](https://flutterawesome.com/content/images/2019/07/Material-Design-Icons.jpg)
 
>
> 材料设计图标图标包可用作一组flutter图标。
>

 
# material_design_icons_flutter

The [Material Design Icons](https://materialdesignicons.com/) Icon pack available as set of Flutter Icons.

Based on Material Design Icons 3.6.95.

## Installation

In the `dependencies:` section of your `pubspec.yaml`, add the following line:

```yaml
  material_design_icons_flutter: 3.2.3695
```

## Usage

```dart
import 'package:material_design_icons_flutter/material_design_icons_flutter.dart';

class MyWidget extends StatelessWidget {
  Widget build(BuildContext context) {
    return new IconButton(
      // Use the MdiIcons class for the IconData
      icon: new Icon(MdiIcons.sword), 
      onPressed: () { print('Using the sword'); }
     );
  }
}
```

Or, if you want to access the icon by a string name, you can use `fromString` method to create one.

This is not recomended because to make `fromString` work we need a map for all icon names. Using this method will not get the benifits of tree-shaking.

```dart
import 'package:material_design_icons_flutter/material_design_icons_flutter.dart';

class MyWidget extends StatelessWidget {
  Widget build(BuildContext context) {
    return new IconButton(
      // Use the string name to access icons.
      icon: new Icon(MdiIcons.fromString('sword')), 
      onPressed: () { print('Using the sword'); }
     );
  }
}
```

## Name Conversion

Some icons' name is reversed keyword in Dart (and most other languages), so the names have been changed.

- `null` -> `nullIcon`
- `switch` -> `switchIcon`
- `sync` -> `syncIcon`
- `factory` -> `factoryIcon`

## Github主页 👉[ziofat/material_design_icons_flutter](http://github.com/ziofat/material_design_icons_flutter)