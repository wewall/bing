test GPG 

# Bing Pictures Interface | 必应壁纸接口
> :hammer: `Bing 壁纸 Api`重装上阵啦 :smile: http://bing.ioliu.cn

## 目前开放的壁纸接口：
 - `/v1{d,w,h,p,size,callback}` 返回今日的壁纸完整数据(`可选参数{d,w,h,p,size,callback}`)： 

    > 若指定参数`{w,h}` ，则直接返回图片

|参数名|类型|是否必要|备注|
|:----:|:---------:|:--------:|---|
|d|`Int`|否|自今日起第`d`天前的数据|
|w|`Int`|否|图片宽度|
|h|`Int`|否|图片高度|
|p|`Int`|否|`Page 页码`:第x页|
|size|`Int`|否|`Size 条数`:每页条数|
|callback|`String`|否|JSONP的回调函数名|

 - `/v1/rand{w,h,type,callback}` 返回随机的壁纸(`可选参数{w,h,type,callback}`)：

|参数名|类型|是否必要|备注|
|:----:|:---------:|:--------:|---|
|w|`Int`|否|图片宽度|
|h|`Int`|否|图片高度|
|type|`String`|否|返回值类型(`json`)|
|callback|`String`|否|JSONP的回调函数名|

- `/v1/blur{d,w,h,r}` 返回高斯模糊壁纸(`可选参数{d,w,h,r}`)：

|参数名|类型|是否必要|备注|
|:----:|:---------:|:--------:|---|
|d|`Int`|否|自今日起第`d`天前的数据|
|w|`Int`|否|图片宽度|
|h|`Int`|否|图片高度|
|r|`Int`|否|模糊半径(`1~50`)|

### **:warning:** `高斯模糊`接口目前只支持指定分辨率(`w,h`)的图片，具体分辨率如下：
```js
/**
 * 已知分辨率
 */
resolutions: [
    '1920x1200',
    '1920x1080',
    '1366x768',
    '1280x768',
    '1024x768',
    '800x600',
    '800x480',
    '768x1280',
    '720x1280',
    '640x480',
    '480x800',
    '400x240',
    '320x240',
    '240x320'
]
```

欢迎点评→[issue](https://github.com/xCss/bing/issues)