# 方法 Method

定義在類別裡面的函數function，稱作**方法method**。就像可以在類別裡面定義變數，同樣地也可以在類別裡面定義函數，需要注意的是，通常會將類別中的函數稱作方法method，實際上的功能與使用方法與函數類似。先看看下列包含了方法的程式碼：

```python
class Student:
    school = "XXXXX High School"
    # A function in class is called Method.
    def go_to_school(self):
        print("I don't want to go to the {}!".format(self.school))
        
benson = Student()
# Call the method via "object.method()" 
benson.go_to_school()
# I don't want to go to the XXXXX High School!
```

看完後，可能會發現`self`這個陌生的詞，不過似乎也不影響猜測其功能。在這個例子中，創造了`Student`類別，並在裡面定義了`go_to_school`方法，於是第9行便可呼叫`benson`中的`go_to_school`方法，印出以上結果。需要注意的是，方法必定要有一個self參數，`self`代表的是呼叫此方法的物件，也就是說，`benson.go_to_school()`類似於`go_to_school(benson)`，而`self`接收便是`benson`。這也就是為什麼be`nson.go_to_school()不`用放任何參數的原因，因為它會自動將`benson`放進去。

另外，如果需要在方法中使用class variable的話，也要用`self`來指名，否則都會出錯。

{% hint style="danger" %}
```python
class Student:
    school = "XXXXX High School"
    def go_to_school(self):
        # Error occur
        print("I don't want to go to the {}!".format(school))
        
benson = Student()
benson.go_to_school()
# NameError: name 'school' is not defined
```

在方法中沒有使用`self.school`
{% endhint %}

## 有參數的方法

既然方法與函數類似，當然也可以傳入參數：

```python
class SearchEngine:
    def search(self, term):
        print("Searching {}......".format(term))
        # search
        print(".")
        print("..")
        print("...")
        print("Search results about {}".format(term))
        
guugle = SearchEngine()
guugle.search("momo")
# Searching momo......
# Search results about momo
```

在上例中，使用了創造了一個搜尋引擎`SearchEngine`類別，並有個`search()`方法，需要傳入搜尋關鍵字`term`才能作用。注意此時`term`不用加`self`，以及在呼叫的時候也不用加`self`，因為`term`不是物件的屬性。

## 💻練習

{% hint style="info" %}
下方是一個可以儲存杯子的系統，這個系統現在需要一個新增杯子的功能，並在要在每次新增成功後印出目前全部的杯子，現在需要你來完成這個系統。

* [ ] 定義`add_cup()`方法，需要接收`id`, `size`兩個參數
* [ ] 將杯子存成字典`new_cup`中，參考`cup_list`
* [ ] 在`add_cup`中，將新的杯子存放到`cup_list`中
* [ ] 印出`cup_list`
* [ ] 在主程式放入三個杯子，`(id, size)`分別是`(1, "M")`, `(2, "M")`, `(3, "L")` 
{% endhint %}

{% tabs %}
{% tab title="First Tab" %}
```python
class CupDatabase:
    cup_list = [
        {
            "id": 999,
            "size": "S"
        }
    ]
      
    # Your code here

U_cup = CupDatabase()

# Your code here

```
{% endtab %}

{% tab title="參考答案" %}
```python
class CupDatabase:
    cup_list = [
        {
            "id": 999,
            "size": "S"
        }
    ]

    def add_cup(self, id, size):
        new_cup = {
            "id": id,
            "size": size
        }
        self.cup_list.append(new_cup)
        print("---Cup List---")
        print(self.cup_list)
        print("--------------")
        print()

U_cup = CupDatabase()
U_cup.add_cup(1, "M")
U_cup.add_cup(2, "M")
U_cup.add_cup(3, "L")
```
{% endtab %}
{% endtabs %}



