# ⚡ 練習：上機實作

## ⭐

{% embed url="https://zerojudge.tw/ShowProblem?problemid=d460" %}

```python
y = int(input())
if 0 <= y and y <= 5: print(0)
elif 6 <= y and y <= 11: print(590)
elif 12 <= y and y <= 17: print(790)
elif 18 <= y and y <= 59: print(890)
else: print(399)
```

{% embed url="https://zerojudge.tw/ShowProblem?problemid=a003" %}

照著題目邏輯寫語法

```python
m, d = input().split()
m = int(m)
d = int(d)
s = (m * 2 + d) % 3
if s == 0:
    print('普通')
elif s == 1:
    print('吉')
elif s == 2:
    print('大吉')
```

{% embed url="https://zerojudge.tw/ShowProblem?problemid=b877" %}

要想一下規則

```python
a, b = map(int, input().split())
if b >= a:
    print(b - a)
else:
    print(100-a+b)
```

## ⭐⭐

{% embed url="https://zerojudge.tw/ShowProblem?problemid=b758" %}

```python

```

{% embed url="https://zerojudge.tw/ShowProblem?problemid=d066" %}

```python
hh, mm = input().split()
hh = int(hh)
mm = int(mm)
sum = hh * 60 + mm
if sum >= 450 and sum < 1020: print("At School")
else: print("Off School")
```

## ⭐⭐⭐

{% embed url="https://zerojudge.tw/ShowProblem?problemid=a006" %}

#### 一行輸入法

```python
a, b, c = input().split()
a = int(a)
b = int(b)
c = int(c)
```

#### 進階方法：

```python
a, b ,c = map(int, input().split())
```

#### 開根號

```python
import math
print(math.sqrt(4))
```

```python
from math import sqrt
a, b, c = map(int, input().split())
if b*b - 4*a*c > 0:
    temp = sqrt(b*b-4*a*c)
    x1 = (-b+temp) / (2*a)
    x2 = (-b-temp) / (2*a)
    print("Two different roots x1=", int(x1), " , x2=", int(x2), sep='')
elif b*b-4*a*c == 0:
    temp = sqrt(b*b - 4*a*c)
    x1 = (-b) / (2*a);
    print("Two same roots x=", int(x1), sep='')
else:
    print("No real root")
```

