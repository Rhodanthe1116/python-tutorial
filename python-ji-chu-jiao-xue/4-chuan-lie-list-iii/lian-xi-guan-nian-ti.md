# ⚡ 練習：觀念題

## 如果要取用 List 中第 3 個元素，需要用以下何者？

1. `l[3]`
2. `l[2]`
3. `l[1]`
4. `l[0]`

2

list的標籤是從0開始

![](../../.gitbook/assets/image%20%28105%29.png)

## 請問Python中的List有以下哪項功能？

1. 一次儲存多個變數
2. 排序
3. 找最大值
4. 以上皆是

4 

1. 基本功能

2. sort\(\)或sorted\(\)

3.max\(\)

## 下列哪一項是正確的？

1. list 中的同個元素可以出現很多次
2. list 中的元素都必須要是相同類型的
3. list 中不能存 list
4. list 的大小\(長度\)是固定的

1

2 可以是不同型態

3 可以存（list也是一種資料型態）

4 list可以隨時增減元素，例如使用append\(\)

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
   >>> print(a[:] is a)
   True
   ```
3. ```python
   >>> print(a[4::-2])


   ['quux', 'baz', 'foo']
   ```

3

1: list中最後一個元素代表-1，所以-6正是'foo'

2: a\[:\]會複製一個新的list，即使他們的值相同（a\[:\] == a），複製的list與原本的list仍是兩個不同的個體。 

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
   a = a + ['d'] + ['e']
   ```

3 

會變成\['a', 'b', 'c', \['d', 'e'\]\]，因為append\(\)會將\(\)裡的東西原封不動的加進去。不同於extend\(\)會將\(\)裡的list與原list合併。

## 有一 List：

```python
a = [1, 2, 7, 8]
```

請寫一段程式碼讓他變成

```python
[1, 2, 3, 4, 5, 6, 7, 8]
```

參考解答

```python
a = a[0:2] + [3, 4, 5, 6] + a[2:]
print(a)
```

## 請問下列程式碼會輸出什麼？

```python
A = [0, 1, 2, 3, 4, 5]
n = len(A)
for i in range(n):
    if i == 0: A[0] = A[0]
    else: A[i] += A[i - 1]
B = [0]
B.extend(A)
print(B)
```

1. \[0, 1, 2, 3, 4, 5\]
2. \[0, 0, 1, 2, 3, 4, 5\]
3. \[0, 0, 1, 3, 6, 10, 15\]
4. \[0, 1, 3, 6, 10, 15\]

3

照著程式碼模擬一遍，到第6行時可知A = \[0, 1, 3, 6, 10, 15\]，此時B = \[0\]，B.extend\(A\)會將B和A合併，於是B變成\[0, 0, 1, 3, 6, 10, 15\]，故選選項三

## 期中題庫

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

### 若 A 是一個可儲存 n 筆整數的串列，且資料儲存於 A\[0\]~A\[n-1\]。經過右側程式碼運算後，以下何者敘述不一定正確？

```python
A = [...(共有n個元素)]
p = q = A[0]
for i in range(1, n):
    if A[i] > p:
        p = A[i]
    if A[i] < q:
        q =A[i]
```

1. **q &lt; p**
2. p 是 A 陣列資料中的最大值
3. q 是 A 陣列資料中的最小值
4. A\[0\] &lt;= p

