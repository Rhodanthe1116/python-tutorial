# ⚡ 練習：觀念題

## 通常 while 是用來處理什麼情況的迴圈？

1. 事先知道明確執行次數的情況
2. 事先不知道明確執行次數的情況
3. 1, 2都很適合
4. 1, 2都不適合

2

while()裡面只能放一個條件，通常不會事先知道while裡面將會做幾次，我們只要知道，會重複執行到while裡面的條件不成立，比如說要不斷的把n除以2，直到n <= 0，可以使用 while(n > 0)，。對於事先知道要執行幾次的情況，比如說執行n次，一般會使用for，如for i in range(n)

## 通常 for 是用來處理什麼情況的迴圈？

1. 事先知道明確執行次數的情況
2. 事先不知道明確執行次數的情況
3. 1, 2都很適合
4. 1, 2都不適合

1

請參照第一題

## 下列程式碼會輸出什麼？

```python
for x in range(10):
    if x % 2 == 0:
        break
    print(x)
```

1. (什麼都沒有輸出)
2. 1 3 5 7 9
3. 2 4 6 8 10
4. 1 2 3 4 5 6 7 8 9

1

因為x在一開始會等於0，第二行也就會成立，執行break會立即跳出for，因此第四行沒有機會被執行到。



## 下列程式碼會輸出什麼？

```python
for x in range(10):
    if x % 2 == 0:
        continue
    print(x)
```

1. (什麼都沒有輸出)
2. 1 3 5 7 9
3. 2 4 6 8 10
4. 1 2 3 4 5 6 7 8 9

2

若x 可以被2整除，將會執行到continue，執行到continue會直接掉過那次迴圈，回到第一行進行下一次迴圈。

## 下列哪段程式碼是對的？

1. ```python
   for x in range(10)
       print(x)
   ```
2.  ```python
    for i in range(10):
        print(i)

    ```



2

for 語法的最後面要加冒號

## 下列哪段程式碼是對的？

1. ```python
   while True:
       print("hi")
   ```
2.  ```python
    while true:
        print("hi")
    ```



1

在Python裡面，True跟False都要首字大寫

## 下列程式碼會輸出什麼？

```python
for i in range(5):
    print("A", end=' ')
    for j in range(3):
        print("*", end='')
        if j == 2:
            break
    print()
```

1

```
A ***
A ***
A ***
A ***
A ***
```

2

```
A **
A **
A **
A **
A **
```

3

```
A 
***
A 
***
A 
***
A 
***
A 
***
```

1

注意print("A", end=' ')因為有修改end所以不會換行，還有break的後面已經沒有程式碼了，所以break沒有起任何作用

## 下列程式碼會輸出什麼？

```python
x = 0
n = 5
for i in range(1, n+1):
    for j in range(1, n+1):
        if i + j == 2:
            x = x + 2
        if i + j == 3:
            x = x + 3
        if i + j == 4: 
            x = x + 4
print(x)
```

1. 18
2. 19
3. 20
4. 21

20

慢慢窮舉i從1\~5, j從1\~5

```python
i + j
1 + 1 = 2 
1 + 2 = 3
1 + 3 = 4
2 + 1 = 3
2 + 2 = 4
3 + 1 = 4
--------
x     = 20
```

1, 1

1



## 下列程式碼會輸出什麼？

```python
x = 5
while x < 10:
    print("YES! YES! YES! YES!")
```

1

```
YES! YES! YES! YES!
```

2

```
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
```

3

```
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
...無限多個
```

3

因為x = 5會一直小於10，因此迴圈會不斷執行

## 上題迴圈稱作什麼？

無窮迴圈、無限迴圈等

## 改自佳儫ppt

### 請問若輸入兩數字n, m，則t會輸出什麼？

```python
n = int(input())
m = int(input())

t = 0
for j in range(1, n+1):
    for i in range(1, m+1):
        t += 1
print(t)
```

1. n\*m
2. (n+1) \* (m+1)
3. n \* (m + 1)
4. n \* n



## 期中 APCS

### 請問下列程式輸出為何？

```python
x = 0
for i in range(n):
    for j in range(i, n):
        k = 1
        while k <= n:
            x = x + 1
            k *= 2
print(x)
```

1. n(n+1)\*sqrt(log2(𝑛))
2. n2(n+1)/2
3. **n(n+1)\[ (log2(n)) + 1 ] / 2**
4. n(n+1)/2

### 請問執行下列程式的時候，哪一行可能永遠不會被執行到

```python
a = int(input())
while a < 10:
    a = a + 5
if a < 12:
    a = a + 2
if a <= 11:
    a = 5
```

1. a = a + 5
2. a = a + 2
3. **a = 5**
4. 每一行都執行得到

### 右側程式片段中執行後若要印出下 列圖案，(a) 的條件判斷式該如何 設定？

```python
for i in range(3):
    for j in range(i):
        print(' ', end='')
    for k in range(6-2*i, ---(a)---, -1):
        print('*', end='')
    print()

# 輸出
'''
******
 ****
  **
'''
```

### 右側程式正確的輸出應該如下程式碼的註解部分。在不修改右側程式之第 4 行及第 7 行程 式碼的前提下，最少需修改幾行程式碼 以得到正確輸出？

```python
k = 4
m = 1
for i in range(1, 5+1):
    for j in range(1, k+1):
        print(' ', end='')
    for j in range(1, m+1):
        print('*', end='')
    print()
    k = k - 1
    m = m + 1

# 理想輸出
'''
    *
   ***
  *****
 *******
*********
'''


```

答案：m = m + 2

### 若 n 為正整數，右側程式三個迴圈執行 完畢後 a 值將為何？

```python
a = 0
n = int(input())

for i in range(1, n+1):
    for j in range(i, n+1):
        for k in range(1, n+1):
            a = a + 1
print(a)

```

### 右側程式片段執行過程中的輸出為何？

```python
a = 5

for i in range(0, 20, a + 1):
    print(i + 5)
```

### 請問右側程式，執行完後輸出為何？

```python
i = 2
x = 3
N = 65536

while i <= N:
    i = i * i * i
    x = x + 1

print(i, x)
```
