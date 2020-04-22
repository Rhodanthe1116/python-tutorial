# 第三份



## list 作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=d573" %}

考list對資料處理的基本操作，和面對不同數量級測資。

```python
import sys
for inputString in sys.stdin:
    n = int(inputString)
    groupOfKnight = [0] * (100000 + 1)
    for _ in range(n):
        newLine = list(map(int, input().split()))
        groupNumber = newLine[0]
        p = newLine[1]
        knights = newLine[2:]

        for knight in knights:
            groupOfKnight[knight] = groupNumber
            
    y = int(input())
    print(groupOfKnight[y])
```

