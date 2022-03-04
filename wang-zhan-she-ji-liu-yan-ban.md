# 網站設計 - 留言板

### 網頁原理

![](<.gitbook/assets/image (125).png>)

### 伺服器

Repl.it

可以提供免費的伺服器，方便的開發環境（寫程式的地方）

[https://replit.com/@hwchang/fastapi-template](https://replit.com/@hwchang/fastapi-template)

### 說明

使用Python以及我預先寫好的網頁模板來完成一個線上留言板

完成範例：[https://fastapi-template.hwchang.repl.co/](https://fastapi-template.hwchang.repl.co)

模板：[https://replit.com/@hwchang/fastapi-template](https://replit.com/@hwchang/fastapi-template)

這個模板已經寫好很多東西了，都是用Python來處理邏輯，另外用了叫做Html及Css的東西來寫一些介面。另外為了讓這個模板變得有趣一點，我加了留言區，可以給大家留言，所以做完終極密碼可以丟給別人玩玩看><，感覺比較好笑。寫完之後如果對修改其他東西有興趣的話，可以去研究一下其他東西，或是跟我討論～

### 模板使用步驟

1. 點擊上方模板，進入頁面後點擊左上方的下拉式箭頭，如下圖的紅框 1
2. 點擊左下方的「fork」來複製一份，如下圖的紅框 2（這時候可能要登入）
3. 完成後應可看到如模板剛點進去的畫面，這時候點擊main.py，在程式碼裡面可以找到一段註解，這裡就是要寫終極密碼判斷的部分。

![](<.gitbook/assets/image (122).png>)

### 檔案架構

![](<.gitbook/assets/image (124).png>)

* `main.py`: Python主程式，主要處理伺服器、網路、與資料流
* `comments.py`: 我們為了方便，將留言的功能獨立到一個檔案中
* `styles.css`: css檔案提供html檔造型
* `index.html`: html檔案提供介面骨架

### html複習

![](<.gitbook/assets/image (123).png>)

每個<>稱做一個標籤，標籤有分開開頭跟結尾，要用相對應的標籤包起來。



![](<.gitbook/assets/image (128).png>)



### css

不特別介紹，大致上就是可以改變網頁造型的東西

### python

引入一些需要的函數庫，如flask可以幫我們處理伺服器的東東，random可以幫我們生成隨機答案





### 網路溝通方法：HTTP

我們跟伺服器請求（Request），伺服器給我們回應（Response）

今天介紹以下兩種請求（Request）：

* 取得：GET
* 新增：POST

舉例來說

![](<.gitbook/assets/image (127).png>)

* 取得留言：`GET /comments/`
* 新增留言：`POST /comments/`

#### 取得留言：`GET /comments/`

不同於之前是取得html，其實伺服器也可以只給我們資料，也就是以類似list + dict的形式回傳

![](<.gitbook/assets/image (121).png>)

#### 新增留言：`POST /comments/`

新增當然需要一些參數，稱作 **Request Body**

例如：

* author: 留言者
* content: 留言內容

![](<.gitbook/assets/image (126).png>)



