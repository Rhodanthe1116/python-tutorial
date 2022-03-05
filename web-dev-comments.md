# 網站開發 - 留言板

## 網頁原理

![](<.gitbook/assets/image (120) (1).png>)

* 請求Request
* 回應 Response

## 伺服器

Repl.it

可以提供免費的伺服器，方便的開發環境（寫程式的地方）

[https://replit.com/@hwchang/fastapi-template](https://replit.com/@hwchang/fastapi-template)

## 模板

使用 Python 以及我預先寫好的網頁模板來完成一個線上留言板

完成範例：[https://fastapi-template.hwchang.repl.co/](https://fastapi-template.hwchang.repl.co)

模板：[https://replit.com/@hwchang/fastapi-template](https://replit.com/@hwchang/fastapi-template)

這個模板已經寫好很多東西了，都是用Python來處理邏輯，另外用了叫做 HTML 及 CSS 的東西來寫一些介面。寫完之後如果對修改其他東西有興趣的話，可以去研究一下其他東西，或是跟我討論～

## 模板使用步驟

1. 點擊上方模板，進入頁面後點擊左上方的下拉式箭頭，如下圖的紅框 1
2. 點擊左下方的「fork」來複製一份，如下圖的紅框 2（這時候可能要登入）
3. 完成後應可看到如模板剛點進去的畫面，這時候點擊 `main.py`，在程式碼裡面可以找到一段註解，這裡就是要寫終極密碼判斷的部分。

![](<.gitbook/assets/image (122).png>)

## 檔案架構

![](<.gitbook/assets/image (133).png>)

* `main.py`: Python主程式，主要處理伺服器、網路網址、資料傳輸（Request & Response）
* `styles.css`: css 檔案提供 html 檔造型
* `index.html`: html 檔案提供介面骨架
* `pyproject.toml` & `requirements.txt`: 紀錄安裝的套件

## HTML 複習

![](<.gitbook/assets/image (123).png>)

每個<>稱做一個標籤，標籤有分開開頭跟結尾，要用相對應的標籤包起來。



![](<.gitbook/assets/image (128).png>)

### 練習

* h1: 把「blablabla 的網站」改成自己的名字
* a: 把「我的個人頁面」改成自己的連結

## CSS

大致上就是可以改變網頁造型的東西（顏色、字型、寬度高度等）

### 練習

* body: 把 background, color 改成自己喜歡的顏色

## Python

引入一些需要的函數庫，如 FastAPI 可以幫我們處理伺服器的東東，random 可以幫我們生成隨機答案

## 網址結構

![](<.gitbook/assets/image (132) (1).png>)

* Scheme：協定
* Domain/host：網域
* Path：路徑
* Query：查詢參數

![](<.gitbook/assets/image (131).png>)



### 會用到的網址

* [https://fastapi-template.hwchang.repl.co/](https://fastapi-template.hwchang.repl.co)
* [https://fastapi-template.hwchang.repl.co/?num=9527](https://fastapi-template.hwchang.repl.co/?num=9527)
* [https://fastapi-template.hwchang.repl.co/docs](https://fastapi-template.hwchang.repl.co/docs)
* [https://fastapi-template.hwchang.repl.co/comments](https://fastapi-template.hwchang.repl.co/comments)

### 練習

* 改變網址來造訪以上路徑
* 改變 num 這個 query 參數來猜數字

## 網路溝通方法：HTTP

我們跟伺服器請求（Request），伺服器給我們回應（Response）

今天介紹以下兩種請求方式（Request Method）：

* 取得：GET，一般我們透過瀏覽器輸入網址就是 GET
* 新增：POST，通常是表單，或是要利用程式來送出，不可透過瀏覽器輸入網址

舉例來說：

![](<.gitbook/assets/image (120).png>)

* 取得留言：`GET /comments`
* 新增留言：`POST /comments`

### 取得留言：`GET /comments`

![](<.gitbook/assets/image (121).png>)

#### 回應代碼（Response Code）

* 200 代表成功

#### **回應資料（Response Body）**

不同於之前是取得html，其實伺服器也可以只給我們文字資料，也就是以類似list + dict的形式回傳

### 新增留言：`POST /comments`

![](<.gitbook/assets/image (126) (1).png>)

#### **請求參數 Request Body**

新增當然需要一些參數，稱作 **Request Body**

**Body 不同於前面的 Query，Query 是公開的在網址上，Body 是隱藏的，且 GET 不能用 Body**

例如：

* author: 留言者
* content: 留言內容

**回應資料（Response Body）**

成功建立（200），回傳留言以及留言時間

![](<.gitbook/assets/image (120) (1) (1).png>)

### Response Code

成功通常以2開頭，常見的不成功有

* 404 Not Found
* 500 Internal Server Error

![](<.gitbook/assets/image (125).png>)

![](<.gitbook/assets/image (133) (1).png>)

## FastAPI



### 練習

* 寫一個 GET /profile，可以回傳你的小檔案

```json
{
    "name": "Vincent",
    "age": 21,
}
```

* 完成 DELETE /comments/{id}
