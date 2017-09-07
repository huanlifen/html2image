## 使用场景

现在流行于朋友圈分享的一些活动页，经常会玩这样的一个功能：将诸如测试之类的结果页保存成图片分享至朋友圈，以此来吸引用户参与，提高活动的pv和uv。

## 如何做

一般来说有这两个技术步骤：
- html2canvas
- canvas2image

当需要连同html中跨域的图片一起转换时，需要增加一个base步骤：
- image proxy（因为canvas2image不支持跨域的图片, 本篇只是点到，不做展开）
- html2canvas
- canvas2image

首先需要将html转成canvas， 再接着将canvas转为图片，至此，用户用手机自带的功能长按就可以保存，当然你也可以自己做长按保存的功能，canvas2image 提供了保存成图片的api。