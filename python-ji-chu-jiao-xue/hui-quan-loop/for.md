# For

先介紹另一個東西

### range\(\)

指定一個範圍，`range(6)`代表 0 ~ 5

{% hint style="warning" %}
`range(6)` 是 0 ~ 5，不是1 ~ 6！
{% endhint %}

### for

類似數學中的 sigma

$$
\sum_{i=0}^{n = 5} i
$$

對於一個範圍中的每一個目標，都做某一件事

例如：對於每個在 \[0, 5\] 的整數（0, 1, 2, 3, 4, 5），都輸出此數字

```python
for i in range(6):
    print(i)
```

或加總，等同於sigma

```python
sum = 0
for i in range(6):
    sum += i
print(sum)
```

更改起始值：

```python
for i in range(2, 6):
    print(i)
```

類似等差：

```python
for i in range(2, 30, 3):
    print(i)
```

## break

跟 while 介紹的一樣

```python
for i in range(6):
    if i == 3:
        break
    print(i) 
```

## continue

跟 while 介紹的一樣

```python
for i in range(6):
    if i == 3:
        continue
    print(i) 
```

## Tip

for ‌跟 in 中間不一定只能放 i，也可以放任何其他變數，也可以不放東西，用`_`表示不放

```python
for _ in range(3):
    print("*")
```

以下僅供參考

```python
x, _, y = (1, 2, 3) # x = 1, y = 3 
x, *_, y = (1, 2, 3, 4, 5) # x = 1, y = 5 
for _ in range(10):     
    do_something()
for _, val in list_of_tuple:
    do_something()
```

