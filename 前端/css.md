
#### 常见问题

 -  a标签为行内元素，设置 **height** 属性无效，需要将a标签的display改为 **block** 或 **inline-block**


### css盒模型
### 字体
CSS 属性 `font-family` 允许您通过给定一个有先后顺序的，由字体名或者字体族名组成的列表来为选定的元素设置字体。
 
指定的是一个优先级从 **高** 到 **低** 的可选字体列表

``` css
# 语雀
body,html{
	font-family:Chinese Quote,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,PingFang SC,Hiragino Sans GB,Microsoft YaHei,Helvetica Neue,Helvetica,Arial,sans-serif;
	}
```


``` css
# element-ui网站
body,html{
	font-family: Helvetica Neue,Helvetica,PingFang SC,Hiragino Sans GB,Microsoft YaHei,SimSun,sans-serif；
	}

```

``` css
# 掘金
html{
font-family:-apple-system,system-ui,Segoe UI,Roboto,Ubuntu,Cantarell,Noto Sans,sans-serif,BlinkMacSystemFont,"Helvetica Neue","PingFang SC","Hiragino Sans GB","Microsoft YaHei",Arial;
}
```


``` css
# 知乎
body{
font-family:-apple-system,BlinkMacSystemFont,Helvetica Neue,PingFang SC,Microsoft YaHei,Source Han Sans SC,Noto Sans CJK SC,WenQuanYi Micro Hei,sans-serif;
}
```

``` css
# 思否
html,body{
 font-family:-apple-system,"Helvetica Neue",Helvetica,Arial,"PingFang SC","Hiragino Sans GB","WenQuanYi Micro Hei","Microsoft Yahei",sans-serif;
}

```

## Grid布局
采用网格布局的区域，称为"容器"（container）。容器内部采用网格定位的子元素，称为"项目"（item）。
``` markup
<div>
  <div><p>1</p></div>
  <div><p>2</p></div>
  <div><p>3</p></div>
</div>
```

上面代码中，最外层的`<div>`元素就是容器，内层的三个`<div>`元素就是项目。

指定容器采用网格布局
```css
div {
  display: grid;
}
```

注意，设为网格布局以后，容器子元素的下列属性设置都将失效
- float
- display: inline-block
- display: table-cell
- vertical-align
- column-*

#### 属性
##### grid-template-columns
>定义每一列的宽度

##### grid-template-rows
>定义每一行的行高

