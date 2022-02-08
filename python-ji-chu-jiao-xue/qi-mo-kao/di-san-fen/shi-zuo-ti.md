# 實作題

## dict 桃竹苗學科 非作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=b563" %}

## toi sort key 非作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e800" %}

## toi 2d list 非作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e838" %}



## sort greedy 非作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=d555" %}

```python
t = 1
while True:
    try:           
        n = int(input())
        a = []
        for i in range(n):
            ta, tb = map(int, input().split())
            p = [ta, tb]
            a.append(p)
        a = sorted(a, key=lambda p: (-p[0], -p[1]))
        
        ans = []
        mx = -1
        for i in range(n):
            if (a[i][1] > mx ):
                ans.append(a[i])
                mx = a[i][1]
        ans = list(reversed(ans))
        print(f'Case {t}:')
        print(f'Dominate Point: {len(ans)}')
        for k, v in ans:
            print(f'({k},{v})')
        t+=1
    except:
        break
```
