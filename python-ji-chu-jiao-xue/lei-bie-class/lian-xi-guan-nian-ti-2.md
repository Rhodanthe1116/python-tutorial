# ⚡ 練習：觀念題2

## 請問下列程式會輸出什麼？

```python
class User:
  def __init__(self, name):
    self.name = name
    print("Hiya {}!".format(self.name))
  
bobo = User("Bobo")
```

1. Hiya
2. bobo
3. Hiya bobo!
4. Hiya Bobo!

## 請問Python中建構子的語法為何？

1. init
2. \_\_init\_\_
3. \_\_create\_\_
4. \_\_new\_\_

## 請問對下面的類別，要如何創造一個實例？

```python
class Tree:
    name = 'Royal Palm'
```

1. new\_tree = Tree()
2. new\_tree = Tree
3. new\_tree = new Tree()
4. new\_tree = new Tree

## 請問下列程式會輸出什麼？

```python
class Sales:
    def __init__(self, id):
        self.id = id
        id = 100

val = Sales(123)
print (val.id)
```

1. SyntaxError
2. 100
3. 123
4. 50

## 請問如何創造下列程式中類別的實例？

```python
class User:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

1. User.create("Gary", 15)
2. User.\_\_init\_\_("Gary", 15)
3. User()
4. User("Gary", 15)

## 若有一類別B要繼承A，在B的建構子中要用以下哪個語法來調用父類別的建構子？

1. self.\_\_init\_\_()
2. parent.\_\_init\_\_(self)
3. B.\_\_init\_\_()
4. A.\_\_init\_\_(self)

## 請問下列程式會輸出什麼？

```python
class Character:
   def walk(self):
        print("*walking*")

   def attack(self):
        print("OOH!")

class Warrior(Character):
    def attack(self):
        print("AHH!")
    
new = Warrior()
new.walk()
```

1. \*walking\*
2. OHH!
3. AHH!
4. AttributeError

## 請問下列程式會輸出什麼？

```python
class Character:
   def walk(self):
        print("*walking*")

   def attack(self):
        print("OOH!")

class Warrior(Character):
    def attack(self):
        print("AHH!")
    
new = Warrior()
new.attack()
```

1. \*walking\*
2. OHH!
3. AHH!
4. AttributeError

## 請問對於下列程式碼的敘述，何者正確？

```python
class A:
    def __init__(self, i = 0):
        self.i = i

class B(A):
    def __init__(self, j = 0):
        self.j = j

def main():
    b = B()
    print(b.i)
    print(b.j)

main()

```

1. B繼承A，但A裡面的i沒有被繼承
2. B繼承A，因此自動繼承A裡所有的資料，所以i也被繼承了
3. 創造b的時候，需要在B()裡面放入一參數，如B(5)
4. 變數j不能被b所取用

## 下列關於public與private的描述，何者錯誤？

1. public的成員可以在class外被讀取與修改
2. private的成員無法在class外被讀取與修改
3. 同樣class中的method可以修改public的成員
4. 同樣class中的method不能修改private的成員
