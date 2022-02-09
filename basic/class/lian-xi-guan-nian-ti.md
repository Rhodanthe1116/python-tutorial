# ⚡ 練習：觀念題

## 請問下列何者定義了一個共通的模板？

1. ​實例 Instance
2. 類別 Class
3. 屬性 Attribute
4. 方法 Method

## 請問下列何者代表一個獨一無二的實體？

1. ​實例
2. 類別
3. 屬性
4. 方法

## Python中的type()函數有什麼作用？

1. 回傳物件的類別
2. 回傳一個類別的實例
3. 回傳一個字串，字串的內容為物件的類別
4. 回傳物件的名稱

## 下列哪個字代表類別定義的開始（下列程式碼中的xxx應填入何者？）

```python
xxx Dog():
  name = ''
  yyy zzz():
    self.name = 'bobby'
```

1. \_\_init\_\_
2. type
3. class
4. def

## 請問方法中第一個參數為何？

1. 物件自己的實例，通常稱作self
2. 物件自己的類別，通常稱作self
3. 物件的屬性，通常稱作this
4. 物件的名稱，為一字串

## 請問要如何取用物件的屬性？

1. object.attr
2. object->attr
3. object:attr
4. object\[attr]

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

## 請問下列關於method與function的敘述，何者錯誤？

1. 在class內定義稱為method，在class外定義稱為function
2. method的前面須指明類別實例，function前面則不用
3. method只能用在改變class內的屬性，不能改變class外的變數
4. function可以改變class內的屬性，也可以改變class外的變數

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



