# While

迴圈，不斷執行相同或類似的東西，例如：一次處理數百萬筆資料、偵測改變等。

## while

先看看 if

```python
i = 1
if i < 6:
    print(i)
    i += 1
```

只會執行一次

再看看 while

```python
i = 1
while i < 6:
    print(i)
    i += 1
```

會執行很多次，直到條件不成立，若沒有跳出一直執行則稱作**無窮迴圈** **Infinite Loop** \(or **Endless Loop**\)

```python
i = 1
while i < 6:
    print(i)
```

## break

可以另外跳出迴圈

```python
i = 1
while i < 6:
    print(i)
    if i == 3:
        break
    i += 1
```

## continue

結束這個迴圈的這一次，但不跳出整個迴圈

```python
i = 0
while i < 6:
    i += 1 
    if i == 3:
        continue
    print(i)
```

