# 函數 Function

### 數學上的函數：

$$
f(x) = \sqrt x = y
$$

f 是一個函數，x 是輸入，根號 x 是過程，y 是輸出

### 程式中看過的函數：

在函數中，「輸入」稱作「參數」，「輸出」則稱作「回傳」

```python
math.sqrt(4)    # sqrt()是一個函數，4是參數，開根號是過程，2是回傳值
print("hello")    # print()是一個函數，"hello"是參數，執行顯示指令是過程，但可以沒有回傳
x = input()    # input()是一個函數，沒有參數，等待使用者輸入是過程，最後回傳輸入的東西
```

上面都是別人寫的函數，而我們也可以自己寫函數。

## 定義函數

### 沒有參數也沒有回傳

```python
def my_function():
  print("Hello from a function")
  
my_function()  # 呼叫函數
```

### 有參數，沒回傳

```python
def greet(name):
    print("hello", name)

greet("Benson")
greet("Menson")
```

### 有參數，有回傳

#### 範例一：求面積

```python
def area(width, height):
    return width * height

print(area(10, 3))
```

#### 範例二：判斷密碼強度

```python
def is_good_password(password):
    if len(password) < 8:
        return False
    else:
        return True

def signup(username, password):
    if not is_good_password(password):
        return "密碼不夠強"
        
```

#### 範例三：圓柱體面積

{% embed url="https://learn.arcade.academy/en/latest/chapters/08_functions/functions.html" %}

![](<../../.gitbook/assets/image (120) (1).png>)

```python
def volume_cylinder(radius, height):
    pi = 3.141592653589
    volume = pi * radius ** 2 * height
    return volume
```

### 預設參數值

```python
def my_function(country = "Norway"):
  print("I am from " + country)

my_function("Sweden")
my_function("India")
my_function()
my_function("Brazil")
```

注意！預設參數會以以下的形式執行：

```python
i = 5

def f(arg=i):
    print(arg)

i = 6
f()
```

### List 當作參數

```python
def my_function(food):
  for x in food:  #food is a list
    print(x)

fruits = ["apple", "banana", "cherry"]

my_function(fruits)
```

### 關鍵字

```python
def my_function(child3, child2, child1):
  print("The youngest child is " + child3)

my_function(child1 = "Emil", child2 = "Tobias", child3 = "Linus")
```

### 未知個數參數

```python
def my_function(*kids):
  print("The youngest child is " + kids[2])
  print(kids)

my_function("Emil", "Tobias", "Linus")
```

##

