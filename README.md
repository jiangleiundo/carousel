## carousel
js原生面向对象的轮播图效果

### 注意事项

1. 设置自动轮播时调用clickHandle()发现 其中的this指向window。

   - 解决：在调用时绑定this，即 clickHandle.bind(this)

2.  如何实现无缝轮播

   - 2.1 将第一张图片克隆下来放到相框最后一个

   - 2.2 无缝轮播时，需要图片在短时间内跳转（第一图和最后一图之间），使用setTimeout()

     可实现先跳转好再完成下一步的动画。（注意：如果不使用setTimeout，跳转动画无法执行）