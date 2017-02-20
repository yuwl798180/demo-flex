# flexdemo

## 基本规则

1. flex 容器
    ```
    flex-flow
    flex-direction
    flex-wrap
    justify-content
    align-items
    align-content
    ```

1. flex 项目
    ```
    flex
    flex-grow
    flex-shrink
    flex-basis
    order
    align-self
    ```

1. 使用复合属性
    ```
    // 容器属性
    flex-flow
    justify-direction
    align-items
    align-content    // 多行时的排列

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
    ```

1. flex-grow 扩展比率
    ```
    默认值：0，表示不扩展。
    当项目 basis 总和超过容器宽，grow 无效。
    当项目 basis 总和小于容器宽，剩余空间按比例分配；不设置值（即0）不分配。
     ```

1. flex-shrink 收缩比率
