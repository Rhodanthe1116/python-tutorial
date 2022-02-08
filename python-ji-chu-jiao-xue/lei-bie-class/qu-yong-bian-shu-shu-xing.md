# 實例變數 Instance Variable

## 實例變數

我們必須要區分清楚**類別**與**實例。**類別是模板，而實例是類別的具體化，但為什麼需要區分開來呢？因為每個實例可以擁有他特有的**實例變數 Instance Variable**，且這個實例變數只有在實例被實例化之後才會存在，相較於類別變數是所有實例共有的，實例變數可以只存在於特定物件裡，例如：

```python
class Circle:
  pi = 3.14 # class variable, shared by every circle.

# Initialization
red_circle = Circle()
hollow_circle = Circle()

red_circle.color = "red" # instance variables

print(red_circle.pi) # 3.14 - class variable
print(red_circle.color) # red - instance variables
print(red_circle.type) # AttributeError

hollow_circle.type = "hollow" # instance variables

print(hollow_circle.pi) # 3.14 - class variable
print(hollow_circle.color) # AttributeError
print(hollow_circle.type) # hollow- instance variables
```

在上例中，紅圓有`color`屬性，而空心圓有`type`屬性，兩個屬性都是`Circle`類別所沒有的，兩者都是實例變數，在成為實例之後才出現的。

## 實例變數與`__init__`

* 常常搭配`__init__`（建構子）使用&#x20;
* 建議不要在建構子外新增實例變數，以便debug

```python
class Circle:
  pi = 3.14 # class variable
  
  def __init__(self, color, type):
    self.color = color # instance variables
    self.type = type # instance variables

# Initialization
red_circle = Circle("red", "")
hollow_circle = Circle("", "hollow")
```



