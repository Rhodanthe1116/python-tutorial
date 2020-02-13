# ⚡ 練習：觀念題

### 1

```python
for i in range(100000, n):
    for j in range(i-100, 1000, -1):
        print(i, j)
```

### 2

```python
for i in range(10**8):
    x = int(input())
    print(x**2)
```

### 3

```python
i = 1
while i < n:
    for j in range(i, n, i):
        l[j] += l[j-i]
    i *= 2
```

### 4

```python
def f(n):
    if n == 0: return 1
    else: return f(n-1) * n
```

### 5

```python
def f(i):
    if i == n: return
    
    v[i] = 0
    f(i+1)
    
    v[i] = 1
    f(i+1)
    
    v[i] = 2
    f(i+1)
```

#### 解答 <a id="&#x89E3;&#x7B54;"></a>

1. $$O(n^2) $$
2. $$O(1)$$ 
3. $$O(n) (n+\frac{n}{2}+\frac{n}{4}+...\approx 2n)$$ 
4. $$O(n)$$
5. $$ O(3^n)$$，可以看成此函數在窮舉一個有 n 項的數字，其中每一項可能為0,1,2，根據重複排列得知有3^n 種

