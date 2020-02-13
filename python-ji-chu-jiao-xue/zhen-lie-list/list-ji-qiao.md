# List 技巧

## 輸入未知大小的 List 並轉成 int

例如輸入

```python
1 2 3 4 5
1 2 3 4 5 6 7
1 2 3
```

都可以用：

```python
 l = list(map(int, input().split()))
```

有點複雜...

### 拆解

已知

#### split\(\)

```python
l = input().split()
print(l)
```

會利用空白分割並存成一字串 list，但我們需要數字 list

#### map\(\)函數

會對所有成員都執行同一個函數

```python
map(int, ["1", "2", "3"])
```

類似於

```python
l = ["1", "2", "3"] 
for elem in l:
    elem 
```

#### list\(\)

將map後的東西變成list

### 所以

```python
 l = list(map(int, input().split()))
```

代表將輸入分開，並將所有元素轉成int，在把它存成list



