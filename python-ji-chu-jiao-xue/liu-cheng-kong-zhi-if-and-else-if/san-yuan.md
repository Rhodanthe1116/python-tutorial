# If 技巧

一行 if

```python
if True: print(1)
```

一行 if 多重指令

```python
if True: print(1); print(2); print(3)
```

一行 if 和一行 elif 等

```python
x = int(input())
if x == 0: print("x == 0")
elif x == 1: print("x == 1")
else: print("x == 2")
```

**條件表達式（**Conditional Expressions**）**：一行 if else，在其他語言稱為**三元運算子**

```python
switch = True
print("On" if switch == True else "Off") 
```

連鎖條件表達式

```python
x = int(input())

s = ( "uno" if (x == 1) else
      "due" if (x == 2) else
      "tre" if (x == 3) else
      "quattro" if (x == 4) else
      "cinque"
 )
 
 print(s)
```

可跟下面相同寫法對照

```python
x = int(input())

if x == 1: s = "uno"
elif x == 2: s = "due"
elif x == 3: s = "tre"
elif x == 4: s = "quattro"
else: s == "cinque"

print(s)
```

**pass**：什麼都不做。用於臨時不知道要寫什麼的紀錄，等待之後回來補

```python
if True:
   pass
else:
   print("False") 
```





