# ⚡ 練習：觀念題2

## 請問下列關於Python函數的敘述，何者錯誤？

1. 函數的參數可以是整數、字串
2. 函數的參數不能是函數
3. 函數可以當作變數一樣，放在list中
4. 函數可以有不同型態的參數

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

## 期末APCS

### 給定函式 A1\(\)、 A2\(\) 與 F\(\) 如下，以下敘述何者有誤？

```python
def A1(n):
    F(n//5)
    F(4*n//5)

def A2(n):
    F(2*n//5)
    F(3*n//5)

def F(x):
    for i in range(x):
        print("*", end='')
    if x > 1:
        F(x//2)
        F(x//2)
  
# Test
A1(5)
print()
A2(5)
print()
A1(13)
print()
A2(13)
print()
A1(14)
print()
A2(14)
print()
A1(15)
print()
A2(15)
```

1. A1\(5\) 印的 '' 個數比 A2\(5\) 多 
2. A1\(13\) 印的 '' 個數比 A2\(13\) 多 
3. A2\(14\) 印的 '' 個數比 A1\(14\) 多 
4. A2\(15\) 印的 '' 個數比 A1\(15\) 多

4

### 右側 F\(\)函式回傳運算式該如何寫，才會使得 F\(14\) 的回傳值為 40?

```python
def F():
    if n < 4:
        return n
    else
        return _____?_____
```

1. n \* F\(n-1\)
2. n + F\(n-3\)
3. n - F\(n-2\)
4. F\(3\*n+1\)

2

### 右側函式兩個回傳式分別該如何撰寫，才能正確計算並回傳兩參數 a, b 之最大公因數 \(Greatest Common Divisor\)？

```python
def GCD(a, b):
    r = a % b
    if r == 0:
        return ______
    return ______
```

1. a, GCD\(b,r\)
2. b, GCD\(b,r\)
3. a, GCD\(a,r\)
4. b, GCD\(a,r\)

2

### 若以 B\(5,2\)呼叫右側 B\(\)函式，總共會印出幾次 “base case”？

```python
def B(n, k):
    if k == 0 or k == n:
        print("base case")
        return 1
    return B(n-1, k-1) + B(n-1, k)

# Test
B(5, 2)
```

1. 1
2. 5
3. 10
4. 19

3

### 給定右側程式，請問程式執行後輸出為何？

```python
s = 1

def add(a):
    s = 6
    for i in range(a+1):
        print(s, end=', ')
        s += 1
        print(s, end=', ')
        
print(s, end=', ')
add(s)
print(s, end=', ')
s = 9
print(s)
```

1. 1,6,7,7,8,8,9
2. 1,6,7,7,8,1,9
3. 1,6,7,8,9,9,9
4. 1,6,7,7,8,9,9

2

### 若以 F\(15\)呼叫右側 F\(\)函式，總共會印出幾行數字？

```python
def F(n):
    print(n)
    if (n % 2 == 1) and n > 1:
        return F(5*n+1)
    else:
        if n % 2 == 0:
            return F(n/2)

# Test
F(15)
```

1. 16 行
2. 22 行
3. 11 行
4. 15 行

4

### 若以 F\(5,2\)呼叫右側 F\(\)函式，執行完畢後回傳值為何?

```python
def F(x, y):
    if x < 1:
        return 1
    else:
        return F(x-y, y) + F(x - 2*y, y)

# Test
print(F(5, 2))
```

1. 1
2. 3
3. 5
4. 8

3

### 若以 G\(100\)呼叫函式後，總共會輸出幾個'\*'?

```python

def K(b):
    print('*')
    if b % 4:
        K(b+1)

def G(m):
    for i in range(m):
        K(i)

G(100)3
```

1. 25
2. 75
3. 150
4. 250

4

### 給定右側函式 F\(\)，F\(n\)執行完所回傳的 x 值為何？

```python
def F(n):
    x = 0
    for i in range(1, n+1):
        for j in range(i, n+1):
            k = 1
            while k <= n:
                k *= 2
                x = x + 1
    return x
```

![](../../.gitbook/assets/image%20%28115%29.png)

1. A
2. B
3. C
4. D

3

### 給定 G\(\), K\(\) 兩函式，執行 G\(3\)後所回傳的值為何？

```python
def K(a, n):
    if n >= 0:
        return K(a, n-1) + a[n]
    else:
        return 0

def G(n):
    a = [5, 4, 3, 2, 1]
    return K(a, n)

print(G(3))

```

1. 5
2. 12
3. 14
4. 15

3

### 函式以 F\(7\) 呼叫後回傳值為 12，則&lt;condition&gt; 應為何？

```python
def F(a):
    if (<condition>):
        return 1
    else:
        return F(a-2) + F(a-3)

print(F(7))

```

1. a &lt; 3
2. a &lt; 2
3. a &lt; 1
4. a &lt; 0

4

### 程式執行完三次 G\(\)的呼叫後，p陣列中有幾個元素的值為 0？

```python
def K(p, v):
    if p[v] != v:
        p[v] = K(p, p[v])
    return p[v]

def G(p, l, r):
    a = K(p, l)
    b = K(p, r)
    if a != b:
        p[b] = a
        
p = [0, 1, 2, 3, 4]
G(p, 0, 1)
G(p, 2, 4)
G(p, 0, 4)

```

1. 1
2. 2
3. 3
4. 4

3

### 請問下列程式會輸出什麼？

```python
def G(B):
    B = B * B
    return B

a = 0
m = 5
a = G(m)
if m < 10:
    a = G(m) + a
else:
    a = G(m)
    
print(a)

```

1. 0
2. 10
3. 25
4. 50

4

### 如下

```python
class element:
    data = 0
    next = -1

def remove_next_element(mylist, current):
    if mylist[current].next != -1:
        # 移除current的下一個element
```

List 是一個陣列，裡面的元素是 element， 它的定義如上程式碼

List 中的每一個 element 利用 next 這個整數變數來記錄下一個 element 在陣列中的位置，如果沒有下一個 element， next 就會記錄-1。所有的 element 串成了一 個串列 \(linked list\)。例如在 list 中有三筆 資料

![](../../.gitbook/assets/image%20%28114%29.png)

它所代表的串列如下圖

![](../../.gitbook/assets/image%20%28117%29.png)

remove\_next\_element 是一個函數，用來移除串列中 current 所指向的下一個元素，但是必須 保持原始串列的順序。例如，若 current 為 3 \(對應到 list\[3\]\)， 呼叫完 remove\_next\_element 後，串列應為

![](../../.gitbook/assets/image%20%28118%29.png)

請問在上程式碼中，註解下應該填入的程式碼為何?

1. mylist\[current\].next = current 
2. mylist\[current\].next = mylist\[mylist\[current\].next\].next 
3. current = mylist\[mylist\[current\].next\].next 
4. mylist\[mylist\[current\].next\].next = mylist\[current\].next 

2









### 

