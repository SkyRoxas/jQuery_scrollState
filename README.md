# scrollState 滾動狀態bar

## Description :

於頁面上方加入物件來顯示頁面滾動軸的進度，以增加使用者體驗

## Options :

Name       | type   | default   | description
---------- | ------ | --------- | -------------------------
color      | string | '#4A8CB4' | 物件顏色
bold       | string | '4px'     | 物件粗細
index      | string | '100'     | 物件 z-index 屬性 值
transition | string | '1s'      | 物件 transition 屬性 值 （過度時間）

## Example :

### Basic

```
$('body').scrollState();
```

### Basic Options

```
$('body').scrollState({
    'color' : "#FF0000",
    'bold' : '5px',
    'index' : '200',
    'transition' : '1.5s'
  });
```

--------------------------------------------------------------------------------

## Function Description

### scrollEvent ()
滾動事件出發時執行

計算 ： （當前視窗高度 + 畫面滾動高度）/ 整個文件的高度 的百分比 賦予 scrollState bar 的寬度

```
   $animateWidth = ($(window).height() + $(window).scrollTop()) / $(document).height() * 100
```
