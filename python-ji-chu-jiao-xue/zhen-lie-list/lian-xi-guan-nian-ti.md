# ⚡ 練習：觀念題

## 請問下列關於List的敘述，何者錯誤？

1. 可以儲存大量資料
2. 可以存放多種型態
3. List裡面只能同時存放一種型態
4. List有個專屬的名字

3

List裡面的資料可以是任意型態，比如同時是整數、小數、字串等

## 請問下列哪一項會讓my\_list不是一個List？

1. my\_list = \[\]
2. my\_list = list\(\)
3. my\_list = input\(\).split\(\)
4. my\_list = input\(\)

4 

input\(\)回傳的結果是字串

## 請問下列創造List的方法，何者錯誤？

1. l = \[0\] \* 5
2. l = list\(range\(5\)\)
3. l = list\(\[0, 1, 2\]\)
4. l = list\[\]

4

沒有此語法

## 請問下列敘述何者錯誤？

1. a = input\(\), a為字串
2. b = input\(\).split\(\), b為list
3. c = range\(5\), c為list
4. d = list\(range\(5\)\), d為list

c

c不是list，是range

## 以下程式若輸入0 1 2 3 4，會輸出什麼？

```python
# input 0 1 2 3 4
my_list = input().split()
print(my_list)
```

1

```text
1 2 3 4 5
```

2

```text
['1', '2', '3', '4', '5']
```

3

```text
[1, 2, 3, 4, 5]
```

4

```bash
[1 2 3 4 5]
```

2

應注意input\(\)的結果會是string，split\(\)後的結果是string的list

## 請問下列程式會輸出什麼？

```python
my_list = list('apple')
print(my_list)
```

1. \['a', 'p', 'p', 'l', 'e'\]
2. \[a, p, p, l, e\]
3. \[apple\]
4. \['apple'\]

1

注意list\(\)會把字串一個字母一個字母切開

## 請問下列程式會輸出什麼？

```python
colors = ['red', 'orange', 'blue']

for color in colors:
    if color == 1:
        break
    print(color, end=' ')
    
for i in range(3):
    if i == 'orange':
        break
    print(colors[i], end=' ')

```

1. red orange blue red orange blue
2. red red
3. red orange blue red
4. red red orange blue

## 請問下列程式碼於第幾行會出現錯誤？

```python
for i in [0, 1, 2, 3, 4]:
    print(i)

for i in list('APPLE'):
    print(i)
    
for i in input().split():
    print(i)

```

1. 第1行
2. 第4行
3. 第7行
4. 以上皆非

4

in 後面可以接list，而三種寫法最終結果都是list，所以都不會發生錯誤

## 請問下列程式碼會輸出什麼？

```python
my_list = ['a', 'b', 'c', 'd', 'e']

print(my_list[1], end=' ')
print(my_list[-2], end=' ')

```

1. b d
2. a d
3. a c
4. b c

1

參考下圖

![](../../.gitbook/assets/image%20%28113%29.png)

## 請問下列程式會輸出什麼？

```python
students = ['ben', 'candy', 'denny']

for i in range(3):
    print(i, end=' ')
```

1. 0 1 2
2. ben candy denny
3. 0 ben 1 candy 2 denny
4. 1 ben 2 candy 3 denny

## 請問下列程式會輸出什麼？

```python
my_list = [0, 1, 2, 3, 4]

my_list[2] *= 9

print(my_list)

```

1. \[0, 1, 8, 3, 4\]
2. \[0, 9, 2, 3, 4\]
3. \[0, 2, 4, 6, 8\]
4. \[0, 1, 18, 3, 4\]

4



## 請問下列程式會輸出什麼？

```python
my_list = [0, 1, 2, 3, 4]

for i in range(5):
    my_list[i] = my_list[i] * my_list[i]

print(my_list)

```

1. \[0, 1, 4, 9, 16\]
2. \[0, 1, 2, 3, 4\]
3. \[0, 2, 4, 6, 8\]
4. \[1, 3, 5, 7, 9\]

1

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

