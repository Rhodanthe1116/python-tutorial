# 參數傳遞 Parameter

參數傳遞有一些需要特別注意，在此之前先介紹一個觀念：

## 物件 Object

在 Python 中，所有東西都是一個物件 Object，我們之前所創造出來的數字、字串、串列也都是物件，而每個物件有：

| Name | Description | Example1 | Example2 |
| :--- | :--- | :--- | :--- |
| Value | 值 | `1000` | `"apple"` |
| Type | 類型 | `int` | `string` |
| ID | 唯一識別，類似地址或身分證，對應記憶體位置 | `1574558016` | `140135852055856` |

可用內建函數來取得：

```python
a = 1000
print(type(a))
print(id(a))

s = "apple"
print(type(s))
print(id(s))
```

可用`is`來比較 ID 以確認兩者是不是一樣：

```python
x = "apple"
y = "apple"
print(id(x))
print(id(y))
print(x is y)
```

其實變數名稱只是一個指向物件的代稱

![](../../.gitbook/assets/23.gif)

```python
print(id(10)); print()

x = 10
y = x
print(id(x))
print(id(y))
```

## 可變物件和不可變物件 Mutable v.s. Immutable

在 Python 中，物件可以分成**可變 mutable** 和**不可變 immutable，**差別在於創造之後還可不可以改變其值。

![](../../.gitbook/assets/image%20%2819%29.png)



### 可變物件 M**utable Object**

```python
l = [0, 1, 2, 3, 4]
print(id(l))
l[1] = 999
print(id(l))
```

可以改變值但 id 不變

### 不可變物件 Imm**utable Object**

改變值但 id 變了，其實是新創一個物件叫做 2 然後再改指向

```python
i = 1
print(id(i))
i = 2
print(id(i))
```

改變值但 id 變了，其實是新創一個物件叫做 2 然後再改指向，如下：

![](../../.gitbook/assets/2.gif)

## 參數傳遞

若想傳參數給函數，可分成可改變跟不可變兩種情形：

### 傳可變物件

直接傳同個物件，在函數中的改變會對原本的物件做改變

```python
def my_function(ly):
    ly[0] = 999
    print("after ly[0] = 999")
    
lx = [0, 1, 2, 3, 4]
print("lx =", lx)
my_function(lx)
print("lx =", lx)
```

實際上情況類似於：

![](../../.gitbook/assets/m.gif)

### 傳不可變物件

```python
def my_function(y):
    y = 999
    print("after y = 999")
    
x = 0
print("x =", x)
my_function(x)
print("x =", x)
```

實際上情況類似於：

![](../../.gitbook/assets/im.gif)

