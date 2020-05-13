# 巢狀迴圈 Nested Loop

## 巢狀迴圈

巢狀迴圈，迴圈裡面放迴圈，可用九九乘法來想

```python
for i in range(1, 10):
    for j in range(1, 10):
        print(i, "*", j, "=", i * j)
    print()
```

![](../../.gitbook/assets/image%20%2816%29.png)

![](../../.gitbook/assets/image%20%2829%29.png)

類似兩層sigma

$$
\sum_{i = 1}^{n = 9}\sum_{j = 1}^{m = 9} i * j
$$

{% embed url="https://www.youtube.com/watch?v=1LCBssxhduU" caption="1:16" %}

另外一種清楚的表示法

```python
for i in range(10):
    print("i =", i, ", j = ", end="")
    for j in range(3):
        print(j, end=", ")
    print()
```

## break, continue and nested loop

break 跟 continue 只會跳離或繼續最近的一圈迴圈！

```python
for i in range(5):
    print("i = ", i, end=' ')
    for j in range(3):
        print("j = ", j)
        break
```

