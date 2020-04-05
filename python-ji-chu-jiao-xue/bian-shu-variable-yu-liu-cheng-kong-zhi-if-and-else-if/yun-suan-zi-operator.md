# 算數運算子 Arithmetic Operators

## 變數的運算：運算子（operator）

也就是運算符號

| 運算子 | 描述 | 例子 | 結果 |
| :--- | :--- | :--- | :--- |
| `+` | 加 | 1 + 1 | 2 |
| `-` | 減 | 1 - 1 | 0 |
| `*` | 乘 | 1 \* 2 | 2 |
| `/` | 除 | 5 / 3 = 1.7 | 1.7 |
| `%` | 除法取餘數 | 5 % 3 \(5 / 3 = 1...2\)  | 2 |
| `//` | 除法取整數 | 5 // 3 \(5 / 3 = 1...2\)  | 1 |
| `**` | 次方 | 2 \*\* 3 | 8 |

### 數字的運算

```python
x = 7
y = 5
print(x+y)    # 運算
print()

z = x + y     # 運算後存變數
print(z)
print()

add = x + y    # 加(Addition)
sub = x - y    # 減(Subtraction)
mul = x * y    # 乘(Multiplication)
div = x / y    # 除(Division)
print(add)
print(sub)
print(mul)
print(div)
print()

mod = x % y        # 取餘數(模)(Modulus)
power = x ** y     # 次方(Power)
floor = x // y     # 取整數(Floor division)
print(mod)         # 7 / 5 = 1 ... 2   
print(power)
print(floor)
print()
```

### 變數自己運算

```python
x = 5
x = x + 2
print(x)
```

### 字串的運算

字串可以做加跟乘

```python
str1 = "hello, "
str2 = "world"
add = str1 + str2
print(add)

add = str1 + str2     #加(Addition)
mul = str1 * 3        #乘(Multiplication)
print(add)
print(mul)
print()
```

### 注意字串與數字的分別

```python
a = 100
b = 50
print(a + b)

str1 = "100"
str2 = "50"
print(str1 + str2)
```

{% hint style="info" %}
可以用`int()`指令來轉換型態，把`string`轉成`int`
{% endhint %}

```python
# int()指令可以把"100"轉成int
a = int("100")    
b = 50
print(a + b)
```

也有這種用法

```python
name = "Benson"
print("hi, " + name)
```

## 運算的優先順序

跟數學一樣，先乘除，後加減，與括號優先

