# 二維串列使用者輸入

## append() 與 +

```python
n = int(input())
data = []
for i in range(n):
    data.append(input().split())
    # 或data += [input().split()]
print(data)
```

## 元素轉型

```python
n = int(input())
data = []
for i in range(n):
    data.append([int(e) for e in input().split()])
    # 或data += [[int(e) for e in input().split()]]
print(data)
```

## 一行寫法

```python
n = int(input())
data = [[int(e) for e in input().split()] for i in range(n)]
print(data)
```
