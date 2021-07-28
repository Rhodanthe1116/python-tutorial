# List-1 觀念題

## 請問下列關於List的敘述，何者錯誤？

1. 可以儲存大量資料
2. 可以存放多種型態
3. List裡面只能同時存放一種型態
4. List有個專屬的名字

## 請問下列哪一項會讓my\_list不是一個List？

1. my\_list = \[\]
2. my\_list = list\(\)
3. my\_list = input\(\).split\(\)
4. my\_list = input\(\)

## 請問下列創造List的方法，何者錯誤？

1. l = \[0\] \* 5
2. l = list\(range\(5\)\)
3. l = list\(\[0, 1, 2\]\)
4. l = list\[\]

## 請問下列敘述何者錯誤？

1. a = input\(\), a為字串
2. b = input\(\).split\(\), b為list
3. c = range\(5\), c為list
4. d = list\(range\(5\)\), d為list

## 以下程式若輸入0 1 2 3 4，會輸出什麼？

```python
# input 0 1 2 3 4
my_list = input().split()
print(my_list)
```

1

```text
1 2 3 4 5
```

2

```text
['1', '2', '3', '4', '5']
```

3

```text
[1, 2, 3, 4, 5]
```

4

```bash
[1 2 3 4 5]
```

## 請問下列程式會輸出什麼？

```python
my_list = list('apple')
print(my_list)
```

1. \['a', 'p', 'p', 'l', 'e'\]
2. \[a, p, p, l, e\]
3. \[apple\]
4. \['apple'\]

## 請問下列程式會輸出什麼？

```python
colors = ['red', 'orange', 'blue']

for color in colors:
    if color == 1:
        break
    print(color, end=' ')
    
for i in range(3):
    if i == 'orange':
        break
    print(colors[i], end=' ')

```

1. red orange blue red orange blue
2. red red
3. red orange blue red
4. red red orange blue

## 請問下列程式碼於第幾行會出現錯誤？

```python
for i in [0, 1, 2, 3, 4]:
    print(i)

for i in list('APPLE'):
    print(i)
    
for i in input().split():
    print(i)

```

1. 第1行
2. 第4行
3. 第7行
4. 以上皆非

## 請問下列程式碼會輸出什麼？

```python
my_list = ['a', 'b', 'c', 'd', 'e']

print(my_list[1], end=' ')
print(my_list[-2], end=' ')

```

1. b d
2. a d
3. a c
4. b c

## 請問下列程式會輸出什麼？

```python
students = ['ben', 'candy', 'denny']

for i in range(3):
    print(i, end=' ')
```

1. 0 1 2
2. ben candy denny
3. 0 ben 1 candy 2 denny
4. 1 ben 2 candy 3 denny

## 請問下列程式會輸出什麼？

```python
my_list = [0, 1, 2, 3, 4]

my_list[2] *= 9

print(my_list)

```

1. \[0, 1, 8, 3, 4\]
2. \[0, 9, 2, 3, 4\]
3. \[0, 2, 4, 6, 8\]
4. \[0, 1, 18, 3, 4\]



## 請問下列程式會輸出什麼？

```python
my_list = [0, 1, 2, 3, 4]

for i in range(5):
    my_list[i] = my_list[i] * my_list[i]

print(my_list)

```

1. \[0, 1, 4, 9, 16\]
2. \[0, 1, 2, 3, 4\]
3. \[0, 2, 4, 6, 8\]
4. \[1, 3, 5, 7, 9\]



