# 實作題

改自B卷，觀念題直接複製B卷的，實作題1\~3題重新挑，皆為作業1星題，第4題為原B卷的第三題，作為挑戰題（以經驗來說學生很難解出來）

## APCS分數對照&#x20;

* 1\~3題分數 \* 70，共210分，若前三題都滿分可以三級分&#x20;
* 第4題不變，四題全對最高310，可得四級分

## 作業 if

{% embed url="https://zerojudge.tw/ShowProblem?problemid=d460" %}

```python
y = int(input())
if 0 <= y and y <= 5: print(0)
elif 6 <= y and y <= 11: print(590)
elif 12 <= y and y <= 17: print(790)
elif 18 <= y and y <= 59: print(890)
else: print(399)
```



## 作業迴圈+if

{% embed url="https://zerojudge.tw/ShowProblem?problemid=d070" %}



```python
while True:
    y = int(input())
    if y == 0:
        break
    if (y % 400 != 0 and y % 100 == 0):
        print("a normal year")
    elif y % 4 == 0:
        print("a leap year")
    else:
        print("a normal year")
```

提示：按照題目，如果y不是400的倍數且y是100的倍數，則y是平年；否則如果y是4的倍數，則y是閏年；其餘都是平年

## 作業 list

{% embed url="https://zerojudge.tw/ShowProblem?problemid=b294" %}

更多測資：

```
5
3 2 4 8 1

# output
56

# 解釋
3*1 + 2*2 + 4*3 + 8*4 + 1*5 = 56
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
