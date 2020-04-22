# ⚡ 練習：觀念題

## 若要在 Python 中判斷各種情況，可用下列哪種語法？

1. `if...else if...else`
2. `if...elif...else`
3. `if...else if...elif`

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

## if 裡面包含另一個 if 稱作什麼？

1. 巢狀 if
2. iff
3. i\(if\)f

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

## 下列程式碼會輸出什麼？

```python
print('a' + 'x' if 2 > 1 else 'y' + 'b')
```

## 下列程式碼會輸出什麼？

```python
x = 5
if x <= 5:
    pass
else:
    print("Hi!")
```

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

```text
0~10
10~20
20~30
30~40
40~50
```

2

```text
0~10
```

3

```text
10~20
```

## 請問如何改寫上段程式碼？

```python
# Your code.
```

## 期中題庫

### 若要邏輯判斷式 !\(X1 \|\| X2\)計算結果為真\(True\)，則 X1 與 X2 的值分別應為何？APCS1060304

1. **X1 為 False，X2 為 False**
2. X1 為 True，X2 為 True
3. X1 為 True，X2 為 False
4. X1 為 False，X2 為 True

### 下列是依據分數 s 評定等第的程式碼片段， 正確的等第公式應為：

* 90~100 判為 A 等 
* 80~89 判為 B 等 
* 70~79 判為 C 等
* 60~69 判為 D 等 
* 0~59 判為 F 等 

這段程式碼在處理 0~100 的分數時，有幾個分數的等第是錯的？

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

### 下列程式碼是自動計算找零程式的一部分，程式碼中三個主要變數分別為 Total \(購買 總額\)，Paid \(實際支付金額\)，Change \(找零金額\)。但是此程式片段有冗餘的程式 碼，請找出冗餘程式碼的區塊。

```python
Total = 123
Paid = 1000
Change = Paid - Total
print('500 : {} pieces'.format((Change - Change % 500)/500))
Change = Change % 500

print("100 : {} coins".format((Change-Change % 100)/100))
Change = Change % 100

# A 區
print("50 : {} coins".format((Change-Change % 50)/50))
Change = Change % 50

# B 區
print("10 : {} coins".format((Change-Change % 10)/10))
Change = Change % 10

# C 區
print("5 : {} coins".format((Change-Change % 5)/5))
Change = Change % 5

# D 區
print("1 : {} coins".format((Change-Change % 1)/1))
Change = Change % 1


```









