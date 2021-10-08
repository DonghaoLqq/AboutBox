# 模型盒子

总共分为两种盒模型：
* ## 内容盒子（W3C盒子）
  
  box-sizing:content-box;
  
  内容盒子是默认的，盒子里面的内容 = width
  
  实际的盒子宽度就是：内容宽度 + width + padding + border + margin

    ![3wc模型盒子](/w3cbox.jpg)

* ## 边框盒子（IE盒子）
  
  box-sizing:border-box;

  边框盒子需要通过代码进行转化，更方便程序员方便使用

  实际的盒子宽度：内容宽度+ width + padding + border + margin

    ![3wc模型盒子](/iebox.jpg)

## 问题
在布局的时候，盒子之间会出现margin塌陷重叠问题（上下关系）

### 解决方法：
* 父元素指定上边框

``` css
father{ 
    border-top:1px solid transparent;
}
```

* 父元素指定上边距

``` css
father{
    padding-top:1px;
}
```

* 父元素指定 overload
  
``` css
father{
    overload:hidden;
}
```
* 子元素转换成inline-block（不建议使用）

``` css
child{
    display:inline-block;
}
```

* 其他方法：float 、absolute 、fixed 也可解决