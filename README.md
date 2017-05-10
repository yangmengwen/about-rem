# about-rem
## rem使用方法总结
### 什么是rem
>rem是css3的度量单位，是一个相对于根元素html的单位。
### 兼容性
>可兼容Mozilla Firefox 3.6+、Apple Safari 5+、Google Chrome、IE9+和Opera11+等大多数浏览器，至于IE8以前的可以忽略不计。
当然也可以这样解决浏览器兼容问题
```html
 example ：
 html {font-size:10px; font-size:.625rem;}
```
这样多写一个绝对单位的声明。这些浏览器会忽略用rem设定的字体大小
### 如何使用
>所有浏览器的默认字体大小是16px，如
```html
 html {
 font-size: 10px; // 将根字体大小设为10px
 } //10px ÷ 16px × 100% = 62.5%;
```
这样设置可以使1rem=10px 方便计算;
BUT，这样会有一个问题：谷歌浏览器支持的最小字体是12px,所以后面如果要设置非字体属性（如 div的rem）就会出现问题
一开始，我是为了解决这个问题就将根字体大小设为20px;
但是在使用过程中发现设置20px计算有点麻烦
于是，就改为
```html
html {
font-size: 100px;
font-size: 625%; // 也可以这样设置即（100 ÷ 16 × 100% = 625%）
}
```
这样后面的padding、margin、width、height、line-height都可以用rem作单位
 
### em 和 rem 的区别
 em 和 rem 都是相对单位，em是相对于父元素的大小，如果html 默认字体大小16px,若body{font-size: 50%}
则body里面的字体大小 1em = 8px ，em的值不是固定的取决于父级元素的大小。
rem 是相对于html根元素的大小，不受父级元素影响
