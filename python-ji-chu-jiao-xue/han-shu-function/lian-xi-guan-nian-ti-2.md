# ⚡ 練習：觀念題2

## 請問下列關於Python函數的敘述，何者錯誤？

1. 函數的參數可以是整數、字串
2. 函數的參數不能是函數
3. 函數可以當作變數一樣，放在list中
4. 函數只能有一個函數參數

2

在Python中，函數的參數可以放函數，請參考講義139頁

## 請問下列程式會輸出什麼？

```python
def g(num):
    num += 10
    return num

def h(num):
    num -= 3
    return num

def f(num, g, h):
    return h(g(num))


print(f(5, g, g))
```

1. 12
2. 24
3. 13
4. 25

4

此題考函數參數。需要注意的是在第13行，傳入f的是兩個g，所以f中的h其實是g，並不是會讓num-=3的h\(num\)，因此不能選12。

## 請問下列關於Python中key參數的敘述，何者錯誤？

1. key參數可以用來自訂比較參數
2. 像max, sort函數皆可以指定key參數可以放在裡
3. key參數接收一個函數，此函數需要有兩個參數，才可以比較兩者。
4. key參數接收一個函數，此函數需回傳一個值，表示需要比較的項目。

3

key函數只能接收一個參數，並且回傳一個要比較的項目。請參考講義143頁。

## 請問下列程式會輸出什麼？

```python
def key(p):
    return p[1] - p[0]

l = [
    [3, 1],
    [9, 0],
    [-1, 9],
    [65, 0],
]

print(max(l, key=key))
```

1. \[3, 1\]
2. \[9, 0\]
3. \[-1, 9\]
4. \[65, 0\]

3

經過key函數後，可以視為在\[-2, -9, 10, -65\]中取最大，很明顯的可以看出10最大，而對應到l中就是\[-1, 9\]

##  請問下列程式會輸出什麼？

```python
def key(p):
    return -p[0]

l = [
    [3, 1],
    [9, 0],
    [-1, 9],
    [65, 0],
]

l = sorted(l, key=key)
print(l[0])
```

1. \[3, 1\]
2. \[9, 0\]
3. \[-1, 9\]
4. \[65, 0\]

4

經過key函數，可以視為將\[-3, -9, 1, -65\]作升序排列，可知-65應在最前面，因此選擇對應到的\[65, 0\]

## 請問下列關於Python中lambda函數的敘述，何者錯誤？

1. lambda內的程式碼若大於一行，可像一般函數一樣換行
2. lambda可用於寫簡短的函數
3. lambda將直接回傳冒號後的結果
4. lambda可以定義多個參數

1

1.lambda內的程式碼只能有一行，若要寫多行函數，可寫成一般函數

##  請問下列程式會輸出什麼？

```python
l = [
    [3, 1],
    [9, 0],
    [-1, 9],
    [65, 0],
]

l = sorted(l, key=lambda x: max(x))
print(l[0])
```

1. \[3, 1\]
2. \[9, 0\]
3. \[-1, 9\]
4. \[65, 0\]

1

可先將lambda函數解析為一般函數，接著經過key函數後，可以視為將\[3, 9, 9, 65\]作升序排列，可知3應在最前面，因此選擇對應到的\[3, 1\]

## 請問下列程式會輸出什麼？

```python
def f(n):
    if n == 1:
        return 3
    elif n == 2:
        return 6
    elif n == 3:
        return 1
    else:
        return 2 * f(n-2) + 7 * f(n-3)
    
print(f(6))
```

1. 70
2. 71
3. 72
4. 73

4

慢慢拆解：

f\(6\) = 2 \* f\(4\) + 7 \* f\(3\)

f\(4\) = 2 \* f\(2\) + 7 \* f\(1\)

其中f\(3\), f\(2\), f\(1\)為已知，推回去即可得f\(6\) = 73

## 請問下列關於遞迴的敘述，何者錯誤？

1. 遞迴編寫非常的直觀
2. 遞迴執行速度快
3. 遞迴可減少冗餘程式碼
4. 最後呼叫的遞迴會最先完成

2

遞迴的執行速度不佳，且若在遞迴中呼叫過多次，可能會造成stack overflow錯誤（類似電腦太多事情處理不完，造成錯誤）。

## 若想要使用sys中的stdin，下列四種方法中，哪項是錯誤的？

```python
import sys
from sys import stdin
import stdin from sys
from sys import *
```

1. 1
2. 2
3. 3
4. 4

3

3.在Python中沒有import a from b的寫法。
