# 串列 List

## 示意圖

![](../../.gitbook/assets/image%20%2894%29.png)

## 語法

```python
data = ['a', 'b', 'z', 'f', 'g']
```

## **串列中可以放**

```python
# 整數(int):
data = [1, 2, -7, 10, 0, 0, 0]

# 浮點數(float):  
data = [1.0, 2.5, -7.2, 0.3]

# 字串(str):  
data = ['a', 'b', 'z', 'f', 'g']

# ...

# 可以同時都塞進去唷:  
data = ['a', 3, '7', 2.5, -4]
```

## 宣告

![](../../.gitbook/assets/image%20%2873%29.png)

```python
# 三種方式宣告
data = [] # Ex: ['a', 3, '7', 2.5, -4]
data = list()
data = input().split()
```

### **\[ \] 宣告**

在用\[\]宣告時每個元素中間要用 , 來區隔唷!

```python
data = [元素0, 元素1, 元素2]
```

也可以搭配 \* 來宣告

```python
data = ['a']*5
# 等同於 data = ['a', 'a', 'a', 'a', 'a']
```

### list\(\) 宣告

```python
data = list( ) 
# print(data) =>  []
data = list(('a', 3, '7', 2.5)) 
# print(data) =>  ['a', 3, '7', 2.5]
data = list("12ab")
# print(data) =>  ['1', '2', 'a', 'b']
```

## 練習

1. 宣告一個具有5個元素的串列
2. 使用\[ \] 宣告一個具有100個相同元素的串列
3. 使用list將一組字串變成串列的模式

