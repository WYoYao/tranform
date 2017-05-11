
# transfrom 整理

> 相关引用的原文链接

[transfrom w3c](http://www.w3cplus.com/content/css3-transform)

[Transform-style和Perspective属性](http://www.w3cplus.com/css3/transform-basic-property.html)

[后面的补充](http://www.w3cplus.com/css3/css3-3d-transform.html)

**我们同时对一个元素进行transform的多种属性操作，例如rotate、scale、translate三种，但这里需要提醒大家的，以往我们叠加效果都是用逗号（“，”）隔开，但transform中使用多个属性时却需要有空格隔开。大家记住了是空格隔开。**

**在使用3D做旋转的时候注意，Z轴是一直垂直到面的，跟随旋转而变化**

[探究transform动画元素的z-index](https://aotu.io/notes/2015/10/21/z-index-and-translate3d/)

> transform 变换的时候会让 z-index “临时失效”，其实并非 z-index 失效了，只是 z-index 被用在不同的 stacking context 上，而非在默认的 context 上同等地比较层级了。所以 DOM 在 transform 的工程中，DOM 处于一个新的 stacking context 里，z-index 也是相对于这个 stacking context 的，所以表现出来的实际是 stacking context 的层次，动画一结束，DOM 又回到默认的 context 里，这时的 z-index 才是在同一个 context 上的比较。

**perspective 和 translate3d 能够影响 DOM 的层级了，它们在屏幕和镜头之间的距离不同，所以就有了层次**