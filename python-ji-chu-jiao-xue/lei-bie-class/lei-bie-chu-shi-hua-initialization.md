# 建構子 Constructors

在之前的教學中，學到可以在類別中定義函數。這邊要介紹一個特別的方法，稱作「`__init__()`」，可以用來初始化 initialize 物件，而且這個方法只會執行一次，只會在物件第一次被創造的時候執行。

{% hint style="info" %}
初始化的意思類似於歸零重來，或將系統恢復成剛開始的樣子
{% endhint %}

```python
class Character:
    def __init__(self):
        print("Successfully created a new Character!")

# __init__() was called.
user = Character()
```

上例中的`__init__()`便是初始化函數，在一般物件導向的程式語言中也稱作**建構子**。他在第`7`行的時候在呼叫`Character()`的時候會跟著執行。`__init__()`只會執行一次！

當然也可以傳入參數到`__init__()`裡：

```python
class Character:
    def __init__(self, name):
        print("Successfully created a new Character called {}!".format(name))

# !!
new_character = Character("Cindy")
```

注意第`6`行將參數傳到`Character()`裡面，就等同於將參數傳到`__init__()`裡面。

## 💻練習

{% hint style="info" %}
試著利用`__init__()`寫出可以接收網址`url`的`Website`類別

* [ ] 寫出`Website`類別
* [ ] 接者在`Website`裡面加上`__init__()`，並要可以接收`url`參數。別忘了`self`
* [ ] 在`__init__()`中，輸出以下格式：

  ```text
  Your site has been published as {url}!
  ```

* [ ] 在主程式中，創造`myshop`實例，並傳`"myshop.com"`進建構子
* [ ] 完成！
{% endhint %}

{% tabs %}
{% tab title="First Tab" %}
```python

```
{% endtab %}

{% tab title="參考答案" %}
```python
class Website:
    def __init__(self, url):
        print("Your site has been published as {}!".format(url))
        
myshop = Website("myshop.com")
```
{% endtab %}
{% endtabs %}

