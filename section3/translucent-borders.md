# 半透明边框

> 背景知识: [background-clip](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-clip)

默认情况下，背景的颜色会延伸至边框下层，这意味着我们设置的透明边框效果会被覆盖掉，在css3中，我们可以通过设置`background-clip:padding-box`来改变背景的默认行为，达到我们想要的效果。


<style>
  #demo{
    width: 100%;
    padding: 60px 80px 80px;
    background: #b4a078;
  }
  #demo div{
    padding: 12px;
    margin: 20px auto;
    background: white;
    border: 10px solid hsla(0, 0%, 100%, .5);
  }
  #demo p{
    color: #f4f0ea;
  }
  #demo div.padding-box{
    background-clip: padding-box;
  }
  #demo div.border-box{
    background-clip: border-box;
  }
</style>

<div id="demo">
  <p>padding-box</p>
  <div class="padding-box">一段文字，吧啦吧啦吧啦。</div>
  <p>border-box</p>
  <div class="normal-box">一段文字，吧啦吧啦吧啦。</div>
</div>

### 浏览器支持

<iframe src="https://caniuse.bitsofco.de/embed/index.html?feat=background-img-opts&amp;periods=future_1,current,past_1,past_2,past_3&amp;accessible-colours=false" frameborder="0" width="100%" height="458px"></iframe>


