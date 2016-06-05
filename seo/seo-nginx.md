# Nginx

## Gzip

| 參數  |  說明 |
|---|---|
| gzip on | on = enable, off = disable  |
| gzip_buffers 16 8k | 壓縮回應內容  |
| gzip_comp_level 6 | 壓縮等級，可設定 1 ~ 9 的整數，數字越大表示壓縮的量越大，也越吃資源，請看個人環境而定  |
| gzip_disable "msie6" | 設定不壓縮的條件，視 Request Header 中的 User-Agent 而定。可以設定 Regular Expression，例如: msie[4-6]  |
| gzip_min_length 1k | 文件內容小於 n 以下不壓縮，這裡的文件內容指的是 Response Header 的 Content-Length，一樣視個人需求而定，沒有標準值  |
| gzip_http_version 1.1 | 設定至少接受的 Http Version  |
| gzip_proxied any | 決定對來自 Proxy 的 Request 如何處理  |
| gzip_types [mime-types] | 指定需要壓縮的 MIME types，或用 * 表示所有 MIME types |
| gzip_vary on | 要不要在 Response Header "Vary: Accept-Encoding" |

### Example

```
http {
    gzip on;
    gzip_min_length 1000;
    gzip_types  *;
    gzip_comp_level 6;
    gzip_proxied any;
    gzip_buffers 16 8k;
    gzip_http_version 1.1;
}
```


## 參考資料
* [Enable gzip compression with nginx](http://blog.norman-chen.me/post/16)