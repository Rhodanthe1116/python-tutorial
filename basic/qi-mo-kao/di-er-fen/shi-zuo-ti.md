# 實作題

### 2d list

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e838" %}

```cpp
#include <stdio.h>

int main()
{
    int n = 0;
    char map[101][101] = {}; 
    char bomb[101][101] = {}; 

    scanf("%d", &n);
    for (int i = 0; i < n; i += 1) {
        for (int j = 0; j < n; j += 1)
            scanf(" %c", &map[i][j]);
    }

    for (int i = 0; i < n; i += 1) {
        for (int j = 0; j < n; j += 1)
            bomb[i][j] = '0';
    }

    for (int i = 0; i < n; i += 1) {
        for (int j = 0; j < n; j += 1) {
            if (map[i][j] == '*') {
                for (int k = 0; k < n; k += 1) {
                    bomb[i][k] = '*';
                    bomb[k][j] = '*';
                }
            }
        }
    }

    for (int i = 0; i < n; i += 1) {
        for (int j = 0; j < n; j += 1)
            printf("%c", bomb[i][j]);
        printf("\n");
    }
}
```

## class

{% embed url="https://zerojudge.tw/ShowProblem?problemid=d093" %}



## toi dict counting sort 非作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e809" %}

```python
order = input()
s = input()
q = int(input())

d = {}
for c in s:
    if c in d:
        d[c] += 1
    else:
        d[c] = 1

for i in range(q):
    sum = int(input())
    for c in order:
        if not c in d:
            d[c] = 0
        sum -= d[c]
        if sum <= 0:
            print(c)
            break
```

## dfs 窮舉

{% embed url="https://zerojudge.tw/ShowProblem?problemid=f168" %}

若沒剪枝會有25%測資TLE

```python
def dfs(l, cnt, p1, p2, p3):
    if p1 > sum(l)/3 or p2 > sum(l)/3 or p3 > sum(l)/3:
        return False
    
    if cnt == len(l) and p1 == p2 and p2 == p3:
        return True
    
    if not cnt < len(l):
        # print(cnt, p1, p2, p3)
        return False
    
    
    a = dfs(l, cnt+1, p1+l[cnt], p2, p3)
    b = dfs(l, cnt+1, p1, p2+l[cnt], p3)
    c = dfs(l, cnt+1, p1, p2, p3+l[cnt])
    return a or b or c

n = input()
l = list(map(int, input().split()))

if dfs(l, 0, 0, 0, 0):
    print('YES')
else:
    print('NO')


```
