# slideunlock  一个用于登录校验，基于jquery的滑动解锁插件
> 本插件在slideunlock的基础上，修复了抖动，灵敏度等问题，使用方法和slideunlock一样
---
## 效果如下：
![img]https://ooo.0o0.ooo/2017/06/27/59523baf8bdd5.gif[/img]
---
## 使用方法如下：
1. 首先引入jquery，然后引入本插件
2. body中插入以下代码
```
<div id="slider">
    <div id="slider_bg"></div>
    <span id="label" class='slider'></span>
    <span id="labelTip">往右拖动验证</span>
</div>
```
3. style中插入以下代码
```
/*滑块*/

    #slider {
        width: 300px;
        height: 36px;
        position: relative;
        text-align: center;
        user-select: none;
        -moz-user-select: none;
        -webkit-user-select: none;
        border-radius: 18px;
    }

    #slider_bg {
        position: absolute;
        left: 0;
        top: 0;
        background-color: #dbf2ed;
        z-index: 1;
    }

    #label {
        width: 50px;
        position: absolute;
        left: 0;
        top: 0;
        z-index: 3;
        cursor: pointer;
    }

    #labelTip {
        position: absolute;
        left: 0;
        width: 100%;
        font-size: 14px;
        color: #fff;
        line-height: 36px;
        text-align: center;
        z-index: 2;
    }
```

4. js中调用插件方法
```
$(document).ready(function(){
  this.slider = new SliderUnlock("#slider",{
      successLabelTip : "验证通过"
  },function(){
      _this.test = true;
  });
  this.slider.init();
});

```

