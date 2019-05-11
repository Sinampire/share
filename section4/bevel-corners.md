# 切角效果

> 背景知识: [gradient](https://developer.mozilla.org/zh-CN/docs/Web/CSS/gradient)

<style>
  #demo{
    width: 100%;
    padding: 60px 0;
  }
  .bevel-corners{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    align-items: center;
    flex-wrap: wrap;
    margin-bottom: 20px;
  }
  .bevel-corners > div{
    width: 249px;
    color: #FFF;
    padding: 1.2em 1.8em;
    hyphens: auto;
    text-align: justify;
    background: #b4a078;
  }
  .bevel-corners > p{
    width: 116px;;
  }
  .bevel-corners:nth-of-type(1) > div{
    background: linear-gradient(45deg, transparent 12px, #b4a078 13px) bottom left, 
                linear-gradient(135deg, transparent 12px, #b4a078 13px) top left, 
                linear-gradient(-135deg, transparent 12px, #b4a078 13px) top right, 
                linear-gradient(-45deg, transparent 12px, #b4a078 13px) bottom right;
    background-size: 51% 51%;
    background-repeat: no-repeat;
  }
  .bevel-corners:nth-of-type(2) > div{
    background: radial-gradient(circle at bottom left, transparent 15px, #b4a078 16px) bottom left, 
                radial-gradient(circle at top left, transparent 15px, #b4a078 16px) top left, 
                radial-gradient(circle at top right, transparent 15px, #b4a078 16px) top right, 
                radial-gradient(circle at bottom right, transparent 15px, #b4a078 16px) bottom right;
    background-size: 51% 51%;
    background-repeat: no-repeat;
  }
</style>

<div id="demo">
  <div class="bevel-corners">
    <p>① linear-gradient</p>
    <div>A paragraph of filler text.La la la de dah de dah de dah de la.La la la de dah de dah de dah de la.La la la de dah de dah de dah de la.</div>
  </div>
  <div class="bevel-corners">
    <p>② radial-gradient</p>
    <div>A paragraph of filler text.La la la de dah de dah de dah de la.La la la de dah de dah de dah de la.La la la de dah de dah de dah de la.</div>
  </div>
</div>


### 浏览器支持

<iframe src="https://caniuse.bitsofco.de/embed/index.html?feat=css-gradients&amp;periods=future_1,current,past_1,past_2,past_3&amp;accessible-colours=false" frameborder="0" width="100%" height="436px"></iframe>
