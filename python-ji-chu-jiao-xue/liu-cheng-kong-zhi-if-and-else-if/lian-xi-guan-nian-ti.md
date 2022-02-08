# ⚡ 練習：觀念題

## 若要在 Python 中判斷各種情況，可用下列哪種語法？

1. ```python
   if
       ...
   else if
       ...
   else
   ```
2. ```python
   if
       ...
   elif
       ...
   else
   ```
3. ```python
   if
       ...
   else if
       ...
   elif
   ```

## 下列哪個程式碼是對的？

1. ```python
   x = 10
   if x = 10:
       print("x等於10")
   else:
       print("x不等於10")
   ```
2. ```python
   x = 10
   if x == 10:
       print("x等於10")
   else:
       print("x不等於10")
   ```
3. 1, 2皆對
4. 1, 2皆非

2

1.的第二行的 = 應改為 ==

## if 裡面包含另一個 if 稱作什麼？

1. 巢狀 if
2. iff
3. i(if)f
4. elif



## 下列哪個程式碼是對的？

1. ```python
   x = 10
   if x == 10:
       print("x等於10")
   ```
2. ```python
   x = 10
   if x == 10:
   print("x等於10")
   ```
3. 1, 2皆對
4.  1, 2皆非



1

2.的第三行應縮排（if裡面的內容應縮排）

## 下列哪個程式碼是對的？

1. ```python
   x = 10
   if x = 10: print("x等於10")
   ```
2. ```python
   x = 10
   if x == 10:
   print("x等於10")
   ```
3. 1, 2皆對
4. 1, 2皆非

4

1.第二行應為==

2.第三行應縮排

## 下列程式碼會輸出什麼？

```python
a = 5
if a > 3:
    print(1)
    print(2)
    if a > 5:
        print(3)
print(4)
```

1. 1 2 4
2. 1 2
3. 1 2 5
4. 1 2 3 4



## 請問下列程式碼會輸出什麼？

```python
ans = 'a' + 'x' if 2 > 1 else 'y' + 'b'
print(ans)
```

ax

此為三元運算子，其等同於

```python
if 2 > 1:
    print('a' + 'x')
else: 
    print('y' + 'b')
```

## 下列程式碼會輸出什麼？

```python
x = 5
if x <= 5:
    pass
else:
    print("Hi!")
```

1. Hi!
2. pass
3. (什麼都沒有輸出)
4. 5



什麼都沒有輸出



因為x <= 5是True，所以會執行pass，pass代表什麼都不做，因此直接結束if，結束程式

## 下列程式碼會輸出什麼？

```python
x = 0
if x <= 10: print("0~10")
if x <= 20: print("10~20")
if x <= 30: print("20~30")
if x <= 40: print("30~40")
if x <= 50: print("40~50")
```

1

```
0~10
10~20
20~30
30~40
40~50
```

2

```
0~10
```

3

```
10~20
```

4

```bash
20~30
```

1

因為每個 if 之間是獨立的，在這裡都會被執行到，而且每個條件也剛好成立，所以輸出會與想法不同。正確寫法請參考下題。

## 請問如何改寫上段程式碼？

```python
# Your code.



```

```python
x = 0
if x <= 10: print("0~10")
elif x <= 20: print("10~20")
elif x <= 30: print("20~30")
elif x <= 40: print("30~40")
elif x <= 50: print("40~50")
```

## 期中題庫

### 若要邏輯判斷式 not (X1 or X2)計算結果為真(True)，則 X1 與 X2 的值分別應為何？APCS1060304

1. **X1 為 False，X2 為 False**
2. X1 為 True，X2 為 True
3. X1 為 True，X2 為 False
4. X1 為 False，X2 為 True

### 下列是依據分數 s 評定等第的程式碼片段， 正確的等第公式應為：

* 90\~100 判為 A 等&#x20;
* 80\~89 判為 B 等&#x20;
* 70\~79 判為 C 等
* 60\~69 判為 D 等&#x20;
* 0\~59 判為 F 等&#x20;

這段程式碼在處理 0\~100 的分數時，有幾個分數的等第是錯的？

```python
if s >= 90:
    print("A")
elif s >= 80:
    print("B")
elif s > 60:
    print("D")
elif s > 70:
    print("C")
else:
    print("F")
```

1. 20
2. **11**
3. 2
4. 10

### 下列程式碼是自動計算找零程式的一部分，程式碼中三個主要變數分別為 Total (購買 總額)，Paid (實際支付金額)，Change (找零金額)。但是此程式片段有冗餘的程式 碼，請找出冗餘程式碼的區塊。

```python
Total = 123
Paid = 1000
Change = Paid - Total
print("500 :", (Change - Change % 500)/500, "pieces")
Change = Change % 500

print("100 :", (Change - Change % 100)/100, "coins")
Change = Change % 100

# A 區
print("50 :", (Change - Change % 50)/50, "coins")
Change = Change % 50

# B 區
print("10 :", (Change - Change % 10)/10, "coins")
Change = Change % 10

# C 區
print("5 :", (Change - Change % 5)/5, "coins")
Change = Change % 5

# D 區
print("1 :", (Change - Change % 1)/1, "coins")
Change = Change % 1
```







