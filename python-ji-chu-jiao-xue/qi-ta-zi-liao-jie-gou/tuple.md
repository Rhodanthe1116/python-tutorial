# 元組 Tuple

\]跟 List 類似，差別在於，List 是可變的，Tuple 是不可變的，也就是說，Tuple 在創造之後便不可以被改變，可以用來維護重要的資料不因意外而被破壞

使用方法也和 List 類似，差別只有宣告時中括號`[]`變成小括號`()`

## 創造 Create

```python
t = ("apple", "banana", "cherry")
print(t)
```

或

```python
t = "apple", "banana", "cherry"
print(t)
```

## 取得 Access

```python
t = ("apple", "banana", "cherry")
print(t[1])
```

## 改變 Change 

{% hint style="danger" %}
不可像 List 一樣

```python
t = ("apple", "banana", "cherry")
t[1] = "orange"
```
{% endhint %}

但可利用`set()`函數，類似之前用過的`list()`，將 tuple 轉換成 list 後修改 list，再轉成 tuple

```python
x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)

print(x)
```

## 新增 Add

不可以新增

{% hint style="danger" %}
```python
t = ("apple", "banana", "cherry")
t[3] = "orange" # This will raise an error
print(t)
```
{% endhint %}

## 序列拆解 Sequence Unpacking

其實之前所用的多重指定就是利用 Tuple 來達成：

### 包裝 Packing

一串資料，稱作**序列 Sequence**，將其打包成 Tuple，稱作 **Packing**

```python
# tuple packing
t = 12345, 54321, 'hello!'
```

### 拆解 Unpacking

相反

```python
# unpacking
x, y, z = t
print(x, y, z)
```

Sequence unpacking 可以用在任何右邊是類似序列物件的時候，包含 Tuple 和 List

```python
# unpacking
x, y, z = (1, 2, 3)
print(x, y, z)
x, y, z = [1, 2, 3]
print(x, y, z)
```

運用**拆開序列運算符 Sequence unpacking operator**，可以將序列拆開，其實之前就有用過，就是`*`

```python
l = [0, 1, 2]
print(l)
print(*l)
t = (4, 5, 6)
print(t)
print(*t)
```

## 其他 Others

### 可變

雖然 Tuple 是不可變的，但他可以裝入可變的物件

```python
t = (["apple", "banana"], ["cherry", "orange"])
t[0][0] = "XXXXX"
print(t) 
```

```python
empty = ()

```

### 創造只含一元素

需要加上逗號，否則括號會被當作運算符號

```python
t = ("apple",)
print(type(t))

# NOT a tuple
t = ("apple")
print(type(t))
```

### 創造只含零元素

```python
t = ()
print(t)
print(len(t))
```

