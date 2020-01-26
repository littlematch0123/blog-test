# CSS 知识总结

### 浏览器渲染原理

1、根据 HTML 构建 HTML 树 (DOM)

2、根据 CSS 构建 CSS 树 (CSSOM)

3、将两棵树合并成一棵渲染树 (render tree)

4、layout 布局 (文档流、盒模型、计算大小和位置)

5、paint 绘制 （把边框颜色、文字颜色、阴影等画出来）

6、compose 合成 (根据层叠关系展示画面)

### CSS 动画

动画其实是一个人脑的bug，是由很多个静止不同的图片，加速播放，让人看起来是在不停播放的视觉效果

动画由许多静止的画面 (帧)，以一定的速度(如每秒30张) 连续播放时，肉眼因视觉残象产生错觉，而误以为是活动的画面

CSS动画有两种实现方式： transform + transition 和 animation

#### transform

CSS变形transform是一些效果的集合，主要是移动、旋转、缩放和倾斜这四种基本操作，还可以通过设置matrix矩阵来实现更复杂的效果。变形transform可以实现2D和3D两种效果。2D变形涉及的属性主要有transform变形函数和transform-origin变形原点

```
<transform-function>: translate | scale | rotate | skew | matrix
```

#### animation

animation 是通过关键帧 @keyframes 来实现更为复杂的动画效果

animation是一个复合属性，包括animation-name、animation-duration、animation-timing-function、animation-delay、animation-iteration-count、animation-direction、animation-play-state、animation-fill-mode共8个子属性

```
animation-name: 动画名称(默认值为none)
animation-duration: 持续时间(默认值为0)
animation-timing-function: 时间函数(默认值为ease)
animation-delay: 延迟时间(默认值为0)
animation-iteration-count: 循环次数(默认值为1)
animation-direction: 动画方向(默认值为normal)
animation-play-state: 播放状态(默认值为running)
animation-fill-mode: 填充模式(默认值为none)
```