# ⚡ 練習：觀念題（題目）

## 請問下列程式碼會輸出什麼？

```python
l = [
    [0, 0, 0, 0, 0],
    [0, 0, 0, 0, 0],
    [0, 0, 0, 0, 0],
    [0, 0, 0, 0, 0],
    [0, 0, 0, 0, 0]
]
n = len(l)
cnt = 17
for j in range(n):
    for i in range(n):
        l[i][(i + j) % n] = 1
        cnt -= 1
        if cnt == 0:
            break
    if cnt == 0:
        break
    
print(l[4][2])

```

1. 0
2. 1
3. 2
4. 3

## 在Python中有多種方法可以建立二維串列，請問下列程式碼中，想要建立一個7 \* 9且值皆為0的二維串列，，哪一種方法較為錯誤？

```python
n = 7
m = 9

# 1.
l1 = [[0] * m] * n

# 2.
l2 = [0] * n
for i in range(n):
    l2[i] = [0] * m
    
# 3.
l3 = []
for i in range(n):
    l3.append([0] * m)

# 4.
l4 = [[0] * m for i in range(n)]
```

1. 1
2. 2
3. 3
4. 4

