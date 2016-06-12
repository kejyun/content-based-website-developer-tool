# Youtube 播放器 Mobile Friendly

Youtube 原生播放器只能指定固定的寬高，在手機解析度較低時，常常會導致破版，可以用下列方法讓它自動隨遮手機解析度寬度縮放

## 加入 CSS

```css
/* Youtube Reflexive */
.vid-container {
    position: relative;
    padding-bottom: 50%;
    padding-top: 35px; height: 0; overflow: hidden;
}

.vid-container iframe,
.vid-container object,
.vid-container embed {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}
```

## 設定播放器 HTML

```html
<div class="vid-container">
    <iframe width="xxx" height="xxx" src="http://www.youtube.com/embed/(EMBED CODE)" frameborder="0"></iframe>
</div>
```

現在 Youtube 嵌入播放器就可以正常地隨著手機解析度大小縮放摟！


## 參考資料
* [How To Make YouTube Embed Videos Reflexive / Mobile Friendly – WebAtude – Internet Marketing Done Right!](http://www.webatude.com/how-to-make-youtube-videos-reflexive-and-mobile-friendly/)