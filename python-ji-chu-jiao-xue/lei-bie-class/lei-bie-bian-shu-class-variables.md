# 類別變數 Class Variables

在類別中創造的變數，我們稱為**類別變數Class variable**，類別變數是所有實例所共有的，且都擁有相同的值。比如說要定義一個圓的類別：

```python
class Circle:
    pi = 3.14
```

因為圓周率對於每個圓都一樣，不論圓的半徑是多少，都可以當作3.14，所以可以設成類別變數，讓所有圓共享。

## 取用變數

在前個部分，創造出了一個類別與實例，也為他設定了屬性，但實際要如何使用呢？其實大致就跟一般使用變數一樣，只要利用`.`來表明屬性是屬於哪個物件的即可：

```python
class Circle:
    pi = 3.14
    
new_circle = Circle()

print("The value of pi of circles is {}.".format(new_circle.pi))
# The value of pi of circles is 3.14.
```

在`class`的定義中，定義了`pi`這個類別變數，並將其值設為`3.14`，而在第4行的`new_circle`實例便會自動擁有這個類別變數，之後在程式中，若要使用這個變數，只要使用`.`來取得即可。使用方法與一般變數相同。

## 💻練習

{% hint style="info" %}
* [ ] 撰寫一個`Dog`類別
* [ ] 為他加上`legs`類別變數，並設定值
* [ ] 創造一個實例，取名`husky`
* [ ] 輸出~~`Every dog has {legs} legs.`~~
{% endhint %}

{% tabs %}
{% tab title="First Tab" %}

{% endtab %}

{% tab title="參考答案" %}
```python
class Dog:
    legs = 4
    
husky = Dog()

print("Every dog has {} legs.".format(husky.legs))
# Every dog has 4 legs.
```
{% endtab %}
{% endtabs %}

