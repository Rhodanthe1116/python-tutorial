# 實例變數 Instance Variable

類別與實例必須要區分開來，類別是模板，而實例是類別的具體化，但為什麼需要區分開來呢？因為每個實例可以擁有他特有的**實例變數 Instance Variable**，且這個實例變數只有在實例被實例化之後才會存在，相較於類別變數是所有實例共有的，實例變數可以只存在於特定物件裡，例如：

```python
class Circle:
  # pi is class variable
  pi = 3.14

# Initialization
red_circle = Circle()
hollow_circle = Circle()

# .color and .type are both instance variables
red_circle.color = "red"
hollow_circle.type = "hollow"
```

在上例中，紅圓有`color`屬性，而空心圓有`type`屬性，兩個屬性都是`Circle`類別所沒有的，兩者都是實例變數，在成為實例之後才出現的。

## 類別變數與實例變數

一般來說，會將每個實例共有且不會改變的性質設為類別變數，而每個實例都不同的性質設為實例變數，通常在初始化的時候進行實例變數的設值，來減少程式碼的重複，關於在初始化時建立實例變數將在下個部分教到。

雖然類別變數和實例變數有區隔，但在Python中，若是執行下列程式：

```python
class Circle:
  # Default color is red.
  color = "red"

red_circle = Circle()
green_circle = Circle()

# Overide the default color which is a class variable.
green_circle.color = "green"
```

上列程式碼有個圓，並且有個`color`類別變數，但在第`9`行的地方，用了實例變數的方式設了值，這時候實例變數會覆蓋類別變數，讓`green_circle.color`變成實例變數，成為一個獨特的屬性。

因為類別變數與實例變數的取用方式一樣，都是用`.`，所以以上程式碼不會發生任何錯誤。

