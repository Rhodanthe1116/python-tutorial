# ⚡ 練習：觀念題（題目版）

## 如果要取用 List 中第 3 個元素，需要用以下何者？

1. `l[3]`
2. `l[2]`
3. `l[1]`
4. `l[0]`

## 請問Python中的List有以下哪項功能？

1. 一次儲存多個變數
2. 排序
3. 找最大值
4. 以上皆是

## 下列哪一項是正確的？

1. list 中的同個元素可以出現很多次
2. list 中的元素都必須要是相同類型的
3. list 中不能存 list
4. list 的大小\(長度\)是固定的

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

## 有一 List：

```python
a = [1, 2, 7, 8]
```

請寫一段程式碼讓他變成

```python
[1, 2, 3, 4, 5, 6, 7, 8]
```

## 請問下列程式碼會輸出什麼？

```python
A = [0, 1, 2, 3, 4, 5]
n = len(A)
for i in range(n):
    if i == 0: A[0] = A[0]
    else: A[i] += A[i - 1]
B = [0]
B += A
print(B)
```

1. \[0, 1, 2, 3, 4, 5\]
2. \[0, 0, 1, 2, 3, 4, 5\]
3. \[0, 0, 1, 3, 6, 10, 15\]
4. \[0, 1, 3, 6, 10, 15\]

