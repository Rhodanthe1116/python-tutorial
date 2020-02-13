# 輸入 Input

```python
x = input()
print(x)
```

{% hint style="danger" %}
`input()之後的變數是一個`**`字串（string）`**`，並不是`**`數字（int）`**`，要用int()指令來將字串轉成數字才能做運算，如下：`
{% endhint %}

```python
x = input()
y = input()
print(x+y)

x = int(input())
y = int(input())
print(x+y)
```

{% hint style="info" %}
如果`int(input())`是輸入文字的話會發生什麼事...
{% endhint %}

## 一次輸入兩個變數

```python
x, y = input().split()
x = int(x)
y = int(y)
print(x, y)
```

## 一次輸入多個變數

```python
x, y, z = input().split()
x = int(x)
y = int(y)
z = int(z)
print(x, y, z)
```

