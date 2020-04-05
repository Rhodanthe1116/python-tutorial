# ⚡ 練習：觀念題

## while 是用來處理什麼情況的迴圈？

1. 事先知道明確執行次數的情況
2. 事先不知道明確執行次數的情況
3. 都可以

## for 是用來處理什麼情況的迴圈？

1. 事先知道明確執行次數的情況
2. 事先不知道明確執行次數的情況
3. 都可以

## 下列程式碼會輸出什麼？

```python
for x in range(10):
    if x % 2 == 0:
        break
    print(x)
```

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

## 期中

請問下列程式輸出為何？

```python
x = 0
for i in range(n):
    for j in range(n):
        k = 1
        while k <= n:
            x = x + 1
            k *= 2
print(x)
```

1. n\(n+1\)√⌊log2 𝑛⌋
2. n2\(n+1\)/2
3. **n\(n+1\)⌊log2n + 1⌋/2**
4. n\(n+1\)/2

請問執行下列程式的時候，哪一行可能永遠不會被執行到

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



