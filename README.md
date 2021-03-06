# image-pdf

image-pdf 图片或文字信息转成PDF文件

## 功能点 Feature
* 支持图片 base64 方式
* 支持图片 src 方式
* 支持中文文字
* 支持分页，避免图片内容被截断
* 支持异步回调


### npm
```
npm install

npm run start

```

### script
```
<script src="index.js"></script>

const {imagePdf} = window.imagePdf
imagePdf(imagesData, 'title')
```

## 参数 Params
* @param {Array} images: [{
*  type 插入类型，image 图片类型，text 文字类型，page 新增一页。默认 image
*  data 插入内容，image 时可为 base64 信息，或 src 地址；text 时为文字内容
*  width 图片宽，图片信息为 src 时可不传
*  height 图片高
*  options: { 文字配置信息
*   fontSize: 文字大小, 默认16px
*   spacing: 间距，默认同5px
*   textIndent: 文字缩进, 单位px,默认0
*  }
* }],
* @param {String} title 下载pdf文件的名称
* @param {Object} options{ 配置信息
*   pagePadding: { // pdf 间距
*       width: 20,
*       height: 25
*   },
*   initFont: 设置中文支持，需引入'jspdf-font'插件，支持'SongtiSCBlack'字体
* }

## 返回 Return
```
imagePdf(imagesData, 'title').then(result => {
    console.log(result)
}, error => {
    console.log(error)
})
```# imageToPdf
