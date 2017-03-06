### &是父级引用 &会被替换成父级选择器

### 默认情况
    .button{
      .black{
        background: black;
      }
    }
----
    .button .black {
      background: black; 
     }
### 使用&的好处
    .button{
      &.red{
        color: red;
      }
    }
----
    .button.red {
      color: red; 
     }