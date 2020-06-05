# ⚡ 練習：觀念題

## 右側程式片段執行 後，count 的值 為何？

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



