# 多重边框

> 背景知识: [box-shadow](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-shadow), [outline](https://developer.mozilla.org/zh-CN/docs/Web/CSS/outline),[outline-offset](https://developer.mozilla.org/zh-CN/docs/Web/CSS/outline-offset)

`box-shadow`用来给元素添加各种阴影效果(一个或多个)。  
参数:`inset | offset-x | offset-y | blur-radius | spread-radius | color`  
其中`spread-radius`阴影扩张半径，当只设置扩张半径时，零偏移，零模糊，产生的效果其实相当于一条实线“**边框**”


```css
div {
  width: 60px; 
  height: 60px;
  margin: 120px auto;
  border-radius: 50%;
  background: #fafafa;
  box-shadow: 0 0 0 15px #E8E2D6, 0 0 0 30px #E1D9C9,  
              0 0 0 45px #D9CFBB, 0 0 0 60px #D2C6AE,  
              0 0 0 75px #CABCA0, 0 0 0 90px #C3B393;
}
```
<div class="demo1">
  <div></div>
</div>

`box-shadow`只能模拟实线边框效果，某些情况下，我们可能需要生成虚线的边框效果，我们可以通过类似于`border`的描边`outline`和对应的描边偏移`outline-offset`来实现。

```css
div {
  width: 200px;
  height: 120px;
  margin: 0 auto;
  background: #efebe9;
  border: 5px solid #B4A078;
  outline: #B4A078 dashed 1px;
  outline-offset: -10px;
}
```
<div class="demo2">
  <div></div>
</div>

<style>
  .demo1, .demo2 {
    width: 100%;
  }
  .demo1 div {
    width: 60px; 
    height: 60px;
    margin: 120px auto;
    border-radius: 50%;
    background: #fafafa;
    box-shadow: 0 0 0 15px #E8E2D6, 0 0 0 30px #E1D9C9,  
                0 0 0 45px #D9CFBB, 0 0 0 60px #D2C6AE,  
                0 0 0 75px #CABCA0, 0 0 0 90px #C3B393;
  }
  .demo2 div {
    width: 200px;
    height: 120px;
    margin: 0 auto;
    background: #efebe9;
    border: 5px solid #B4A078;
    outline: #B4A078 dashed 1px;
    outline-offset: -10px;
  }
</style>

### 浏览器支持

<iframe src="https://caniuse.bitsofco.de/embed/index.html?feat=css-boxshadow&amp;periods=future_1,current,past_1,past_2,past_3&amp;accessible-colours=false" frameborder="0" width="100%" height="436px"></iframe>