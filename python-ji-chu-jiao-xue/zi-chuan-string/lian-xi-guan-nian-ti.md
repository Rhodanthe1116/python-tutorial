# ⚡ 練習：觀念題

## 下列何者較不能代表一個字串？

1. "hello"
2. 'hello'
3. hello

## 下列何者可以正確表示字串中的第一個字？

1. str\[0\]
2. str.sub\(0, 1\)
3. sub\(str, 0, 1\)

## 知道怎麼處理輸入的資料是非常重要的一件事，請問下列跟字串有關的程式碼會輸出什麼？

```python
my_string = "1 2 3 4 5"
print(my_string.split())
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

## 期中

執行後，輸出為何？

```python
item = ['2', '8', '3', '1', '9']

count = 5

for a in range(count-1):
    c = a
    t = item[a]
    for b in range(a+1, count):
        if (item[b] < t):
            c = b
            t = item[b]
        if ((a == 2) and (b == 3)):
            print(t, c)

```

1. 1 2
2. **1 3**
3. 3 2
4. 3 3

若一字串str = "Hello world!0"，則str\[12\]等於多少？本題並沒有錯字或多打字

1. 未宣告
2. **0**
3. !
4. \n

