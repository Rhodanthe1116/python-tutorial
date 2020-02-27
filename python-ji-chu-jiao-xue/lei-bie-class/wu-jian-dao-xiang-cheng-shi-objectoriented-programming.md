# 物件導向程式 Object-Oriented Programming

如果只是利用實例變數來儲存key跟value，那不如直接用字典就可以達成相同的功能。通常會利用初始化與實例變數，來表明或限制實例變數的種類或用途，維持物件的屬性，例如：

```python
class Circle:
  pi = 3.14
  def __init__(self, diameter):
    # Self refers to the object. Radius is a instance variable 
    self.radius = diameter / 2
  
small_circle = Circle(12)
big_circle = Circle(11460)
```

在上例中，`self`可能是`small_circle`或`big_circle`，不管怎樣，`self`都是實例，因此`radius`都是實例變數。

若是搭配所有介紹過的功能，便可實現出物件導向的好處：

```python
class Circle:
  pi = 3.14
  def __init__(self, diameter):
    print("Creating circle with diameter {d}".format(d=diameter))
    
    # Self is an object. Radius is a instance variable 
    self.radius = diameter / 2
    
  def circumference(self):
    # Here can use class variable and instance variable both
    return 2 * self.pi * self.radius
  
medium_pizza = Circle(12)
teaching_table = Circle(36)
round_room = Circle(11460)

print(medium_pizza.circumference())
print(teaching_table.circumference())
print(round_room.circumference())
```

在上例中，定義了圓Circle這個類別，利用了此類別創造了三個實例`medium_pizza`, `teaching_table`, `round_room` ，每個實例有不同的半徑`radius`，同時也可以用相同的圓周長方法`circumference()`來取得周長。

如此一來，不僅可以維持資料的結構，也可以有效地重複利用定義的類別。不斷地累積功能，便可製成一個完整的物件。

