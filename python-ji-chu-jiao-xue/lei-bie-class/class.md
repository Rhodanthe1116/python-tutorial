# 類別 Class

在現實生活中，人的思考會將一個一個東西包裝，視為一個獨立的個體，又或是稱做一個獨立的物件，而每個物件又會有其專屬的屬性。例如遊戲中的人物便可視作一個物件，而一個遊戲人物必定會有血量、攻擊力等等的**屬性**。除了屬性之外，他還可以有一些**操作方法**，比如跳躍、移動等等。

在 Python 中，可以利用 Class 語法來創造一個自訂的物件型態。

## Python 中的 Class

```python
my_int = 6
print(type(my_int))
# <class 'int'>

my_list = [1, 2, 3]
print(type(my_list))
# <class 'my_list'>
```

在上面的程式碼中，利用了type來印出之前常見的資料型態，可以發現在&lt;&gt;中都有個class的字樣，而這裡我們就要利用類似的原理來創造自訂的資料型態。

{% hint style="info" %}
試著印出string和dictionary的type
{% endhint %}

## 創造類別 Create a Class

Class 可以幫助我們創造物件的模板或原型

```python
class Charactor:
    hp = 100
```

上方利用`class`創造出一個叫`Charactor`的自訂資料型態，我們可以在裡面加上`hp`這個**屬性 Attrtibute**

## 創造類別實例 Create Class Instance

只創造 Class並不會創造出任何新的物件，因為Class只是一個模板而已，需要透過創造實例來創造新物件，就跟有了int，還要再給他一個數字一樣。 

**實例 Instance** 是類別的實體化

```python
class Charactor:
     hp = 100

# Create Instance
new_charactor = Charactor()

print(type(new_charactor))
# <class '__main__.Charactor'>
```

在第 5 行利用`Charactor()`創造一個新的實例物件，再將`new_charactor`指定為他。若利用type\(\)會發現他的class為Charactor

## 取用變數屬性

可以用`.`取用屬性：

```python
class Charactor:
     hp = 100

new_charactor = Charactor()

# new_charactor.hp
print(new_charactor.hp)
# 100
```

在class的定義中，將定義了hp這個變數，並將其值設為100，而在new\_charactor時便會自動擁有這個變數，之後在程式中，若要使用這個變數，只要使用`.`來取得即可。使用方法與一般變數相同。

```python
new_charactor.hp = 50
print(new_charactor.hp)
# 50
```

{% hint style="info" %}
試著創造一個學生Class，為其設定「名字」跟「號碼」兩個屬性。
{% endhint %}

#### 不同的實例不共用屬性

假如今天有兩個實例，若做以下操作：

```python
class Charactor:
     hp = 100

charactor_1 = Charactor()
charactor_2 = Charactor()

charactor_1.hp = 70

print(charactor_1.hp)
print(charactor_2.hp)
# 70
# 100
```

可以發現兩者的hp不一樣，因為每個實例顯然需要是獨立的。



## Initialization

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



