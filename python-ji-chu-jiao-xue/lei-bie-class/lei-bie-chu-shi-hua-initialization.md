# 建構子 Constructors

在之前的教學中，學到可以在類別中定義函數。這邊要介紹一個特別的方法，稱作「\_\_init\_\_\(\)」，可以用來初始化 initialize 物件，而且這個方法只會執行一次，只會在物件第一次被創造的時候執行。

{% hint style="info" %}
初始化的意思類似於歸零重來，或將系統恢復成剛開始的樣子
{% endhint %}

```python
class Charactor:
    def __init__(self):
        print("Successfully created a new Charactor!")

# __init__() called
user = Charactor()

print(user.hp)
```

上例中的\_\_init\_\_\(\)便是初始化函數，在一般物件導向的程式語言中也稱作**建構子**。他在第7行的時候在呼叫Charactor\(\)的時候會跟著執行。\_\_init\_\_\(\)只會執行一次！

當然也可以傳入參數到\_\_init\_\_裡：

```python
class Charactor:
    def __init__(self, name):
        print("Successfully created a new Charactor called {}!".format(name))

# !!
new_charactor = Charactor("Cindy")
print(user.hp)
```

注意第6行將參數傳到Charactor裡面，就等同於將參數傳到\_\_init\_\_裡面。

