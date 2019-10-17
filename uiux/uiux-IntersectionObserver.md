# IntersectionObserver 元素偵測

透過瀏覽器內建的 `IntersectionObserver` 即可設定在網頁上的元素被使用者看到可以觸發函式，可以透過這些函式去對元素做互動


```js
let options = {
  root: document.querySelector('#scrollArea'),
  rootMargin: '0px',
  threshold: 1.0
}

let observer = new IntersectionObserver(observedCallback, options);


// 觀察到元素的 callback
function observedCallback(observeElementsCollectioin) {

}
```

## 參考資料
* [IntersectionObserver/polyfill at master · w3c/IntersectionObserver](https://github.com/w3c/IntersectionObserver/tree/master/polyfill)
* [Intersection Observer API - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API)
* [The Intersection Observer Threshold example - JSFiddle](https://jsfiddle.net/api/mdn/)
* [The Intersection Observer API - Arnelle’s Blog](https://blog.arnellebalane.com/the-intersection-observer-api-d441be0b088d)
* [Intersection Observer - Web API 接口参考 | MDN](https://developer.mozilla.org/zh-CN/docs/Web/API/IntersectionObserver)
* [russellgoldenberg/scrollama: Scrollytelling with IntersectionObserver.](https://github.com/russellgoldenberg/scrollama)
