# 串列的新增

新增元素

![](<../../.gitbook/assets/image (69).png>)

1. 方法一:　append()
2. 方法二:　+

## append (元素):

串列的 append() 操作可將一個元素加入到串列的尾端

![](<../../.gitbook/assets/image (102).png>)

```python
record = ['rice', 'cake', 'noodle', 'fruit']
food = input()
record.append(food)
```

更多範例

```python
a = ['a', 'b']
a.append(2)
print(a)
# 輸出 ['a', 'b', 2]
```

## "+”運算子

串列的 "+”會將2個串列內的元素結合產生一個新串 列，因此我們可以將想要加入的元素先轉形成串列

```python
food = 'egg'
record = record + [food] # 新同學加入
```

![](<../../.gitbook/assets/image (80).png>)

也可以直接將input()放在中括號內

```python
record += [input()]
```

還有連加的操作

```python
record = record + [input()] + [input()]
```

更多範例

```python
a = ['a', 'b']
a += [2]
print(a)
# 輸出 ['a', 'b', 2]
```

## 練習時間

輸入一行有5個整數，每個整數間隔一個空格，請將這5個數都+10後存成串列再輸出

```bash
# 範例輸入:
17 36 48 80 77

# 範例輸出:
[27, 46, 58, 90, 87]
```
