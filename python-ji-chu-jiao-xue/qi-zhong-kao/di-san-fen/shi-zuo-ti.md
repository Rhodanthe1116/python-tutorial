# 實作題

## 流程控制 作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=a006" %}

基本的流程控制

```python
from math import sqrt
a, b, c = map(int, input().split())
if b*b-4*a*c>0:
    temp=sqrt(b*b-4*a*c)
    x1=(-b+temp)/(2*a)
    x2=(-b-temp)/(2*a)
    print("Two different roots x1=", int(x1), " , x2=", int(x2), sep='')
elif b*b-4*a*c ==0:
    temp=sqrt(b*b-4*a*c)
    x1=(-b)/(2*a);
    print("Two same roots x=", int(x1), sep='')
else:
    print("No real root")
```

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

## List（二維）TOI

{% embed url="https://toi-reg.csie.ntnu.edu.tw/question/202006/Orienteering.pdf" %}



{% embed url="https://zerojudge.tw/ShowProblem?problemid=f148" %}

會用到一些技巧，如ASCII和資料結構，但不用也可以慢慢寫完

```python
w, h = map(int, input().split())
n = int(input())
l = []
ans = []
cnt = 0
for i in range(26):
    ans.append([-1, -1])
for i in range(w):
    r = input().split()
    l.append(r)
for i in range(w):
    for j in range(h):
        c = l[i][j]
        index = ''
        if c == 'a':
            index = 0
        elif c == 'b':
            index = 1
        elif c == 'c':
            index = 2
        elif c == 'd':
            index = 3
        elif c == 'e':
            index = 4
        elif c == 'f':
            index = 5
        elif c == 'g':
            index = 6
        elif c == 'h':
            index = 7
        elif c == 'i':
            index = 8
        elif c == 'j':
            index = 9
        elif c == 'k':
            index = 10
        elif c == 'l':
            index = 11
        elif c == 'm':
            index = 12
        elif c == 'n':
            index = 13
        elif c == 'o':
            index = 14
        elif c == 'p':
            index = 15
        elif c == 'q':
            index = 16
        elif c == 'r':
            index = 17
        elif c == 's':
            index = 18
        elif c == 't':
            index = 19
        elif c == 'u':
            index = 20
        elif c == 'v':
            index = 21
        elif c == 'w':
            index = 22
        elif c == 'x':
            index = 23
        elif c == 'y':
            index = 24
        elif c == 'z':
            index = 25
        else:
            continue
        ans[index][0] = i
        ans[index][1] = j
        cnt += 1


if cnt < n:
    print("Mission fail.")
else:
    cnt = n
    for i in range(26):
        if (ans[i][0] != -1):
            cnt -= 1
            print(*ans[i])
            if cnt == 0:
                break
```

## List（二維）TOI

{% embed url="https://toi-reg.csie.ntnu.edu.tw/question/202006/Detector.pdf" %}



{% embed url="https://zerojudge.tw/ShowProblem?problemid=f149" %}

```python
r, c = map(int, input().split())
l = []
for i in range(r):
    a = list(map(int, input().split()))
    l.append(a)
ok = 0
no = 0
total = 0
dir = [
    [-1, -1],
    [-1, 0],
    [-1, 1],
    [0, -1],
    [0, 1],
    [1, -1],
    [1, 0],
    [1, 1],
]
for i in range(r):
    for j in range(c):
        if l[i][j] == 0:
            continue
        elif l[i][j] == 1:
            total += 1
            continue
        elif l[i][j] == 5:
            for d in dir:
                if 0 <= i+d[0] and i+d[0] < r and 0 <= j+d[1] and j+d[1] < c:                        
                    if l[i+d[0]][j+d[1]] == 5 or l[i+d[0]][j+d[1]] == 4:
                        l[i][j] = 4
for i in range(r):
    for j in range(c):
        if l[i][j] == 0:
            continue
        elif l[i][j] == 1:
            for d in dir:
                if 0 <= i+d[0] and i+d[0] < r and 0 <= j+d[1] and j+d[1] < c:                        
                    if l[i+d[0]][j+d[1]] == 5:
                        ok += 1
                        break
print(ok, total - ok)
```

## 參考

{% embed url="https://toi-reg.csie.ntnu.edu.tw/tasks.php" %}



