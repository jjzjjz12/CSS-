# 1.flex弹性布局

## 1.父元素属性

```css
1.display:flex;
/* 主轴 */
2.justify-content:flex-start|center|flex-end|space-between|space-around|space-evenly
/* 换行会有行间距，一般垂直排布不使用换行 */
3.flex-wrap:wrap|nowrap|wrap-reverse
/* 交叉轴针对一行 */
4.align-items:stretch|baseline|flex-start|center|flex-end
/* 交叉轴针对多行 */
5.align-content:flex-start|center|flex-end|space-between|space-around|space-evenly
/* 切换主轴，用于垂直排布子元素 */
6.flex-direction:row|column|……
7.gap:20px;
```

## 2.子元素属性

```css
/* 排列顺序，越大越前 */
1.order:0 1 2 3 4……
/* 单独控制某子项的布局位置 */
2.align-self:flex-start|center|flex-end
/* 有剩余空间会按照数字占比延申 */
3.flex-grow:0|1|2|……
/* 超出部分按数字占比压缩，默认1是全部子元素平均压缩超出部分 */
4.flex-shrink:1|2|……
/* 初始值,类似width，优先于width */
5.flex-basis:auto|100px|200px|……
/* 上面345缩写,g|s|b */
/* width=0所有空间都由flex-grow分配 */
/* 全部子元素都flex:1就是给所有子元素设置等宽分配一行 */
6.flex:1——>flex:1 1 0% 
```

**注意点：**
    1. 垂直布局时父元素切换主轴，justify-content等永远是主轴方向的属性，交叉轴一样。
    2. align-items默认是stretch会==占满交叉轴==
    3. 可以用定位元素做