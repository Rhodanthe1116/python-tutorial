# 二維串列建立

串列內可放的元素:

* 整數\(int\)
* 浮點數\(float\)
* 字串\(str\)
* **串列\(list\)**
* **...**

## 二維串列建立方法

1. \[\]
2. append\(\)、 +
3. 中括號內建立

## 中括號宣告

### Before

1. \[元素0, 元素1, 元素2\]
2. \[ \]搭配 \* 來宣告

如

```python
['a']*5 == ['a', 'a', 'a', 'a', 'a']
```

### Now:

1. \[元素0, 元素1, 元素2\]，元素可為串列

錯誤：

![](../../.gitbook/assets/image%20%2893%29.png)

原因：會改到同一個

```python
data = [[0]*5]*3
print(data)
data[0][2] = 9
print(data)
```

```bash
# 輸出
[[0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0]]
[[0, 0, 9, 0, 0], [0, 0, 9, 0, 0], [0, 0, 9, 0, 0]]
```

![](../../.gitbook/assets/image%20%2870%29.png)

## 運用 for 迴圈

```python
data = [0]*3
for i in range(len(data)):
    data[i] = [0]*5
data[0][2] = 9
print(data)
```

```bash
# 輸出
[[0, 0, 9, 0, 0],
[0, 0, 0, 0, 0],
[0, 0, 0, 0, 0]]
```

![](../../.gitbook/assets/image%20%2874%29.png)

## append\(\) 和 +

假設 

```python
元素 = [1, 2, 3]
```

### append\(\): 直接在括號內加入想要的元素

```python
a = ['a', 'b']
a.append(元素)
print(a)
```

```bash
# 輸出:
['a', 'b', [1, 2, 3]]
```

### + : 需為串列形態

```python
a = ['a', 'b']
a += [元素]
print(a)
```

```bash
# 輸出:
['a', 'b', [1, 2, 3]]
```

### 範例

建立一個 3\*5 的二維串列

```python
data = []
x = 5
y = 3
for i in range(y):
    data.append([0]*x)
print(data)
data[2][1] = -1
print(data)
```

注：`data.append([0]*x)` 換成 + 也可以:

```python
data += [[0]*5]
```

```bash
# 輸出:
[[0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0]]
[[0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, -1, 0, 0, 0]]
```

## 中括號內建立

一維串列建立:

```python
data = [int(d) for d in input().split()]
```

二維串列建立\(3\*5 的二維串列\):

```python
data = [[0]*5 for i in range(3)]
```

## 整理：二維串列建立

### 第一種:

```python
data = [[0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0]]
```

### 第二種:

```python
data = [0]*3
for i in range(len(data)):
    data[i] = [0]*5
```

### 第三種:

```python
data = []
for i in range(3):
    data.append([0]*5)
```

或

```python
data = []
for i in range(3):
    data += [[0]*5]
```

## 第四種:

```python
data = [[0]*5 for i in range(3)]
```

## 練習時間

輸入一行有2個整數代表二維串列的大小，每個整數間隔一個空格，請輸出一個每個元素都是 -1 且符合輸入大小的二維串列

```bash
# 範例輸入
2 5

# 範例輸出:
[[-1, -1, -1, -1, -1], [-1, -1, -1, -1, -1]]
```



