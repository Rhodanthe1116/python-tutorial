# 巢狀 If

if 裡面包一個 if

```python
x = int(input())
y = int(input())
if x > 0:
    if y > 0:
        print("第一象限")
    else:    
        print("第四象限")
else:
    if y > 0:
        print("第二象限")
    else:    
        print("第三象限")
```

```python
num = int(input("請輸入一個數字："))
if num % 2 == 0:
    if num % 3 == 0:
        print("此數字可以被 2 和 3整除")
    else:
        print("此數字可以被 2 整除，但不能被 3 整除")
else:
    if num % 3 == 0:
        print("此數字可以被 3 整除，但不能被 2 整除")
    else:
        print("此數字不能被 2 和 3 整除")
```

