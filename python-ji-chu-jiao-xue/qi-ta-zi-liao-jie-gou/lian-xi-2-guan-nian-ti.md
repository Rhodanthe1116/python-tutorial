# ⚡ 練習2：觀念題

## 下列關於set的敘述，何者錯誤？

1. set內的元素不重複
2. set內的元素沒有順序（無序）
3. set可以用索引值存取
4. set可以用in語法來確認元素是否存在

3

set無序，也不能用索引值存取。

## 請問下列程式會輸出什麼？

```python
s = set()
l = [1, 3, 3, 0, 9, 3, 4, 1, 5, 0, 9]
sum = 0
for num in l:
    if num in s:
        continue
    s.add(num)
    sum += num
print(sum)
```

1. 18
2. 20
3. 22
4. 24

3

此程式會將l中不重複的元素相加，因此將1, 3, 0, 9, 4, 5相加等於22。

## 請問下列對於程式的輸出結果的描述，何者錯誤

```python
a = {1, 4, 0, 2}
b = {0, 2, 9, 5}

print(a & b)
print(a | b)
print(a - b)
print(a ^ b)
```

1. 輸出的第一行為：{0, 2} 
2. 輸出的第二行為：{0, 1, 2, 4, 5, 9} 
3. 輸出的第三行為：{1, 4} 
4. 輸出的第四行為：{5, 9}

4

應為{1, 4, 5, 9}，符號^為不交集，會將各個集合獨有的元素回傳。請參考集合的運算

## 請問下列關於dictionary的描述，何者錯誤？

1. dictionary內的key可以重複，也就是一個key可以對應到不同的value
2. dictionary跟set一樣，不會按照key的大小排序（無序）
3. dictionary可以用索引值存取
4. dictionary可以用in語法來確認key是否存在

1

dict的key不能重複，新的value會覆蓋掉舊的value，key為一對一的索引值。

## 請問下列會輸出什麼？

```python
d = {
    0: 0,
    1: 0,
    2: 0
}
print(d[3])
```

1. 0
2. 3
3. 2
4. KeyError: 3

4

若以\[\]存取不存在的元素，會出現KeyError。在存取之前需要確認元素是否存在。

## 請問下列會輸出什麼？

```python
n = 10
a = [0, 9, 3, 2, 1, 3, 5, 3, 2, 9]
d = {}
for i in range(n):
    if a[i] in d:
        d[a[i]] += 1
    else:
        d[a[i]] = 1

print(d[3])
```

1. 1
2. 2
3. 3
4. 4

3

此程式為典型的統計出現次數，因此3的出現次數為3。

## 請問下列程式會輸出什麼？

```python
n = 12
l = [2, 4, 2, 3, 2, 5, 3, 7, 2, 3, 4, 3]
d = {}
for key in l:
    if key in d:
        d[key] += 1
    else:
        d[key] = 1
l = sorted(d.items(), key= lambda x: (-x[1], x[0]))
print(l[0])
```

1. \(2, 3\)
2. \(3, 4\)
3. \(4, 2\)
4. \(2, 4\)

4

此程式會統計數字出現頻率，並且將字典依頻率排序，頻率越高越前面，若頻率相同則將key依照字典序輸出。因此輸出\(2, 4\)

## 請問若要將下列程式碼中的keys跟values合併成一個dict，需使用下列哪個語法？

```python
keys = ['a', 'b', 'c']
values = [1, 2, 3]
```

1. dict\(keys, values\)
2. zip\(keys, values\)
3. zip\(dict\(keys, values\)\)
4. dict\(zip\(keys, values\)\)

4

zip將資料打包，回傳的型態為 zip，需使用強制轉型為其他型態，因此需要再包一層dict

## 請問下列程式若要成功運行，需要在問號處填入何者？

```python
d = {
    4: 5,
    8: 2,
    3: 1,
    9: 0,
}
for k, v in --?--:
    print(k, v)

```

1. d.items\(\)
2. d.values\(\)
3. d.keys\(\)
4. \*\*d

1

item為key與value的pair，因此填入d.items\(\)才會回傳item，兩個變數k, v才會都有對應的數值。

## 若要合併兩個字典，可用以下哪個語法？

1. new = {\*dict1, \*dict2}
2. new = {\*\*dict1, \*\*dict2}
3. new = {\*dict1, \*\*dict2}
4. new = {dict1, dict2}

2

\*\*將字典拆解，\*將list拆解。



## 多的

## 下列關於字典與函式的敘述，何者錯誤？

1. 參數前面加上 \*\* 表示將傳入的值打包成字典
2. 當參數為 \*\* 時，使用此函式對應的引數為 key=value
3. 傳入的引數會自動轉成一個字典的key，且型態為字串
4. 在函式參數中，一般參數、\*參數_、\*\*_參數的順序皆可任意對換

