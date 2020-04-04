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





