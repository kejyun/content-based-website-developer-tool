# Ckeditor

* 官方網站：http://ckeditor.com/
* 目前版本：4.7.1

## 安裝

```
bower install ckeditor --save
```

## 初始化

載入 `ckeditor.js`

```html
<script src="../ckeditor.js"></script>
```

初始化需要 ckeditor 元素（by element id），將要初始化的元素編號帶入 `CKEDITOR.replace( ELEMENT_ID );`

```html
<textarea name="editor1" id="editor1" rows="10" cols="80">
    This is my textarea to be replaced with CKEditor.
</textarea>
<script>
    // Replace the <textarea id="editor1"> with a CKEditor
    // instance, using default configuration.
    CKEDITOR.replace( 'editor1' );
</script>
```

## 延伸設定

在初始化時，將設定帶入後方參數即可

```javascript
CKEDITOR.replace( 'editor1', {
    customConfig: ''
});
```

## 取得元素資料

初始化後，Ckeditor 會將資源存放在 `CKEDITOR.instances`，並依照傳入的 `ELEMENT_ID` 去存放，所以可以透過存取 `CKEDITOR.instances` 中的 `ELEMENT_ID` 物件去取得資料

```javascript
var data = CKEDITOR.instances.editor1.getData();
```

## 參考資料
* [Quick Start Guide - CKEditor 4 Documentation](http://docs.ckeditor.com/#!/guide/dev_installation)
