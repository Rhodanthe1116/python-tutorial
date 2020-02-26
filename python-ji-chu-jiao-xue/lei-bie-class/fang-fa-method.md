# 方法 Method

定義在類別裡面的函數function，稱作方法method。就像可以在類別裡面定義變數，同樣地也可以在類別裡面定義函數，需要注意的是，通常會將類別中的函數稱作方法method，實際上的功能與使用方法與函數類似。先看看下列包含了方法的程式碼：

```python
class Student:
    energy = 100
    
    def go_to_school(self):
        self.energy -= 100
        print("I don't want to go to school!")
        print("I have {} energy".format(self.energy))
        
benson = Student()
benson.go_to_school()
# I don't want to go to school!
# I have 0 energy
```

看完後，可能會發現self這個陌生的詞，不過似乎也不影響猜測其功能。在這個例子中，創造了Student類別，並在裡面定義了go\_to\_school方法，於是第9行便可呼叫Benson中的go\_to\_school方法，印出以上結果。需要注意的是，方法必定要有一個self參數，self代表的是呼叫此方法的物件，也就是說，benson.go\_to\_school\(\)類似於go\_to\_school\(benson\)，而self接收便是benson。這也就是為什麼benson.go\_to\_school\(\)不用放任何參數的原因，因為它會自動將benson放進去。

另外，如果需要在方法中使用成員變數的話，也要用self來指名，否則都會出錯。

```python
class Student:
    energy = 100
    
    def go_to_school(self):
        energy -= 100
        print("I don't want to go to school!")
        print("I have {} energy".format(energy))
        
benson = Student()
benson.go_to_school()
# UnboundLocalError: local variable 'energy' referenced before assignment

```

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

在上例中，使用了創造了一個搜尋引擎`SearchEngine`類別，並有個search方法，需要傳入搜尋關鍵字term才能作用。注意此時term不用加self，以及在呼叫的時候也不用加self。

## 💻🚧練習

{% hint style="info" %}
下方是一個可以儲存杯子的系統，這個系統現在需要一個新增杯子的功能，並在要在每次新增成功後印出目前全部的杯子，現在需要你來完成這個系統。

* [ ] 定義add\_cup方法，需要接收id, size兩個參數
* [ ] 將杯子存成字典new\_cup中，參考cup\_list
* [ ] 在add\_cup中，將新的杯子存放到cup\_list中
* [ ] 印出cup\_list
* [ ] 在主程式放入三個杯子，分別是\(1, "M"\), \(2, "M"\), \(3, "L"\) 
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



