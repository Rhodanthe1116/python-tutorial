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

4

要注意雖然物件的名稱是小寫bobo，但物件的name屬性是大寫的Bobo

## 請問Python中建構子的語法為何？

1. init
2. \_\_init\_\_
3. \_\_create\_\_
4. \_\_new\_\_

2

要記得init前後各加上兩個底線

## 請問對下面的類別，要如何創造一個實例？

```python
class Tree:
    name = 'Royal Palm'
```

1. new\_tree = Tree\(\)
2. new\_tree = Tree
3. new\_tree = new Tree\(\)
4. new\_tree = new Tree

1

1為正確語法，其他皆不正確

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

3

id與self.id為不同變數。

## 請問如何創造下列程式中類別的實例？

```python
class User:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

1. User.create\("Gary", 15\)
2. User.\_\_init\_\_\("Gary", 15\)
3. User\(\)
4. User\("Gary", 15\)

4

User\(\)裡面的引數數量需與\_\_init\_\_\(\)函數的參數數量相同（不包含self）

## 若有一類別B要繼承A，在B的建構子中要用以下哪個語法來調用父類別的建構子？

1. self.\_\_init\_\_\(\)
2. parent.\_\_init\_\_\(self\)
3. B.\_\_init\_\_\(\)
4. B.\_\_init\_\_\(self\)

4

此為python語法

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

1

Warrior繼承Character，會將所有成員都保留，包含walk\(\)及attack\(\)，即使attack\(\)被改寫了也不會影響walk\(\)

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

3

Warrior繼承Character，會將所有成員都表留，包含walk\(\)及attack\(\)，而在Warrior中，attack\(\)被改寫了，因此執行的是Warrior的attack\(\)而不是Character的attack\(\)

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
2. B繼承A，因此自動繼承A裡所有的資料
3. 創造b的時候，需要在B\(\)裡面放入一參數，如B\(5\)
4. 變數j不能被b所取用

1

i為一實例變數，繼承不會自動繼承實例變數，因為在B裡面沒有調用A的建構子。若在B裡面加上A.\_\_init\_\_\(self\)即可解決這個問題

## 下列關於public與private的描述，何者錯誤？

1. public的成員可以在class外被讀取與修改
2. private的成員無法在class外被讀取與修改
3. 同樣class中的method可以修改public的成員
4. 同樣class中的method不能修改private的成員

4

同樣class中的method可以修改同樣class中的private成員，又或者說private的成員正是需要透過method來修改。

