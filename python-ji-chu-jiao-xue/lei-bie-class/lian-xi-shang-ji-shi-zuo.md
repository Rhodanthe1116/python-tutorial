# ⚡ 練習：上機實作

本章的練習與以往的不同，因為這類的功能並不是Zerojudge（或一般程式競賽、APCS檢測）的主要目的，所以並不會在Zerojudge測試。相反的，此練習將以打造應用程式為目標，並在自己的電腦上完成應用程式。

{% hint style="info" %}
練習利用本章教的內容，寫出`Store`類別，並開設三間`Store`，每間商店有各自的`name`, `location`, `stock`，`stock`是一個字典，key是商品名，value是庫存數。須利用`__init__()`設立一個建構子，建構子中同時需要建立`menu`實例變數，並從`stock`中擷取出`menu`，並且要有`introduction()`方法能夠輸出該商店`Store`的介紹，

* [ ] 寫出`Store`類別
* [ ] 每間商店有各自的`name`, `location`, `stock`
* [ ] `stock`是一個字典，`key`是商品名，`value`是庫存數，例如：

  ```python
  stock = {
      "name1": 4,
      "name2": 7
  }
  ```

* [ ] 利用`__init__()`設立一個建構子，為`name`, `location`, `stock`初始化
* [ ] 建構子中同時需要建立`menu`變數，並從`stock`中擷取出`menu`，`menu`為一`list`，格式

  ```python
  ['name1', 'name2']
  ```

* [ ] 並且要有`introduction()`方法能夠輸出該`Store`的介紹，介紹內容須包含`name`, `location`, `menu`
* [ ] 最後，需要有個`sell()`方法，能夠賣出要求的商品，因此需要傳入一個`product`參數，例如：

  ```python
  def sell(self, product):
    # Do something here.
  ```

* [ ] 運用已經寫好的`din_tai_fung`來測試自己的程式做的對不對
* [ ] 自行增加另外兩間店！
{% endhint %}

{% tabs %}
{% tab title="First Tab" %}
```python
# Your code below




# Your code above

# Example store for you 
din_tai_fung_stock = {
    "Xiaolongbao": 8,
    "Shaohsing Wine Marinated Chicken": 4
}

din_tai_fung = Store("Din Tai Fung", "Taipei", din_tai_fung_stock)

print("The menu of Din Tai Fung:")
print(din_tai_fung.menu)
print()

din_tai_fung.introduction()
print()

din_tai_fung.sell("Xiaolongbao")
din_tai_fung.sell("Xiaolongbao")
din_tai_fung.sell("Xiaolongbao")
din_tai_fung.sell("Shaohsing Wine Marinated Chicken")
print()
```
{% endtab %}

{% tab title="參考解答" %}
```python
class Store:
    def __init__(self, name, location, stock):
        self.name = name
        self.location = location
        self.stock = stock
        self.menu = list(self.stock.keys())
    
    def introduction(self):
        print("{} is located at {}.".format(self.name, self.location))
        print("It sells {}".format(self.menu))
        
    def sell(self, product):
        print("{} was sold.".format(product))
        self.stock[product] -= 1
        print("There are only {} {}.".format(self.stock[product], product))
    
din_tai_fung_stock = {
    "Xiaolongbao": 8,
    "Shaohsing Wine Marinated Chicken": 4
}

din_tai_fung = Store("Din Tai Fung", "Taipei", din_tai_fung_stock)

print("The menu of Din Tai Fung:")
print(din_tai_fung.menu)
print()

din_tai_fung.introduction()
print()

din_tai_fung.sell("Xiaolongbao")
din_tai_fung.sell("Xiaolongbao")
din_tai_fung.sell("Xiaolongbao")
din_tai_fung.sell("Shaohsing Wine Marinated Chicken")
print()
```
{% endtab %}
{% endtabs %}

{% hint style="success" %}
恭喜完成！

你已經掌握了class的基本概念。除了本章所教的概念外，class還有其他功能值得去探索。你也可以試著為剛剛的練習增加一些功能，例如：

1. 增加商品的價錢
2. 新增增減庫存的功能
3. 新增批量銷售的功能

來挑戰自己！
{% endhint %}







