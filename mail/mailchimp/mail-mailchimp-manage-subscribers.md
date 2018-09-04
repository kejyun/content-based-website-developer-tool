# 管理訂閱者


## 訂閱者狀態


| 狀態 | 說明  |
|---|---|
| subscribed | 訂閱，可以寄送電子信給此 email  |
| unsubscribed | 解除訂閱，email 在清單中，但無法寄送電子信給此 email  |
| pending | 等待，此 email 尚未確認是否訂閱，等待二階段確認  |
| cleaned | 清除，此 email 已被從清單中移除  |

## 刪除

> We don’t typically recommend deleting addresses from your list because it’s permanent and cannot be undone. It’s better to change its status to unsubscribed or cleaned.

不建議使用刪除，刪除會將 email 永久移除，建議用 `unsubscribed` 或 `cleaned`

## 參考資料
* [Developer | MailChimp](https://developer.mailchimp.com/documentation/mailchimp/guides/manage-subscribers-with-the-mailchimp-api/)
