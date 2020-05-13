# for 迴圈

![](../../.gitbook/assets/image%20%285%29.png)

![](../../.gitbook/assets/image%20%2827%29.png)

## **while到for**

![](../../.gitbook/assets/image%20%2815%29.png)

![](../../.gitbook/assets/image%20%2842%29.png)

簡單範例

```python
for i in range(6):
    print(i)
```

實際範例

**數數小生，從 1 數到 10 :**

```python
for count in range(1, 10  , 1):
    print(count , end=' ')
print('!')
```

```bash
# 輸出？

```

**數數能手，從 10 數到 1 :**

```python
for count in range(10, 1  ,-1):
    print(count , end=' ')
print('!')
```

```bash
# 輸出？

```

## **練習 : 數數大師**

**請試著使用 for … in range\(x, y, z\) : 來數數**

1. **請印出 0 1 2 3 4 5 6 7 8 9 !**
2. **請印出 1 3 5 7 9 11 13 15 17 19 !**

{% hint style="info" %}
**\#hit : e\(x, y, z\)， x 是開頭、 y 是結尾\( 不含 y \)、z 是公差**
{% endhint %}

\*\*\*\*

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

