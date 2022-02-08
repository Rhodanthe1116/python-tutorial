# ⚡ 練習：觀念題

## 要如何創造一個函數？

1. def myFunction():
2. function myFunction():
3. create myFunction():
4. func myFunction():

## 下列哪個內建函數會回傳物件的專屬號碼？

1. ref()
2. identity()
3. id()

3

id()為Python的語法，可以回傳物件的id

## 請問下列程式將輸出什麼？

```python
def outerFun(a, b):
    def innerFun(c, d):
        return c + d
    return innerFun(a, b)
    return a

result = outerFun(5, 10)
print(result)
```

1. 5
2. 15
3. (15, 5)
4. Syntax Error

2

result = outerFun(5, 10)

outerFun(5, 10) 會執行第4行 return innerFun(5, 10)

return innerFun(5, 10) 會執行第3行 return 5 + 10

整個傳回就去就是result = 5 + 10

## 請問下列程式將輸出什麼？

```python
print(square(5))

def square(num):
    return num * num
```

1. 25
2. 5
3. NameError
4. SyntaxError

3

程式在呼叫 square() 時，還沒有看過 square() 函式的定義，第一行應在第四行後出現才正確

## 對於下列函數func的呼叫，何者較不合理？

```python
def func(name, age=17):
    print("{}{}歲".format(name, age))
    
```

1. func('小明', 15)
2. func('小明')
3. func(15, '小明')
4. func(age=15, name='小明')

3

若沒有明確指定，引數的順序需與參數相同。

## 請問下列程式將輸出什麼？

```python
def add(a, b):
    return a + 5, b + 5

result = add(3, 2)
print(result)
```

1. 15
2. 8
3. (8, 7)
4. SyntaxError

3

函數可以回傳多的回傳值，此時回傳的型態會是一個Tuple（類似list，由小括號包起來），result可以改寫成x, y。

## 請問下列程式將輸出什麼？

```python
def func(name, age=17):
    print("{}{}歲".format(name, age))
    
func('小明', 20)
```

1. 小明17歲
2. 小明20歲
3. SyntaxError
4. NameError

2

如果有傳入引數，那麼預設的參數就會被覆蓋掉。

## 下列對於Python函數的敘述，何者錯誤？

1. 函數只能回傳一個回傳值
2. 函數可以有很多的參數
3. 函數裡面可以不寫return
4. 函數裡面的變數可以與函數外的變數同名

1

1.可以有多個回傳值

## 請問下列程式將輸出什麼？

```python
def func(num, data):
  num += 10
  for i in range(len(data)):
    data[i] = i

d = 0
l = [0, 0, 0, 0, 0, 0]
func(d, l)
print(d, l)
```

1. 0 \[0, 1, 2, 3, 4, 5]
2. 10 \[0, 1, 2, 3, 4, 5]
3. 0 \[0, 0, 0, 0, 0, 0]
4. 10 \[0, 0, 0, 0, 0, 0]

1

int 為不可變，list為可變，可參考講義128頁

## 請問下列程式將輸出什麼？

```python
def scope_test():
    spam = "local spam"
    print(spam)
   
spam = "global spam"
scope_test() 
```

1. local spam
2. NameError
3. global spam
4. SyntaxError

1

在函式中，呼叫同名的變數時， 指的是函式內的那個變數而不是函式外的。

## 期末 APCS

給定一個 1x8 的串列 A， A = {0, 2, 4, 6, 8, 10, 12, 14}。右側函式 Search(x) 真正目的是找到 A 之中大於 x 的最小值。然而，這個函式有誤。請問下列哪個函式呼叫可測出函式有誤？

```python
A = [0, 2, 4, 6, 8, 10, 12, 14]

def Search(x):
    high = 7
    low = 0
    while high > low:
        mid = (high + low) // 2
        if A[mid] <= x:
            low = mid + 1
        else:
            high = mid
    return A[high]
```

1. Search(-1)&#x20;
2. Search(0)
3. Search(10)
4. Search(16)

4
