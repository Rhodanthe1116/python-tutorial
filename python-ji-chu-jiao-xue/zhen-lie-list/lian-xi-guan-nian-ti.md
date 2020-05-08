# ⚡ 練習：觀念題

## 如果要取用 List 中第 3 個元素，需要用以下何者？

1. `l[3]`
2. `l[2]`
3. `l[1]`

## List 有以下哪些功能？

1. 一次儲存多個變數
2. 排序
3. 找最大值

## 下列哪一項是正確的？

1. list 中的同個元素可以出現很多次
2. list 中的元素都必須要是相同類型的
3. list 中不能存 list

## 假設有一個 List:

```python


a = ['foo', 'bar', 'baz', 'qux', 'quux', 'corge']


```

以下哪個指令與輸出結果是相吻合的？

1. ```python
   >>> print(a[-6])

   Traceback (most recent call last):
     File "<stdin>", line 1, in <module>
   IndexError: list index out of range  

   ```
2. ```python
   >>> a[:] is a
   True
   ```
3. ```python
   >>> print(a[4::-2])


   ['quux', 'baz', 'foo']
   ```

## 假設有一 List：

```python
a = ['a', 'b', 'c']
```

若想讓他變成

```python
['a', 'b', 'c', 'd', 'e']
```

則下列哪一項是不正確的？

1. ```python
   a.extend(['d', 'e'])
   ```
2. ```python
   a += ['d', 'e']
   ```
3. ```python
   a.append(['d', 'e'])
   ```
4. ```python
   a = a + 'd' + 'e'
   ```

## 有一 List：

```python
a = [1, 2, 7, 8]
```

寫一段程式碼讓他變成

```python
[1, 2, 3, 4, 5, 6, 7, 8]
```

## 期中

### 下列程式擬找出陣列 A\[\]中的最大值和最小值。不過，這段程式碼有誤，請問 A\[\]初始值如何設定就可以測出程式有誤？

```python
M = -1
N = 101
s = 3
A = [______?______]

for i in range(s):
    if A[i] > M:
        M = A[i]
    elif A[i] < N:
        N = A[i]


print("M = ", M)
print("N = ", N)
```

1. \[90, 80, 100\]
2. **\[80, 90, 100\]**
3. \[100, 90, 80\]
4. \[90, 100, 80\]

### 程式碼執行後輸出結果為何？

```python
a = [1, 3, 5, 7, 9, 8, 6, 4, 2]
n = 9
tmp = 0

for i in range(n):
    tmp = a[i]
    a[i] = a[n-i-1]
    a[n-i-1] = tmp

for i in range(int(n/2) + 1):
    print(a[i], a[n-i-1], end=' ')
```

1. 2 4 6 8 9 7 5 3 1 9
2. 1 3 5 7 9 2 4 6 8 9
3. **1 2 3 4 5 6 7 8 9 9**
4. 2 4 6 8 5 1 3 7 9 9

### 右側程式片段執行 後，count 的值 為何？

```python
maze = [
    [1, 1, 1, 1, 1],
    [1, 0, 1, 0, 1],
    [1, 1, 0, 0, 1],
    [1, 0, 0, 1, 1],
    [1, 1, 1, 1, 1]
]
count = 0
for i in range(1, 3+1):
    for j in range(1, 3+1):
        dir = [
            [-1, 0],
            [0, 1],
            [1, 0],
            [0, -1]
        ]
        for d in range(4):
            if maze[i+dir[d][0]][j+dir[d][1]] == 1:
                count += 1

print(count)

```

### 右側程式片段執行過程的輸出 為何？

```python
arr = [0] * 10
for i in range(10):
    arr[i] = i

sum = 0
for i in range(1, 9):
    sum = sum - arr[i-1] + arr[i] + arr[i+1]
print(sum)

```

### 下列程式碼會輸出什麼？

```python
n = 10
a = [1, 3, 9, 2, 5, 8, 4, 9, 6, 7]

index = 0
for i in range(1, n):
    if a[i] >= a[index]:
        index = i
print(index)


```

