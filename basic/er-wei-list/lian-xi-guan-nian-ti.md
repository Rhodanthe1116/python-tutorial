# ⚡ 練習：觀念題

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

1

若照著程式模擬一遍，可以發現此程式其實是在將二維串列不斷的畫上斜線，如果遇到邊界則從當最左欄開始畫，直到畫了17個格子為止，最後l將變成：

```python
[1, 1, 1, 1, 0]
[0, 1, 1, 1, 1]
[0, 0, 1, 1, 1]
[1, 0, 0, 1, 1]
[1, 1, 0, 0, 1]
```

而其中l\[4]\[2]為並沒有被畫到，因此為0

C

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

1

利用第一種方法所創造出來的串列會指向同一個一維串列，請參考講義91頁的示意圖

C

## 期中 apcs

### 右側程式片段執行 後，count 的值 為何？

```python
maze = [
    [1, 1, 1, 1, 1],
    [1, 0, 1, 0, 1],
    [1, 1, 0, 0, 1],
    [1, 0, 0, 1, 1],
    [1, 1, 1, 1, 1]
]
count = 0
for i in range(1, 3+1):
    for j in range(1, 3+1):
        dir = [
            [-1, 0],
            [0, 1],
            [1, 0],
            [0, -1]
        ]
        for d in range(4):
            if maze[i+dir[d][0]][j+dir[d][1]] == 1:
                count += 1

print(count)

```

1. 3
2. 36
3. 12
4. 20

4

假設 x,y,z 為布林(boolean)變數 且 x=True, y=True, z=False，並定義符號

* ! 代表 not&#x20;
* && 代表 and
* || 代表 or&#x20;

請問下面各布林運算式的真假值依序為何？

* !(y || z) || x&#x20;
* !y || (z || !x)&#x20;
* z || (x && (y || z))&#x20;
* (x || x) && z