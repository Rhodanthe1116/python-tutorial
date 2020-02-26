# 建構子 Constructors

在之前的教學中，學到可以在類別中定義函數。這邊要介紹一個特別的方法，稱作「\_\_init\_\_\(\)」，可以用來初始化 initialize 物件，而且這個方法只會執行一次，只會在物件第一次被創造的時候執行。

{% hint style="info" %}
初始化的意思類似於歸零重來，或將系統恢復成剛開始的樣子
{% endhint %}

```python
class Charactor:
    def __init__(self):
        print("Successfully created a new Charactor!")
    hp = 100

# __init__() called
user = Charactor()

print(user.hp)
```

上例中的\_\_init\_\_\(\)便是初始化函數，在一般物件導向的程式語言中也稱作**建構子**。他在第7行的時候在呼叫Charactor\(\)的時候會跟著執行。

### \_\_init\_\_\(\) Function

```python
class Charactor:
    def __init__(self):
        print("Successfully created a new Charactor!")
    hp = 100

user = Charactor()
print(user.hp)
```

在物件裡面的函數我們稱他為**方法 Method** ，在這裡我們可以看到，在執行`Charactor()`時會執行一次`__init__()`方法！注意其中的`self`，`self`代表類別自己本身，不過因為此時類別並沒有實體，也沒有名稱，所以使用`self`代表物件本身，`self`的存在為必要。

若想在初始化時給他一些參數，亦可：

```python
class Charactor:
    def __init__(self, n, h):
        print("Successfully created a new Charactor!")
        self.name = n
        self.hp = h

user = Charactor("Menson", 9532)

print(user.name)
print(user.hp)
```

注意以上使用了`self.name`和`self.hp`來取用自己本身的成員屬性，而`n`跟`h`則是外部傳來的變數

