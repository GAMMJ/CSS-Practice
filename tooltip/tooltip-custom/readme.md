<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      /* container 설정 */
.container {
  display: flex;
  justify-content: center;
  flex-direction: row;
}

.inner-container {
  display: flex;
  flex-direction: column;
  width: 200px;
  text-align: center;
  margin-top: 50px;
}

/* 툴팁 기본 스타일  */

.tooltip {
  position: relative;
}

.tooltip .tooltiptext {
  visibility: hidden;
  width: 120px;
  background-color: black;
  color: #fff;
  border-radius: 6px;
  padding: 5px 0;
  text-align: center;

  position: absolute;
  z-index: 1;
}

.tooltip:hover .tooltiptext {
  visibility: visible;
}

/* 툴팁 화살표 기본 스타일 설정 시작 */

.tooltip .tooltiptext::after {
  content: "";
  position: absolute;
  border-style: solid;
  border-width: 5px;
}
/*끝*/

/* 툴팁 방향 설정 시작 */

/* 왼쪽 툴팁 */
.tooltip .tooltip-left {
  top: -5px;
  right: 70%;
}

.tooltip .tooltip-left::after {
  top: 50%;
  left: 100%;
  transform: translateY(-50%);
  border-color: transparent transparent transparent black;
}

/* 오른쪽 툴팁 */
.tooltip .tooltip-right {
  top: -5px;
  left: 70%;
}

.tooltip .tooltip-right::after {
  top: 50%;
  right: 100%;
  transform: translateY(-50%);
  border-color: transparent black transparent transparent;
}
/* 아래쪽 툴팁 */
.tooltip .tooltip-bottom {
  top: 130%;
  left: 50%;
  transform: translateX(-50%);
}

.tooltip .tooltip-bottom::after {
  bottom: 100%;
  left: 50%;
  transform: translateX(-50%);
  border-color: transparent transparent black transparent;
}

/* 위쪽 툴팁 */
.tooltip .tooltip-top {
  bottom: 130%;
  left: 50%;
  transform: translateX(-50%);
}

.tooltip .tooltip-top::after {
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
  border-color: black transparent transparent transparent;
}

/* 끝 */
    </style>
  </head>
  <body>
    <div class="container">

      <div class="inner-container">
        <div class="tooltip">(LEFT)
          <span class="tooltiptext tooltip-left">왼쪽 툴팁</span>
        </div>
    
        <br><br>
        
        <div class="tooltip">(RIGHT)
          <span class="tooltiptext tooltip-right">오른쪽 툴팁</span>
        </div>
    
        <br><br>
      
        <button class="tooltip">(TOP)
          <span class="tooltiptext tooltip-top">위쪽 툴팁</span>
        </button>
    
        <br><br>
    
        <button class="tooltip">(BOTTOM)
          <span class="tooltiptext tooltip-bottom">아래쪽 툴팁</span>
        </button>
    
      
    </div>
  </body>
</html>
