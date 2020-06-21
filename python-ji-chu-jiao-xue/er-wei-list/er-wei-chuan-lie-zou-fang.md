# 二維串列走訪

![](../../.gitbook/assets/image%20%2882%29.png)

## 複習：一維串列走訪

```python
for i in range():
# 或
for i in list:
```

## len\(\)函式在二維串列中

```python
data = [[17, 36, 48, 87, 63], [92, 73, 64, 33, 81], [88, 76, 32, 55, 47]]
print(len(data))
# 黃色的長度，輸出3
print(len(data[0]))
# 一段藍色的長度，輸出5
```

![](../../.gitbook/assets/image%20%2878%29.png)

## range\(\)走訪

```python
data = [[17, 36, 48, 87, 63],
        [92, 73, 64, 33, 81],
        [88, 76, 32, 55, 47]]
for i in range(len(data)):
    for j in range(len(data[i])):
        print(data[i][j], end=' ')
        
# 輸出 
# 17 36 48 87 63 92 73 64 33 81 88 76 32 55 47

# 注:
# len(data) == 3
# len(data[0]) == 5
```

## list 走訪

```python
data = [[17, 36, 48, 87, 63],
        [92, 73, 64, 33, 81],
        [88, 76, 32, 55, 47]]
for i in data:
    for j in i:
        print(j, end=' ')
    
# 輸出
# 17 36 48 87 63 92 73 64 33 81 88 76 32 55 47
```

![](../../.gitbook/assets/image%20%2877%29.png)

## range\(\) + list\(\)

```python
data = [[17, 36, 48, 87, 63],
        [92, 73, 64, 33, 81],
        [88, 76, 32, 55, 47]]
for i in range(len(data)):
    for j in data[i]:
        print(j, end=' ')
            
# 輸出
# 17 36 48 87 63 92 73 64 33 81 88 76 32 55 47
```

* i 分別為 0 1 2 代表索引值
* j 為 data\[i\] 內的元素

## 任務: 聚餐

班上要招開國小同學會，因此大家決定要用投票的方式來 選擇一間想要的餐廳，請你寫一個程式，來幫助大家決定一 間最理想的餐廳吧!

* 每位同學會輸入一行，表示想吃的餐廳。
* 每行可輸入多家餐廳，每家餐廳中間用一個空格間隔。
* 每行的每間餐廳都代表一票。
* 統計直到輸入0表示投票結束。

```bash
# 範例輸入:
a b
c a d
a f b
c
d c
f a g c
c d
0

# 範例輸出:
a: 4
b: 2
c: 5
d: 3
f: 2
g: 1
```

### **思考流程:**











### **你的答案**

```python
# Your code here.








```

