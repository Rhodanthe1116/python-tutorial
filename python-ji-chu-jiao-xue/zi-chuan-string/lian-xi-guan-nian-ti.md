# ⚡ 練習：觀念題

## 下列何者較不能代表一個字串？

1. "hello"
2. 'hello'
3. hello

3

字串應以""或''包起來

## 下列何者可以正確表示字串中的第一個字元？

1. str\[0\]
2. str.sub\(0, 1\)
3. sub\(str, 0, 1\)
4. str\[0:\]

1

字串跟串列一樣，標籤都是從0開始。2.跟3.非python的語法，4則是字串切片，\[0:\]代表從0開始往後都保留。

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

4

```bash
[1 2 3 4 5]
```

2

應注意input\(\)的結果會是string，split\(\)後的結果是string的list

## 下列程式將輸出什麼？

```python
char = 'a'
char = ord(char)
char += 2
char = chr(char)
print(char)
```

1. **c**
2. a2
3. 99
4. a 2

1

第二行 char = ord\('a'\) =&gt; char = 97

第三行 char += 2 =&gt; char = 99

第四行 char = chr\(99\) =&gt; char = 'c'

## 請問下列程式將不會輸出什麼？

```python
str = "abcde"
print(str[::2])
print(str[1::2])
print(str[::-2])
```

1. **db**
2. ace
3. eca
4. bd

1

第二行：ace

第三行：bd

第四行：eca（即使是遞減也會從n-1開始遞減） 



## 要印出以下資訊，需要在程式碼中的{}裡分別填入什麼？

```bash
  20.53 		 for apple
+ 97.57 		 for banana
+ 66.70 		 for nuts
-------------------------
= 10.33 		 for fruits.
```

```python
apple = 20.5333
banana = 10.3333
nuts = 66.7
fruits = apple + banana + nuts

myorder = """
I want to pay:
  {} \t\t for apple
+ {} \t\t for banana
+ {} \t\t for nuts
-------------------------
= {} \t\t for fruits.
"""

print(myorder.format(fruits, banana, apple, nuts))
```

1. ```python
   {2:.2f}
   {1:.2f}
   {3:.2f}
   {0:.2f}
   ```
2. ```python
   {2:.2f}
   {2:.1f}
   {2:.3f}
   {2:.0f}
   ```
3. ```python
   {0:.2f}
   {1:.2f}
   {2:.2f}
   {3:.2f}
   ```
4. ```text
   {2:.3f}
   {2:.2f}
   {2:.1f}
   {2:.0f}
   ```

1

{:}的語法為：冒號前面指定format\(\)裡面元素的標籤，而冒號後面的語法代表輸出至小數點後幾位數（這裡.2f代表2位）

## 請問下列程式將輸出什麼？

```python
s = 'foo'
t = 'bar'
print('barf' in 2 * (s + t))
```

1. **True**
2. False
3. barf
4. foobarfoobar

1

拆解

'barf' in 2 \* \('foo' + 'bar\)

'barf' in 2 \* 'foobar'

'barf in 'foo**barf**oobar'

True

## 請問下列程式將輸出什麼？

```python
print(ord('nuts'))
```

1. 程式會出錯
2. 102 111 111
3. 102
4. 324

1

ord\(\)裡面只能放一個字元（字母，長度為一的字串\)

## 請問下列哪一項是錯誤的？

1. s\[::-1\]\[::-1\] == s
2. s\[:\] == s
3. s\[:\] is s
4. s\[::-1\]\[::-1\] is s

4

關鍵：字串切片會複製一個新的字串，複製後的新字串與原本的字串為兩個不同的空間，所以經翻轉再翻轉（\[::-1\]\[::-1\]）過後的字串與原字串不是同個字串（a is not b），儘管他們的值是相同的（a == b）。

另外一個需要注意的點是，s\[:\]這種切片方法並不會複製新的字串，畢竟其結果等同於沒切片。



## 下列哪一項會回傳「去除前後空格的字串」

1. strip\(\)
2. replace\(\)
3. lower\(\)
4. count\(\)

1

replace\(\) 替換

lower\(\) 將字串中所有字轉為小寫

count\(\) 統計字串中的某個字出現的總次數

## 期中

### 執行後，輸出為何？

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

### 若一字串str = "Hello world!0"，則str\[12\]等於多少？本題並沒有錯字或多打字

1. 未宣告
2. **0**
3. !
4. \n

### 若一串列 str = \['H', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd', '!', '0'\]，則str\[12\]等於多少？本題並沒有錯字或多打字

1. 未宣告
2. **0**
3. !
4. \n

### 



