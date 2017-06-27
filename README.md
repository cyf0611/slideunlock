# slideunlock  一个用于登录校验，基于jquery的滑动解锁插件
> 说明：本插件在slideunlock的基础上，修复了抖动，灵敏度等问题，使用方法和slideunlock一样。除此之外，你可利用本插件改编一个类似于拖动滑块，组合图片的验证方式
---
## 效果如下：
下图是一个gif图片，加载速度可能比较慢


![](https://ooo.0o0.ooo/2017/06/27/59523baf8bdd5.gif)
---
## 使用方法如下：
**1. 首先引入jquery，然后引入本插件，注意：最好使用高版本的jq（项目附带的那个即可），低版本的可能会出现一些bug**

**2. body中插入以下代码**
```
<div id="slider">
    <div id="slider_bg"></div>
    <span id="label" class='slider'></span>
    <span id="labelTip">往右拖动验证</span>
</div>
```
**3. style中插入以下代码**
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
        height: 36px;
        width: 50px;
        border-radius: 18px;
        background-color: #4db4f2;
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

**4. js中调用插件方法**
```
$(function () {
    var slider = new SliderUnlock("#slider",{
        successLabelTip : "验证通过"
    },function(){
        //此处是验证成功之后执行的代码
    });
    slider.init();
});

```

