## 自学Flutter时遇到的坑与解决办法，分享出来，希望能一起成长。
1. Stack布局中默认是没有宽高的，如果想撑满宽度，需要给left:0和right:0来将控件撑开
2. 使用NotificationListener可以监听ScrollView的滑动距离 通过scrollNotification.metrics.pixels来拿到
3. Swiper组件中的itemCount数量不能为0，切记，否则会报错：Failed assertion: line 110 pos 12: '_positions.isNotEmpty'
4. 将多次请求合并到一起去请求，使用Future.wait([getDelegationData(), getData()]);
5. Json转Bean，可以用一键格式化工具来搞定，地址https://javiercbk.github.io/json_to_dart/
6. 使用GridView的时候，动态设置item的高度可以用gridDelegate中的childAspectRatio来设置宽高比来搞
7. 使用Container来包裹一切内容，可以使用alignment来设置内容的对齐方式，如果使用坐标，记着左上角是（-1，-1） 右下角是 （1,1）
8. 想要加边框 圆角 背景 渐变色等 使用BoxDecoration来实现 Container就可以加
9. TabBar可以设置被选中的文字样式和未被选中的文字样式，还有下方的指示条的样式，很好用
10. 想要类似于relativelayout中的控件层叠效果，使用Stack+Positioned就可以办到，在Stack中可以指定元素的排列位置，例如alignment: Alignment.center，可以使元素在没有指定x轴坐标时自动居中，很好用
11. 想要圆角，只需要用ClipRRect包裹一下即可
12. 在flutter 中对 Expanded 使用 来平分布局占用比例（相当于Android里面的LinearLayout 控件中设置权重）。注意Expanded必须在Flex布局(也就是Row，Colum等布局中，在其他布局中会报错)
13. 计算屏幕的宽高 MediaQuery.of(_context).size.width, MediaQuery.of(_context).size.height
14. ScrollView中的primary 如果为 true，即使滚动视图没有足够的内容来支撑滚动，滚动视图也是可滚动的。否则，默认为 false 情况下，只有具有足够内容的用户才能滚动视图。
15. 使用ListView和GrideView的时候 高度不确定的时候 需要在builder中增加shrinkWrap: true属性
16. 要在环境变量中配置镜像，否则Flutter在启动过程中一些dependences下载不下来，会被墙。
17. 多行长文本使用'''  '''来包裹。如果用'  '的话会报错。
18. 使用Expand来解决放置不下的问题
19. Flexible widgets must be placed directly inside Flex widgets。出现的情况是在Column中放了两个高度未知的控件 导致高度计算出问题。解决办法：一个给定高度，一个去适应
20. 使用Wrap流式布局可以搞瀑布流等效果
21. Flutter中富文本使用RichText来实现同一段文字，不同效果
22. SnackBar：提示框，会在App下方出现，类似于Toast的感觉。
23. 
