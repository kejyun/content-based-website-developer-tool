# Responsive Image srcset

使用 srcset 做圖片 lazyloading，並顯示適合裝置像素密度的圖片

一般螢幕的像素密度為 1 倍（163 dpi），同個長寬在畫面可以顯示 1x1 = 1 pixel 的像素

Retina 像素密度為 2 倍（326 dpi），同個長寬在畫面可以顯示 2x2 = 4 pixel 的像素

3 倍（401 dpi）的像素密度，同個長寬在畫面可以顯示 3x3 = 9 pixel 的像素

> PS: `401 dpi` 不為 `163 dpi` 的 3 倍，但還是視為 3 倍


寬高 100 px 的圖片到像素密度為 1 倍的螢幕，會將寬高 100px 圖片放到寬高為 100w *像素密度解析度* 的地方顯示，可以正常顯示

寬高 100 px 的圖片到像素密度為 2 倍的螢幕，會將寬高 100px 圖片放到寬高為 200w *像素密度解析度* 的地方顯示，等於是圖片解析度較低的圖片被撐大去顯示了，所以看起來會糊糊的

若放到像素密度為 3 倍的螢幕，則會被稱大到 300w 的 *像素密度解析度* 範圍去顯示，則會更加糊

所以比較好的螢幕像素密度，應該提供更高解析度的圖片去顯示，可以使用 `srcset` 去達到這樣的需求

```html
<img src="source.jpg" width="100%"
     srcset="source_400.jpg 400w,
            source_600.jpg 600w,
            source_1280.jpg 1280w"
/>
```

***source_400.jpg 400w***

圖片檔案寬度為 400px 的 `source_400.jpg` 檔案放到像 *像素密度解析度* 為 400w 的裝置顯示


***source_600.jpg 600w***

圖片檔案寬度為 600px 的 `source_600.jpg` 檔案放到像 *像素密度解析度* 為 600w 的裝置顯示

***source_1280.jpg 1280w***

圖片檔案寬度為 600px 的 `source_1280.jpg` 檔案放到像 *像素密度解析度* 為 1280w 的裝置顯示


## AMP 圖片 srcset

```html
<amp-img alt="Hummingbird"
  src="images/hummingbird-wide.jpg"
  width="640"
  height="457"
  layout="responsive"
  srcset="source_400.jpg 400w,
         source_600.jpg 600w,
         source_1280.jpg 1280w"
            >
</amp-img>
```

## 參考資料
* [响应式图片 - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)
* [用 srcset 屬性做簡單的 Responsive Image « The Front Row](http://blog.zhusee.in/post/248199/basic-responsive-image-with-srcset-property)
* [Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/#feat=srcset)
* [網頁和行動裝置介面設計的尺寸單位(二) – Syue Ming Yu – Medium](https://medium.com/@syuemingyu/%E7%B6%B2%E9%A0%81%E5%92%8C%E8%A1%8C%E5%8B%95%E8%A3%9D%E7%BD%AE%E4%BB%8B%E9%9D%A2%E8%A8%AD%E8%A8%88%E7%9A%84%E5%B0%BA%E5%AF%B8%E5%96%AE%E4%BD%8D-%E4%BA%8C-17dd1590a851)
* [iPhone 6 Plus downsampling artifacts explained](http://www.idownloadblog.com/2014/11/20/iphone-6-downsampling-explained/)
* [Retina顯示器 - 維基百科，自由的百科全書](https://zh.wikipedia.org/wiki/Retina%E6%98%BE%E7%A4%BA%E5%B1%8F)
* [Responsive images with srcset, sizes & heights – AMP](https://www.ampproject.org/docs/design/responsive/art_direction)
* [amp-img (Built-in) – AMP](https://www.ampproject.org/docs/reference/components/amp-img)
* [aFarkas/lazysizes: High performance and SEO friendly lazy loader for images (responsive and normal), iframes and more, that detects any visibility changes triggered through user interaction, CSS or JavaScript without configuration.](https://github.com/aFarkas/lazysizes)
