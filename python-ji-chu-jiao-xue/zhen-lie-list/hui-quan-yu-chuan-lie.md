# 迴圈與串列

## **串列 + for ... in range**

輸入：17  36  48

### **Before**

```python
a, b, c = input().split()
print(a)
print(b)
print(c)

# 輸出
17
36
48
```

### Now

```python
data = input().split()
for i in range(3):
    print(data[i])
    
# 輸出
17
36
48
```

**超級比一比**\



![](<../../.gitbook/assets/image (73).png>)

```python
data = input().split() 
print(data)

""" 輸出 
['17', '36', '48']
"""
```

```python
data = input().split()
for i in data:
    print(i)
    
""" 輸出 
17
36
48
"""
```

```python
data = input().split()
for i in range(3):
    print(data[i])
    
""" 輸出 
17
36
48
"""
```

## **任務: 飲食偏好記錄**

**記錄5位同學們的飲食偏好**

* **每次輸入一行，第一個為數字(1\~5)代表每位學生的座號**
* **輸入完座號後空一格輸入食物種類Ex: rice/noodle/Dumpling等等…代表喜歡的食物。**
* **最多輸入5行，若輸入的第一個數字不為1\~5則代表記錄結束**

![](<../../.gitbook/assets/image (74).png>)

* **記錄每位同學的飲食偏好，並輸出**
* **若有學生的座號未輸入則在該欄位輸出-1**

```bash
# 範例輸入一
1 rice
2 noodle
3 dumpling
4 cake
5 fruit

# 範例輸出一
['rice', 'noodle', 'dumpling', 'cake', 'fruit'] 
```

```bash
# 範例輸入二
3 rice
4 noodle
1 dumpling
0

# 範例輸出二
['dumpling', -1, 'rice', 'noodle', -1] 
```

```python
# Your code here.









```

## 參考解答

```python
record = [-1, -1, -1, -1, -1]  
for i in range(5):                     
    text = input().split()        
    n = int(text[0])                     
    if n > 5 or n < 1:            
        break
    else:
        record[n-1] = text[1]           
print(record)                                                                                                                             
```
