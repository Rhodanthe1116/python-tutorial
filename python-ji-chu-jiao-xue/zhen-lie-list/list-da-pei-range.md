# list 搭配 range

## **動動腦**

```python
print(list(range(2)))
# [0, 1]
print(list(range(3, 2, -1)))
# [3]
print(list(range(3, 2)))
# []
print(list(range(1, 5, 4)))
# [1]
print(list(range(-1, 1)))
# [-1, 0]
```

```python
for i in range(3)
# 下面這樣可以嗎？
for i in list(range(3))
```

## **for ... in …**

在for迴圈中，除了in range( ) 還能 in 很多東西：

```python
for i in '0', 0, 'z', 3.4 :
# 跑4次迴圈，且 i 分別代表 0 0 z 3.4，型態分別為str  int  str  float
```

```python
for color in 'red','green','blue':
    print(color)
```

```python
color = ['red','green','blue']
for e in color :
    print(e)
```

### 不能in:

```python
for i in 3:
# Error
for i in 3.4:
# Error

```

### **for ... in input().split()**

```python
a = input().split()
for d in a:
# 不會error，input會自動把數字轉成str的型態
```

還可以把input().split()直接寫在裡面：

```python
for d in input().split():
```

輸入: abc 123 0 x2

abc 123 0 x2 經過split()處理後變成\['abc', '123', '0', 'x2' ]

等同於

```python
for d in ['abc', '123', '0', 'x2' ]:
# 會跑4次迴圈，且 d 分別為'abc'  '123'  '0'  'x2'，型態皆為str
```

## **任務: 字串統計**

* 每次輸入一行，每組字串用空格間隔
* 請統計出總共有幾組字串，並將它們一行一行的輸出

```bash
# 範例輸入一
a b a
# 範例輸出一
a
b
a
有 3 個字串

# 範例輸入二

# 範例輸出二
有 0 個字串
```

### **參考解答**

```python
count = 0
for d in input().split():
    count += 1
    print(d)
print("有", count, "個字串")
```

## **任務: 數字加總**

* 每次輸入一行，每組數字皆為整數且用空格間隔
* 請將輸入的數字加總並輸出

```bash
# 範例輸入一
1 2 3 4
# 範例輸出一
10

# 範例輸入二
0 1 0 -2
# 範例輸出二
-1
```

### **參考解答**

```python
count = 0
for d in input().split():
    # 注意要轉型 
    count += int(d)
print(count)
```
