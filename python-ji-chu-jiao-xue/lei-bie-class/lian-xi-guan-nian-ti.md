# ⚡ 練習：觀念題

## 請問下列何者定義了一個共通的模板？

1. 物件
2. 類別
3. 屬性
4. 方法

2

類別為物件的模板。

## 請問下列何者代表一個獨一無二的實體？

1. 物件
2. 類別
3. 屬性
4. 方法

1

每個物件都是獨一無二的，其中一個物件的資料改變不會造成所有物件的資料改動

## Python中的type()函數有什麼作用？

1. 回傳物件的類別
2. 回傳一個類別的實例
3. 回傳一個字串，字串的內容為物件的類別
4. 回傳物件的名稱

1

type回傳一個物件的類別，但並不是以字串型態回傳

## 下列哪個字代表類別定義的開始

1. \_\_init\_\_
2. type
3. class
4. def

3

class代表類別定義的開始

## 請問方法中第一個參數為何？

1. 物件自己的實例，通常稱作self
2. 物件自己的類別，通常稱作self
3. 物件的屬性，通常稱作this
4. 物件的名稱，為一字串

1

self為一實例。

## 請問要如何取用物件的屬性？

1. object.attr
2. object->attr
3. object:attr
4. object\[attr]

1

自己創造的類別的屬性取用方法與平常使用內建型態的方法相同，都是使用.來取用

## 請問下列程式會輸出什麼？

```python
class Tree:
    name = 'Royal Palm'
    
new_tree = Tree()
another_tree = Tree()
another_tree.name = 'Taiwan Date Palm'

print(new_tree.name, another_tree.name, sep=', ')
```

1. Royal Palm, Taiwan Date Palm
2. Taiwan Date Pale, Royal Palm
3. Royal Palm, Royal Palm
4. Taiwan Date Palm, Taiwan Date Palm

1

在class內建立的變數都是 class 的屬性，稱為類別變數，不同實力的類別變數獨立且不互相影響。

## 請問下列程式會輸出什麼？

```python
class Circle:
    radius = 0
      
    def getDiameter(self):
        return 2 * radius

new_circle = Circle()
new_circle.radius = 5

print(new_circle.getDiameter())
```

1. 5
2. 0
3. 10
4. NameError

4

第5行會產生NameError: name 'radius' is not defined。radius應該要改為self.radius才正確。使用類別變數時，必須要明確指出self才不會出錯。

## 請問下列關於method與function的敘述，何者錯誤？

1. 在class內定義稱為method，在class外定義稱為function
2. method的前面須指明類別實例，function前面則不用
3. method只能用在改變class內的屬性，不能改變class外的變數
4. function可以改變class內的屬性，也可以改變class外的變數

3

method也可以改變class外的變數，但為了方便維護，會盡量避免更改外部變數

## 請問下列程式會輸出什麼？

```python
class Tree:
    name = 'Royal Palm'
    
def myPrint(tree):
    print(tree.name, tree.height)
    
newTree = Tree()
myPrint(newTree)
newTree.height = '15.234'
```

1. Royal Palm
2. Royal Palm 15.234
3. AttributeError
4. SyntaxError

3

在第五行的時候，newTree還沒有height這個屬性，因此產生AttributeError。



