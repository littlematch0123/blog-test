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

CSS动画有两种实现方式： transition 和 animation

#### transition

过渡transition是一个复合属性，包括transition-property、transition-duration、transition-timing-function、transition-delay这四个子属性。通过这四个子属性的配合来完成一个完整的过渡效果

```
transition-property: 过渡属性(默认值为all)
transition-duration: 过渡持续时间(默认值为0s)
transiton-timing-function: 过渡函数(默认值为ease函数)
transition-delay: 过渡延迟时间(默认值为0s)
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