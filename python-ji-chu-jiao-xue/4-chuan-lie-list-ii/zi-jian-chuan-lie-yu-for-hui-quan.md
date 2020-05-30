# 自建串列與for迴圈

## for與list回顧

還記得for 與list的搭配嗎

```python
data = input().split()
for d in data:
    a = int(d)
```

透過for迴圈與int\(\)，可以依序取得 data內的元素且為整數形態

![](../../.gitbook/assets/image%20%2877%29.png)

![](../../.gitbook/assets/image%20%2888%29.png)

## append\(\) 或 + 搭配for迴圈

```python
data = []
for d in input().split():
      data.append(int(d))
```

或

```python
data = []
for d in input().split():
      data += [int(d)]
```

## 任務:串列新增

* 輸入一串數字，每個數字間隔一個空白，請建立一個整數形態的串列並輸出。
* 接著讓使用者輸入一個數，表示想在該串列中，再加入的數字數量。
* 一行輸入一個，依序輸入，最後再以數字形態輸出結果。

```bash
# 範例輸入:
80 16
2
5
71

# 範例輸出:
[80, 16]
[80, 16, 5, 71]
```

```bash
# 範例輸入:
80 16
3
10
20
30

# 範例輸出:
[80, 16]
[80, 16, 10, 20, 30]
```

```bash
# 範例輸入:
-1
2
0
0

# 範例輸出:
[-1]
[-1, 0, 0]
```

