# Wordpress Nginx


## wp-content 重新導向整個目錄至子網域（subdomain）

若網站做改版，不再用 Wordpress 時，Wordpress 中的圖片可以使用 Nginx 做重新導向，在 Nginx 設定檔設定下方轉址方式即可

```
server {
    rewrite ^(/wp-content/uploads)(.*)$ https://assets.kejyun.com$2 permanent;
}
```

## 參考資料
* [wordpress - Nginx redirect 301 the entire content of the folder to a subdomain - Stack Overflow](https://stackoverflow.com/questions/34234008/nginx-redirect-301-the-entire-content-of-the-folder-to-a-subdomain)
