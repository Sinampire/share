# 专业术语

```css
.container {
  width: 100%;
  height: 1000px;
  color: transparent;
}
```

#### 1. 属性
> 属性对应的是平常我们书面或交谈时对 CSS 的中文称谓。  
例如，上面示意代码中的 height 和 color 就是属性。  
当我们说起“这个元素高度是100像素”，或者“这个文字颜色是透明色”时，  
这里提到的“高度”和“颜色”就是CSS的属性。

#### 2. 值
> “值”大多与数字挂钩。  
例如，上面的 1000px 就是典型的值。在 CSS 世界中，值的分类非常广泛，下面是一些常用的类型。  
• 整数值，如 z-index: 1 中的 1。  
• 数值，如 line-height: 1.5 中的 1.5。  
• 百分比值，如 padding: 50%中的 50%。  
• 长度值，如 width: 99px。  
• 颜色值，如 color: #999。  

此外，还有字符串值、位置值等类型。在 CSS3 中，还有角度值、频率值、时间值 等类型，这里就不全部展示了。

#### 3. 关键字
> 顾名思义，关键字指的是 CSS 里面很关键的单词,  
上面示例CSS代码中的transparent就是典型的关键字，还有常见的 solid、inherit 等都是关键字，其中 inherit 也称作“泛关键字”，所谓泛关键字，就是“所有CSS属性都可以使用的关键字”的意思。

#### 4. 变量
> CSS 中目前可以称为变量的比较有限，CSS3 中的 currentColor 就是变量，非常有用。  
currentColor顾名思意就是“当前颜色”，准确讲应该是“当前的标签所继承的文字颜色”

<style>
  .demo i.icon {
    display: inline-block;
    width: 16px;
    height: 20px;
    background-image: url(../image/sprite_icons.png) !important;
    background-color: currentColor;
  }
  .demo i.icon1 { background-position: 0 0; }
  .demo i.icon2 { background-position: -20px 0; }
  .demo i.icon3 { background-position: -40px 0; }
  .demo i.icon4 { background-position: -60px 0; }
  .demo .link { margin-right: 15px; color: #000;}
</style>
<p class="demo-color">
  <input type="color" name="color"/>
</p>
<p class="demo">
  <a href="javascript:;" class="link"><i class="icon icon1"></i>返回</a>
  <a href="javascript:;" class="link"><i class="icon icon2"></i>刷新</a>
  <a href="javascript:;" class="link"><i class="icon icon3"></i>收藏</a>
  <a href="javascript:;" class="link"><i class="icon icon4"></i>展开图片</a>
</p>
<!-- jquery -->
<script type="text/javascript" src="http://s8.pdim.gs/static/a5edbc346f719dbe.js"></script>
<script type="text/javascript">
  $('.demo-color input[name="color"]').on('change', function() {
    $('.demo .link').css('color', $(this).val());
  })
</script>

#### 5. 长度单位
> CSS中的单位有时间单位(如 s、ms)，还有角度单位(如 deg、rad 等)，最常见的自然还是长度单位(如 px、em 等)  
需要注意的是，诸如 2% 后面的百分号%不是长度单位。  
因为 2% 就是一个完整的值，就是一个整体，可以理解为0.02，故2%也同样是值。  
如果继续细分，长度单位又可以分为相对长度单位和绝对长度单位。  
(1)相对长度单位————相对长度单位又分为相对字体长度单位和相对视区长度单
• 相对字体长度单位，如 em 和 ex，还有 CSS3 新世界的 rem 和 ch(字符 0 的宽度)。  
• 相对视区长度单位，如 vh、vw、vmin 和 vmax。  
(2)绝对长度单位————最常见的就是 px，还有 pt、cm、mm、pc 等。

#### 6. 功能符
> 值以函数的形式指定(就是被括号括起来的那种)，主要用来表示颜色(rgba 和 hsla)、 背景图片地址(url)、元素属性值、计算(calc)和过渡效果等，如 rgba(0,0,0,.5)、 url('css-world.png')、[attr('href')](http://www.runoob.com/try/try.php?filename=trycss_func_attr)和 scale(-1)。

#### 7. 属性值
> 属性冒号后面的所有内容统一称为属性值。例如，1px solid rgb(0,0,0)就可以称为属性值，  
它是由“值+关键字+功能符”构成的。属性值也可以由单一内容构成。例如，z-index:1 的 1 也是属性值。

#### 8. 声明 
属性名加上属性值就是声明，例如:
```css
color: transparent;
```

#### 9. 声明块 
声明块是花括号({})包裹的一系列声明，例如:
```css
{
  height: 99px;
  color: transparent;
}
```

#### 10. 规则或规则集 
出现了选择器，而且后面还跟着声明块，比下这个例子，就是一个规则集:
```css
.container {
  height: 99px;
  color: transparent;
}
```

#### 11. 选择器
选择器是用来瞄准目标元素的东西，例如，上面的.container就是一个选择器。
> 类选择器: 指以“.”这个点号开头的选择器。很多元素可以应用同一个类选择器。“类”，
天生就是被公用的命。  
> ID选择器: “#”打头，权重相当高。ID 一般指向唯一元素。但是，在 CSS 中，ID
样式出现在多个不同的元素上并不会只渲染第一个，而是雨露均沾。但显然不推荐
这么做。  
> 属性选择器: 指含有[]的选择器，形如[title]{}、[title= "css-world"]{}、
[title~="css-world"]{} 、 [title^= "css-world"]{} 和 [title$="css-
world"]{}等。  
> 伪类选择器: 一般指前面有个英文冒号(:)的选择器，如:first-child 或:last-
child 等。  
> 伪元素选择器: 就是有连续两个冒号的选择器，如::first-line::first-
letter、::before 和::after。

#### 12. 关系选择器 
> 关系选择器是指根据与其他元素的关系选择元素的选择器。  
• 后代选择器:选择所有合乎规则的后代元素。空格连接。  
• 相邻后代选择器:仅仅选择合乎规则的儿子元素，孙子、重孙元素忽略，因此又称“子
选择器”。>连接。适用于 IE7 以上版本。  
• 兄弟选择器:选择当前元素后面的所有合乎规则的兄弟元素。~连接。适用于 IE7 以上
版本。  
• 相邻兄弟选择器:仅仅选择当前元素相邻的那个合乎规则的兄弟元素。+连接。适用于
IE7 以上版本。 

#### 13. @规则
> @规则指的是以@字符开始的一些规则，像@media、@font-face、@page 或者@support， 诸如此类。
