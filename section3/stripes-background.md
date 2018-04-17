# 条纹背景

> 背景知识: [gradient](https://developer.mozilla.org/zh-CN/docs/Web/CSS/gradient), [linear-gradient](https://developer.mozilla.org/zh-CN/docs/Web/CSS/linear-gradient), [radial-gradient](https://developer.mozilla.org/zh-CN/docs/Web/CSS/radial-gradient), [repeating-linear-gradient](https://developer.mozilla.org/zh-CN/docs/Web/CSS/repeating-linear-gradient)

线性渐变`linear-gradient`是CSS3非常重要的一个模块，但在真实的开发中，我们并不常用，在这里，我举两个自己经常会用到的场景，分别是`进度条`和`不规则卡片`。

## 进度条

<div align="center"><img src="../image/progress.jpg" width="500" align="center"/></div>

<style>
  #demo1 {
    width: 100%;
    padding: 80px 0px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around; 
  }
  #demo1 .progress-outer {
    width: 60%; height: 12px;
    border-radius: 8px;
    overflow: hidden;
    position: relative; 
  } 
  #demo1 .progress-enter {  
    height: inherit;
    background: rgba(180, 160, 120, .2); 
  }
  #demo1 .progress-bg {
    width: 60%; 
    height: inherit;
    border-radius: 6px; 
    background: repeating-linear-gradient(-45deg, #D9CFBB  25%, #C3B393 0, #C3B393 50%,
          #D9CFBB 0, #D9CFBB 75%, #C3B393 0);
    background-size: 16px 16px;
    animation: panoramic 3s linear infinite;
  }
  @keyframes panoramic
  {
  0% {background-position: 0px;}
  100% {background-position: 50px;}
  }
</style>

<div id="demo1">
  <div class="progress-outer">
    <div class="progress-enter">
      <div class="progress-bg"></div>
    </div>
  </div>
</div>


## 不规则卡片

<div align="center"><img src="../image/coupon.jpeg" width="100%" align="center"/></div>


>卡片顶部凹进来的弧形我们可以通过径向渐变`radial-gradient`来实现

<style>
  #demo2 {
    width: 100%;
    padding: 60px 0px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around; 
  }
  #demo2 .coupon-card {
    width: 200px;
    height: 120px;
    background-image: radial-gradient(circle at 100px -8px, transparent 20px, #b4a078 21px);
  }
</style>

<div id="demo2">
  <div class="coupon-card"></div>
</div>



### 浏览器支持

<iframe src="https://caniuse.bitsofco.de/embed/index.html?feat=css-gradients&amp;periods=future_1,current,past_1,past_2,past_3&amp;accessible-colours=false" frameborder="0" width="100%" height="436px"></iframe>