### 清除浮动

#### clear-float1: after + zoom

```css
/* IE6-IE7 */
.parent {
  zoom: 1;
}

/* IE8以上 + !IE */
/* IE8以上和非IE浏览器才支持:after */
.parent:after {
  display: block;
  clear: both;
  content: '';
  visibility: hidden;
  height: 0;
}
```

#### clear-float2: 末尾 br + clear

```css
.parent br:last-child {
  display: block;
  clear: both;
  content: '';
  visibility: hidden;
  height: 0;
}
```

#### clear-float3: 末尾空 div + clear

```css
.parent div:last-child {
  display: block;
  clear: both;
  content: '';
  visibility: hidden;
  height: 0;
}
```

#### clear-float4: 父级 div 定高

```css
.parent {
  height: 200px;
}
```

#### clear-float5: 父级 div 定宽 + 溢出隐藏或滚动

必须定义 width 或 zoom:1，同时不能定义 height，使用 overflow:hidden | auto 时，浏览器会自动检查浮动区域的高度

```css
.parent {
  width: 98%;
  overflow: hidden;
  /* overflow: auto; */
}
```

#### clear-float6: 父级 div 浮动

```css
.parent {
  width: 99%;
  float: left;
}
.div2 {
  clear: both;
}
```

#### clear-float7: 父级 table 布局

```css
.parent {
  width: 99%;
  display: table;
}
```
