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

## 二維list 作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=a015" %}

考最基本的輸入輸出跟索引

```python
import sys
for ss in sys.stdin:
    row, column = map(int, ss.split())
    l = []
    for i in range(row):
      new_row = list(map(int, input().split()))
      l.append(new_row)

    for j in range(column):
      for i in range(row):
        print(l[i][j], end=' ')
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

## list TOI

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e836" %}

比較進階的list，需要紀錄以前輸入的資料，並找最大值。也可利用兩個list做key跟value的map。下列是直接建一個全部數字的頻率的表，index代表數字，value代表頻率，也可達到相同的效果。

```python
import sys
for ss in sys.stdin:
    n = int(ss)
    input_numbers = list(map(int, input().split()))
    frequency = [0] * 20000
    for input_number in input_numbers:
        input_number += 9999
        frequency[input_number] += 1

    max_frequency = 0
    number_of_different = 0
    for number in range(20000):
      if frequency[number] > 0:
        number_of_different += 1
      max_frequency = max(max_frequency, frequency[number])
    print(number_of_different)

    if max_frequency <= 1:
        print('NO')
    else:
      for input_number in input_numbers:
          input_number += 9999
          # -1 代表已輸出過
          if frequency[input_number] == -1:
            continue
          if frequency[input_number] == max_frequency:
              frequency[input_number] = -1
              print(input_number - 9999, end=' ')

      print()
```
