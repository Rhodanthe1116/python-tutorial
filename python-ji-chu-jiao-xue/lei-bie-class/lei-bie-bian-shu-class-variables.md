# 類別變數 Class Variables

在類別中創造的變數，我們稱為**類別變數Class variable**，類別變數是所有實例所共有的，且都擁有相同的值。比如說要定義一個圓的類別：

```python
class Circle:
    pi = 3.14
```

因為圓周率對於每個圓都一樣，不論圓的半徑是多少，都可以當作3.14，所以可以設成類別變數，讓所有圓共享。

## 類別變數的共通性

對class variable的修改，會讓所有實例的值一起更動

雖然比較少見，但有時候我們會用到此性質

在有些語言中，稱為**Static**

```python
class Circle:
  pi = 3.14 # class variable

# 可以直接利用class名稱來取用
print(Circle.pi) # 3.14 class variable

red_circle = Circle()
green_circle = Circle()

# 對class variable的修改，會讓所有實例的值一起更動
Circle.pi = 3.14159
print(Circle.pi) # 3.14159
print(red_circle.pi) # 3.14159
print(green_circle.pi) # 3.14159
```

## 實例變數覆蓋類別變數

### 為什麼可以混用

一般來說，會將每個實例共有且不會改變的性質設為類別變數，而每個實例都不同的性質設為實例變數，通常在初始化的時候進行實例變數的設值，來減少程式碼的重複，關於在初始化時建立實例變數將在下個部分教到。

雖然類別變數和實例變數有區隔，但在Python中，若是執行下列程式：

```python
class Circle:
  # Default color is red.
  color = "red" # class variable

red_circle = Circle()
green_circle = Circle()

# Overide the class variable.
green_circle.color = "green" # becomes instance variable
```

上列程式碼有個圓，並且有個`color`類別變數，但在第`9`行的地方，用了實例變數的方式設了值，這時候**實例變數會覆蓋類別變數**，讓`green_circle.color`變成實例變數。

因為類別變數與實例變數的取用方式一樣，都是用`.`，所以以上程式碼不會發生任何錯誤。

### 可能造成的問題1

```python
class Circle:
  pi = 3.14 # class variable

red_circle = Circle()
green_circle = Circle()

# Overide the class variable.
green_circle.pi = 3.1 # instance variable

print(Circle.pi) # 3.14 class variable
print(red_circle.pi) # 3.14 class variable
print(green_circle.pi) # 3.1 instance variable <------


Circle.pi = 3.14159 # class variable <------ 更改了class variable
print(Circle.pi) # 3.14159 class variable
print(red_circle.pi) # 3.14159 class variable
print(green_circle.pi) # 3.1 instance variable <------ 沒有一起改
```

### 可能造成的問題2

{% embed url="https://docs.python.org/3/tutorial/classes.html#class-and-instance-variables" %}

Generally speaking, instance variables are for data unique to each instance and class variables are for attributes and methods shared by all instances of the class:

```python
class Dog:

    kind = 'canine'         # class variable shared by all instances

    def __init__(self, name):
        self.name = name    # instance variable unique to each instance

>>> d = Dog('Fido')
>>> e = Dog('Buddy')
>>> d.kind                  # shared by all dogs
'canine'
>>> e.kind                  # shared by all dogs
'canine'
>>> d.name                  # unique to d
'Fido'
>>> e.name                  # unique to e
'Buddy'
```

As discussed in [A Word About Names and Objects](https://docs.python.org/3/tutorial/classes.html#tut-object), shared data can have possibly surprising effects with involving [mutable](https://docs.python.org/3/glossary.html#term-mutable) objects such as lists and dictionaries. For example, the _tricks_ list in the following code should not be used as a class variable because just a single list would be shared by all _Dog_ instances:

```python
class Dog:

    tricks = []             # mistaken use of a class variable

    def __init__(self, name):
        self.name = name

    def add_trick(self, trick):
        self.tricks.append(trick)

>>> d = Dog('Fido')
>>> e = Dog('Buddy')
>>> d.add_trick('roll over')
>>> e.add_trick('play dead')
>>> d.tricks                # unexpectedly shared by all dogs
['roll over', 'play dead']
```

Correct design of the class should use an instance variable instead:

```python
class Dog:

    def __init__(self, name):
        self.name = name
        self.tricks = []    # creates a new empty list for each dog

    def add_trick(self, trick):
        self.tricks.append(trick)

>>> d = Dog('Fido')
>>> e = Dog('Buddy')
>>> d.add_trick('roll over')
>>> e.add_trick('play dead')
>>> d.tricks
['roll over']
>>> e.tricks
['play dead']
```

## 💻練習

{% hint style="info" %}
* [ ] 撰寫一個`Dog`類別
* [ ] 為他加上`legs`類別變數，並設定值
* [ ] 創造一個實例，取名`husky`
* [ ] 輸出~~`Every dog has {legs} legs.`~~
{% endhint %}

{% tabs %}
{% tab title="First Tab" %}

{% endtab %}

{% tab title="參考答案" %}
```python
class Dog:
    legs = 4
    
husky = Dog()

print("Every dog has {} legs.".format(husky.legs))
# Every dog has 4 legs.
```
{% endtab %}
{% endtabs %}
