# 二維串列 Two-dimensional lists



類似 Excel 等表格，有兩個軸，其實就是在 List 裡面放 List，如下：

```python
a = [[1, 2, 3], 
     [4, 5, 6]]
```

等同於

```python
a = [[1, 2, 3], [4, 5, 6]]
```

可以換行或不換行，每個元素的取得如下：

```python
a = [[1, 2, 3], [4, 5, 6]]
print(a[0])
print(a[1])
print(a[0][2])
a[0][1] = 7
print(a)
print(a[0])
```

| a | 0 | 1 | 2 |
| :--- | :--- | :--- | :--- |
| 0 | `a[0][0]` | `a[0][1]` | `a[0][2]` |
| 1 | `a[1][0]` | `a[1][1]` | `a[1][2]` |

同樣是可變的，使用等於會指向同一個

```python
a = [[1, 2, 3], [4, 5, 6]]
b = a
print("a", a)
print("b", b)
print()

a[0][1] = 7
print("a", a)
print("b", b)
print()

b[0][2] = 9
print("a", a)
print("b", b)
```

也可以不同大小

```python
a = [[1, 2, 3, 4], [5, 6], [7, 8, 9]]
```

## 遍歷 Loop Through

```python
a = [[1, 2, 3, 4], [5, 6], [7, 8, 9]]
for i in range(len(a)):
    for j in range(len(a[i])):
        print(a[i][j], end=' ')
    print()
```

```python
a = [[1, 2, 3, 4], [5, 6], [7, 8, 9]]
for row in a:
    for elem in row:
        print(elem, end=' ')
    print()
```

## 輸出技巧 Print Technique

```python
a = [[1, 2, 3, 4], [5, 6], [7, 8, 9]]
for row in a:
    print(*row)
```

## 創造 Create

一維的方法會不可行

{% hint style="danger" %}
```python
n = 3
m = 5
a = [[0] * m] * n
```

比如說：

```python
n = 3
m = 5
a = [[0] * m] * n

for row in a:
    print(*row)
print()

a[0][0] = 1

for row in a:
    print(*row)
```
{% endhint %}

因為`[[0] * m] *  n`會讓 n 個都指向相同的`[[0] * m]`

### 第一種方法

```python
n = 3
m = 4
a = [0] * n
for i in range(n):
    a[i] = [0] * m
```

### 第二種方法

```python
n = 3
m = 4
a = []
for i in range(n):
    a.append([0] * m)
```

### 第三種方法

```python
n = 3
m = 4
a = [[0] * m for i in range(n)]
```

## Input

假設要輸入n = 3的 list：

```python
# n = 3
3
0 1 2 3
4 5 6 7
8 9 10 11
```

### 直觀但不好寫

```python
n = int(input()) 
a = []
for i in range(n):
    row = input().split()
    for i in range(len(row)):
        row[i] = int(row[i])
    a.append(row)
```

### 直觀好寫

```python
n = int(input()) 
a = []
for i in range(n):
    row = list(map(int, input().split()))
    a.append(row)
```

或

```python
n = int(input()) 
a = []
for i in range(n):
    a.append([int(j) for j in input().split()])
```

### 不直觀但好寫

```python
n = int(input()) 
a = [[int(j) for j in input().split()] for i in range(n)]
```

## Generator

```python
a = [[0] * m for i in range(n)]
```

像這樣`for`在list裡面是利用一種叫做產生器的東西，其實之前就有看過產生器，比如`range()`，就是一個產生器，產生出一個類似list但不是list，又可以遍歷的物件

產生器也可以巢狀

```python
n = 9
m = 9
a = [[i * j for j in range(m)] for i in range(n)]

for row in a:
    print(*row)
```

