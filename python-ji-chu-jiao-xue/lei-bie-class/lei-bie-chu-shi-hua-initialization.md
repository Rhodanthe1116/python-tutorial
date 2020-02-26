# 類別初始化 Initialization

`Charactor()`回傳一個創造出的物件，若是我們想在創造物件的同時執行一些動作或給他一些參數，比如發出通知訊息或給人物設定一些初始素質，可以在類別裡面定義以下初始函數：

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

