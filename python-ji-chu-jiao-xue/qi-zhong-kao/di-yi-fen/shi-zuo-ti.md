# 實作題

## 流程控制 作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=d584" %}

照著題目好好做就可以拿到分數，但題目較複雜，可能會花比較多的時間看題目。

```python
import sys
for ss in sys.stdin:
    role, level = map(int, ss.split())
    point = 0

    # level up
    if level > 10 and role is not 0:
        point += 3 * (level - 10)
    if role is 2 and level > 8:
        point += 3 * (min(level, 10) - 8)

    # upgrade role
    if role is not 0:
        if level >= 8 and role is 2:
            point += 1
        if level >= 10 and role is not 2:
            point += 1
        if level >= 30:
            point += 1
        if level >= 70:
            point += 1
        if level >= 120:
            point += 3

    print(point)
```

## list 作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=d562" %}

考怎麼運用list的操作，可以用內建函數，也可以自己用for跑，如果寫過的話不會花太多時間。

```python
import sys
for ss in sys.stdin:
    n = int(ss)
    l = list(map(int, input().split()))

    print(*l)
    
    for _ in range(n-1):
        l.reverse()
        l.pop()
        print(*l)
```

## list 二進位

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e799" %}

需要有二進位的觀念，其他照著做即可，主要要花時間處理進位轉換。

```python
import sys
for input_string in sys.stdin:
    n, m = map(int, input_string.split())
    symbol = input()

    for _ in range(n):
        num = int(input())

        binary_num = [0] * m
        for i in range(m):
            if (num % 2 == 1):
                binary_num[-i-1] = 1
            num = int(num / 2)

        for digit in binary_num:
            if digit == 0:
                print('.', end=' ')
            elif digit == 1:
                print(symbol, end=' ')
        print()

```

## 二維list TOI

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e787" %}

二維list的基本操作，以及比較複雜的行列關係。

```python
import sys
for ss in sys.stdin:
    n, m = map(int, ss.split())

    treasure_map = []
    for i in range(n):
        new_row = list(map(int, input().split()))
        treasure_map.append(new_row)

    # 注意：兩張圖之間有個空格
    input()
    
    transforming_map = []
    for i in range(n):
        new_row = list(map(int, input().split()))
        transforming_map.append(new_row)

    for i in range(n):
        for j in range(m):
            sum_of_row_and_column = 0
            # 算行
            for ii in range(n):
                sum_of_row_and_column += transforming_map[ii][j]
            # 算列
            for jj in range(m):
                sum_of_row_and_column += transforming_map[i][jj]
            # 扣掉重複的
            sum_of_row_and_column -= transforming_map[i][j]

            if sum_of_row_and_column % 2 == 1:
                treasure_map[i][j] = int(not treasure_map[i][j])

    for row in treasure_map:
        print(*row)

```
