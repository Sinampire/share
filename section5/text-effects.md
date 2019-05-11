
# 常见的文字效果

> 背景知识: [text-shadow](https://developer.mozilla.org/zh-CN/docs/Web/CSS/text-shadow), [filter](https://developer.mozilla.org/zh-CN/docs/Web/CSS/filter)

<style>
  #demo {
    width: 100%;
  }
  #demo > div {
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-wrap: wrap;
  }
  #demo > div > h5 {
    width: 229px;
  }
  #demo > div > p {
    padding: 18px 28px;
    text-align: justify; 
    font-size: 26px;
  }
  #demo > div:nth-of-type(1) > p {
    background: hsl(40, 28.57% , 58.82%);
    color: hsl(40, 28.57% , 28.82%);
    text-shadow: 0 .03em .03em hsla(0,0%,100%,.8);
  }
  #demo > div:nth-of-type(2) > p {
    background: hsl(40, 28.57% , 28.82%);
    color: hsl(40, 28.57% , 58.82%);
    text-shadow: 0 .03em .03em black;
  }
  #demo > div:nth-of-type(3) > p {
    background: #b4a078;
    color: white;
    text-shadow:  0 0 2px hsl(40, 28.57% , 28.82%), 
                  0 0 2px hsl(40, 28.57% , 28.82%), 
                  0 0 2px hsl(40, 28.57% , 28.82%), 
                  0 0 2px hsl(40, 28.57% , 28.82%), 
                  0 0 2px hsl(40, 28.57% , 28.82%),
                  0 0 2px hsl(40, 28.57% , 28.82%), 
                  0 0 2px hsl(40, 28.57% , 28.82%), 
                  0 0 2px hsl(40, 28.57% , 28.82%),  
                  0 0 2px hsl(40, 28.57% , 28.82%);
  }
  #demo > div:nth-of-type(4) > p {
    background: hsl(40, 28.57% , 28.82%);
  }
  #demo > div:nth-of-type(4) > p a {
    background: hsl(40, 28.57% , 28.82%);
    color: white;
    transition: .5s;
    font-weight: 500;
    text-shadow: 0 0 .1em, 0 0 .3em;
  }
  #demo > div:nth-of-type(4) > p a:hover{
    animation: .8s text-blink-effect infinite alternate;
  }
  #demo > div:nth-of-type(5) > p {
    background: #b4a078;
    color: white;
    text-shadow:  0 1px hsl(0, 0%, 90%),
                  0 1px hsl(0, 0%, 90%), 
                  0 2px 4px hsla(0, 0%, 0%,.5); 
  }
  #demo > div:nth-of-type(6) > p {
    background: #b4a078;
    color: white;
    text-shadow:  1px 1px hsl(40, 28.57% , 28.82%), 2px 2px hsl(40, 28.57% , 28.82%),
                  3px 3px hsl(40, 28.57% , 28.82%), 4px 4px hsl(40, 28.57% , 28.82%);
  }
</style>

<div id="demo">
  <div>
    <h5>1️ 浅色底深色字</h5>
    <p>You-need-to-know-css-tricks</p>
  </div>
  <div>
    <h5>2️ 深色底浅色字</h5>
    <p>You-need-to-know-css-tricks</p>
  </div>
  <div>
    <h5>3️ 空心字:text-shadow</h5>
    <p>You-need-to-know-css-tricks</p>
  </div>
  <div>
    <h5>4 外发光文字:text-shadow</h5>
    <p><a>You-need-to-know-css-tricks</a></p>
  </div>
  <div>
    <h5>5 文字凸起</h5>
    <p>You-need-to-know-css-tricks</p>
  </div>
  <div>
    <h5>6 文字凸起</h5>
    <p>You-need-to-know-css-tricks</p>
  </div>
</div>


### 浏览器支持

<iframe src="https://caniuse.bitsofco.de/embed/index.html?feat=css-gradients&amp;periods=future_1,current,past_1,past_2,past_3&amp;accessible-colours=false" frameborder="0" width="100%" height="436px"></iframe>
