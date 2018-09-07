# flex demo

## 基本规则

1. flex 容器
    ```
    flex-flow
        flex-direction || row
        flex-wrap || nowrap
    justify-content || flex-start
    align-items || stretch
    align-content || stretch
    ```

1. flex 项目
    ```
    flex
        flex-grow || 0
        flex-shrink || 1
        flex-basis || auto
    order || 0
    align-self || 覆盖 align-items
    ```

1. 使用复合属性
    ```
    // 容器属性
    flex-flow
    justify-content
    align-items
    align-content || 多行时的排列

    // 项目属性
    flex
    order
    align-self
    ```

1. flex 复合简写属性
    ```
    flex: initial;    // 0  1  atuo
    flex: none;       // 0  0  auto
    flex: auto;       // 1  1  auto
    flex: 1;          // 1  1  0%
    flex: 4;          // 4  1  0%
    ```

1. flex-grow 扩展比率
    ```
    默认值：0，表示不扩展。
    当 "主轴宽-子项基准值和" M>0 时有效，flex-shrink 无效。
    每个子项的实际宽 = basis + 扩展宽。

    // 实例
    .flex {display:flex; width:1000px;}
    .flex:nth-child(1) {flex:1 4 200px;}   扩展宽度为: 1/(1+2+3)*100px
    .flex:nth-child(2) {flex:2 5 300px;}   扩展宽度为: 2/(1+2+3)*100px
    .flex:nth-child(3) {flex:3 6 400px;}   扩展宽度为: 3/(1+2+3)*100px
     ```

1. flex-shrink 收缩比率
    ```
    默认值：1，表示按原大小放缩。
    当 "主轴宽-子项基准值和" M<0 时有效，flex-grow 无效。
    每个子项的实际宽 = basis - 缩减宽。

    // 实例
    .flex {display:flex; width:600px;}
    .flex:nth-child(1) {flex:1 4 300px;}   缩减宽度为: 4*300/(4*300+5*200+6*400)*300px
    .flex:nth-child(2) {flex:2 5 200px;}   缩减宽度为: 5*200/(4*300+5*200+6*400)*300px
    .flex:nth-child(3) {flex:3 6 400px;}   缩减宽度为: 6*400/(4*300+5*200+6*400)*300px
    ```

1. flex 使用注意
    ```
    设为 flex 布局以后，子元素的 float、clear、vertical-align 属性将失效。

    当 flex 为多行效果，align-content 属性生效。

    flex-direction 为 row 时：Main-Axis 方向是从左到右，Cross-Axis 方向是从上到下；
    flex-direction 为 column 时：Main-Axis 方向是从上往下，Cross-Axis 方向是从右往左。

    当flex横向分均排列子项目时，
        在第一项设置（margin-right:auto;）就会将整行多余的margin放在第一项后面；
        在第一项后面设置（margin-left:auto; margin-right:auto;）可以将第一项居中。
    ```


## flex 实例
1. [筛子九点](https://yuwl798180.github.io/flexdemo/example/dice.html)
1. [圣杯布局](https://yuwl798180.github.io/flexdemo/example/HolyGrail.html)
1. [纯flex布局音乐盒](https://yuwl798180.github.io/flexdemo/example/musicapp.html)
