Language: [English](https://github.com/flutterchina/nine_grid_view) | 中文简体

[![Pub](https://img.shields.io/pub/v/nine_grid_view.svg?style=flat-square&color=009688)](https://pub.dartlang.org/packages/nine_grid_view)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[![Pub](https://img.shields.io/pub/v/nine_grid_view.svg?style=flat-square&color=2196F3)](https://pub.flutter-io.cn/packages/nine_grid_view)

### NineGridView
类似微博动态，微信朋友圈，展示图片的九宫格控件。支持单张大图预览。  
同时也支持微信群组，钉钉群组头像效果。

### DragSortView
类似微博/微信发布动态选图九宫格。支持按压放大效果，拖拽排序，拖拽到指定位置删除。

### Pub
```yaml
dependencies:
  nine_grid_view: ^1.0.0
```

### Example
```yaml
import 'package:nine_grid_view/nine_grid_view.dart';

NineGridView(
  margin: EdgeInsets.all(12),
  padding: EdgeInsets.all(5),
  space: 5,
  type: NineGridType.weChatGp,
  itemCount: itemCount,
  itemBuilder: (BuildContext context, int index) {},
);

DragSortView(
  imageList,
  space: 5,
  margin: EdgeInsets.all(20),
  padding: EdgeInsets.all(0),
  itemBuilder: (BuildContext context, int index) {},
  initBuilder: (BuildContext context) {},
  onDragListener: (MotionEvent event, double itemWidth) {
    /// 判断拖动到指定位置删除
    /// return true;
    if (event.globalY > 600) {
      return true;
    }
    return false;
  },
);     
```

### Screenshots

截图无法查看？  
掘金地址：[Flutter 九宫格](https://juejin.im/post/5ebd74b5f265da7bbd2f9aa6)  
简书地址：[Flutter 九宫格](https://www.jianshu.com/p/0f761fe6ad66)

|<img src="screenshots/nine_grid_view1.jpg" width="260" height="513"/>|<img src="screenshots/nine_grid_view2.jpg" width="260" height="513"/>|<img src="screenshots/nine_grid_view3.jpg" width="260" height="513"/>|
|:---:|:---:|:---:|
|<img src="screenshots/nine_grid_view4.jpg" width="260" height="513"/>|<img src="screenshots/nine_grid_view5.jpg" width="260" height="513"/>|<img src="screenshots/nine_grid_view6.jpg" width="260" height="513"/>|
|<img src="screenshots/nine_grid_view7.jpg" width="260" height="513"/>|<img src="screenshots/nine_grid_view8.jpg" width="260" height="513"/>|<img src="screenshots/nine_grid_view9.gif" width="220" height="465"/>|

### App
本组件来源于Flutter仿微博客户端[Fitness](https://github.com/Sky24n/Fitness)。  
百度云盘：[提取码 ttbn](https://pan.baidu.com/s/1HgBaR68oJYe7nnOTJlSg0Q)  
腾讯微云：[点击下载](https://share.weiyun.com/5T2hhs8c)  
请使用微信或QQ浏览器扫码下载！

![](https://upload-images.jianshu.io/upload_images/13222938-0bcbf2ba5a046d25.png)

### Others

另外一个[NineGridView](https://github.com/flutterchina/flukit)在 [flukit](https://github.com/flutterchina/flukit) UI组件库里面，通过封装GridView实现。本项目使用的Stack + Positioned实现。