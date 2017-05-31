# SVG
学习SVG相关知识的总结笔记

### 描边动画
#### 主要思路
使用path对象的`getTotalLength`方法获取path对象的长度，然后，设置`stroke-dasharray`和`stroke-dashoffset`属性值等于path对象的长度。然后，利用动画特性，逐渐改变`stroke-offseet`属性值直到`0`。

#### 代码片段
```javascript
var length = strokeRect.getTotalLength();
strokeRect.attr({'stroke-dasharray': length,'stroke-dashoffset':length});
Snap.animate(length, 0, function(val){
    strokeRect.attr({'stroke-dashoffset':val});
  }, 2000, mina.easeinout(), null
);
```
### 效果截图


