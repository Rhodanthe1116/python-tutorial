# ⚡ 練習：觀念題

## 通常 while 是用來處理什麼情況的迴圈？

1. 事先知道明確執行次數的情況
2. 事先不知道明確執行次數的情況
3. 1, 2都很適合
4. 1, 2都不適合

## 通常 for 是用來處理什麼情況的迴圈？

1. 事先知道明確執行次數的情況
2. 事先不知道明確執行次數的情況
3. 1, 2都很適合
4. 1, 2都不適合

## 下列程式碼會輸出什麼？

```python
for x in range(10):
    if x % 2 == 0:
        break
    print(x)
```

1. \(什麼都沒有輸出\)
2. 1 3 5 7 9
3. 2 4 6 8 10
4. 1 2 3 4 5 6 7 8 9

## 下列程式碼會輸出什麼？

```python
for x in range(10):
    if x % 2 == 0:
        continue
    print(x)
```

## 下列哪段程式碼是對的？

1. ```python
   for x in range(10)
       print(x)
   ```
2. ```python
   for i in range(10):
       print(i)
   ```

## 下列哪段程式碼是對的？

1. ```python
   while True:
       print("hi")
   ```
2. ```python
   while true:
       print("hi")
   ```

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

```text
A ***
A ***
A ***
A ***
A ***
```

2

```text
A **
A **
A **
A **
A **
```

3

```text
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

## 下列程式碼會輸出什麼？

```python
x = 5
while x < 10:
    print("YES! YES! YES! YES!")
```

1

```text
YES! YES! YES! YES!
```

2

```text
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
```

3

```text
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
YES! YES! YES! YES!
...無限多個
```

## 上題迴圈稱作什麼？



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
2. \(n+1\) \* \(m+1\)
3. n \* \(m + 1\)
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

1. n\(n+1\)\*sqrt\(log2\(𝑛\)\)
2. n2\(n+1\)/2
3. **n\(n+1\)\[ \(log2\(n\)\) + 1 \] / 2**
4. n\(n+1\)/2

### 請問執行下列程式的時候，哪一行可能永遠不會被執行到

```python
a = input()
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

### 右側程式片段中執行後若要印出下 列圖案，\(a\) 的條件判斷式該如何 設定？

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

