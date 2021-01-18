# 網頁遊戲設計​ - 終極密碼

先寫簡單的判斷程式

```python
ans = 88

num = int(input())

if num > ans:
    result = '太大了，再小一點'
elif num < ans:
    result = '太小了，再大一點'
else:
    result = '猜對了！'

print('輸入了' + str(num) + ': ' + str(result))

```

### 好工具：格式化字串

原本要寫很複雜

```python
print('輸入了' + str(num) + ': ' + str(result))
```

利用格式化字串變很簡單

```python
print(f'輸入了{num}: {result}')
```

放進程式碼

```python
ans = 88

num = int(input())

if num > ans:
    result = '太大了，再小一點'
elif num < ans:
    result = '太小了，再大一點'
else:
    result = '猜對了！'

print(f'輸入了{num}: {result}')
```

迴圈讓程式可以重複執行

```python
ans = 88

while True:
    num = int(input())

    if num > ans:
        result = '太大了，再小一點'
    elif num < ans:
        result = '太小了，再大一點'
    else:
        result = '猜對了！'

    print(f'輸入了{num}: {result}')
```

加入random

```python
import random

ans = random.randint(1, 100)

while True:
    num = int(input())

    if num > ans:
        result = '太大了，再小一點'
    elif num < ans:
        result = '太小了，再大一點'
    else:
        result = '猜對了！'

    print(f'輸入了{num}: {result}')
```

放到網頁上

![](.gitbook/assets/image%20%28110%29.png)

Repl.it

可以提供免費的伺服器，方便的開發環境（寫程式的地方）

[https://repl.it/@hwchang/python-guess-the-number-template](https://repl.it/@hwchang/python-guess-the-number-template)

### 說明

使用Python以及我預先寫好的網頁模板來完成一個線上終極密碼小遊戲

完成範例：[http://python-guess-the-number.hwchang.repl.co/](http://python-guess-the-number.hwchang.repl.co/)

模板：[https://repl.it/@hwchang/python-guess-the-number-template](https://repl.it/@hwchang/python-guess-the-number-template)

這個模板已經寫好很多東西了，都是用Python來處理邏輯，另外用了叫做Html及Css的東西來寫一些介面。另外為了讓這個模板變得有趣一點，我加了留言區，可以給大家留言，所以做完終極密碼可以丟給別人玩玩看&gt;&lt;，感覺比較好笑。寫完之後如果對修改其他東西有興趣的話，可以去研究一下其他東西，或是跟我討論～

### 模板使用步驟

1. 點擊上方模板，進入頁面後點擊左上方的下拉式箭頭，如下圖的紅框 1
2. 點擊左下方的「fork」來複製一份，如下圖的紅框 2（這時候可能要登入）
3. 完成後應可看到如模板剛點進去的畫面，這時候點擊main.py，在程式碼裡面可以找到一段註解，這裡就是要寫終極密碼判斷的部分。





* main.py: 要把Python程式馬上放去的地方
* styles.css: css檔案提供html檔造型
* index.html: html檔案提供介面骨架

### html index.html

&lt;--- ---&gt;代表註解，跟Python類似

&lt;h1&gt;代表標題文字，可以任意更改&lt;h1&gt;&lt;/h1&gt;內的文字，類似print\('something'\)

&lt;div&gt;代表一個區塊

&lt;p&gt;代表內文，就是一般小的文字，其中由大括號包住的{{num}}跟{{result}}是等等要由Python來填入的變數

&lt;/br&gt;代表換行，類似print\(\)

&lt;form&gt;代表表單，表單裡有個&lt;input&gt;可以送出num給伺服器，另一個&lt;input&gt;是一個按鈕，按下去可以提交（submit）表單

每個&lt;&gt;稱做一個標籤，標籤有分開開頭跟結尾，要用相對應的標籤包起來。

### css

不特別介紹，大致上就是可以改變網頁造型的東西

### python

引入一些需要的函數庫，如flask可以幫我們處理伺服器的東東，random可以幫我們生成隨機答案



### 完成終極密碼要做的事

這個模板已經把介面等等的部分寫好了，輸入的部分也處理好了，現在你們有三個變數可以使用，分別是：

* ans: 正確答案，型態為整數
* num: 使用者輸入的數字，型態為整數
* result: 輸出的字串，型態為字串

請寫一段簡單的程式讓result的結果符合終極密碼的邏輯！

但感覺有點簡單，甚至不需要用到迴圈while，因為這網頁就已經可以當作迴圈了

寫完的話可以按下圖紅框，會挑出一個網頁，並且有網址，可以分享給大家，也可以按右上方的share把程式碼給大家看～

3小時

