# If

還記得比較運算子嗎？

### 比較運算子（Comparison Operators）

| 運算子 | 名稱 | Example | Try it |
| :--- | :--- | :--- | :--- |
| == | 等於 | x == y | [Try it »](https://www.w3schools.com/python/showpython.asp?filename=demo_oper_compare1) |
| != | 不等於 | x != y | [Try it »](https://www.w3schools.com/python/showpython.asp?filename=demo_oper_compare2) |
| &gt; | 大於 | x &gt; y | [Try it »](https://www.w3schools.com/python/showpython.asp?filename=demo_oper_compare4) |
| &lt; | 小於 | x &lt; y | [Try it »](https://www.w3schools.com/python/showpython.asp?filename=demo_oper_compare5) |
| &gt;= | 大於等於 | x &gt;= y | [Try it »](https://www.w3schools.com/python/showpython.asp?filename=demo_oper_compare6) |
| &lt;= | 小於等於 | x &lt;= y | [Try it »](https://www.w3schools.com/python/showpython.asp?filename=demo_oper_compare7) |

## if

```python
a = 33
b = 200
if b > a:
  print("b 大於 a")
```

## 縮排

{% hint style="danger" %}
```python
a = 33
b = 200
if b > a:
print("b is greater than a") # you will get an error
```
{% endhint %}

## if...else

```python
a = 200
b = 33
if b > a:
  print("b 大於 a")
else:
  print("b 小於等於 a")
```

## if...elif

if...else if

```python
a = 200
b = 33
if b > a:
  print("b 大於 a")
elif a == b:
  print("a 和 b 相等")
```

## if...elif...else

if...else if...else

```python
a = 200
b = 33
if b > a:
  print("b 大於 a")
elif a == b:
  print("a 和 b 相等")
else:
  print("a 大於 b")
```

## 一行if

如果只有後面只有一行指令可以寫成一行

```python
a = 33
b = 200
if a > b: print("b 大於 a")
```

{% hint style="danger" %}
不行

```python
a = 33
b = 200
if a > b: print(1)
    print(2)
```
{% endhint %}

## 且、或

還記得邏輯運算子嗎？

#### 邏輯運算子（Logical Operators）

| 運算子 | 說明 | 範例 | Try it |
| :--- | :--- | :--- | :--- |
| and  | 且 | x &lt; 5 and  x &lt; 10 | [Try it »](https://www.w3schools.com/python/showpython.asp?filename=demo_oper_logical1) |
| or | 或 | x &lt; 5 or x &lt; 4 | [Try it »](https://www.w3schools.com/python/showpython.asp?filename=demo_oper_logical2) |
| not | 否 | not\(x &lt; 5 and x &lt; 10\) | [Try it »](https://www.w3schools.com/python/showpython.asp?filename=demo_oper_logical3) |

```python
if a > 10 and b > 10:
  print("a和b都大於10")

if a > 10 or b > 10:
  print("a或b至少有一個大於10")
```

## 

