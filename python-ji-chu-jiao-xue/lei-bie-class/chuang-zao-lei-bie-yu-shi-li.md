# 實例 Instance

## 實例 Create Instance

只定義 Class 並不會創造出任何新的物件，因為Class只是一個模板而已，需要透過創造實例來創造新物件，就跟有了int，還要再給他一個數字一樣。 **實例 Instance** 是類別的具象化。**區別類別與實例非常重要！**

```python
class Character:
     name = "loser"
     hp = 100

# Create instance 1
new_character_1 = Character()
# Create instance 2
new_character_2 = Character()

print(type(new_character1))
# <class '__main__.Character'>
```

在第 5 行利用`Characer()`創造一個新的實例物件，再將`new_character1`指定為他。若利用`type()`會發現他的class為`Character`

## 取用變數

在前個部分，創造出了一個類別與實例，也為他設定了屬性，但實際要如何使用呢？其實大致就跟一般使用變數一樣，只要利用`.`來表明屬性是屬於哪個物件的即可：

```python
class Character:
     name = ""
     hp = 100
    
new_character_1 = Character()
new_character_1.name = "winner"

print(new_character_1.name) # "winner"
print(new_character_1.hp) # 100


new_character_2 = Character()
new_character_2.name = "loser"

print(new_character_2.name) # "loser"
print(new_character_2.hp) # 100
```

在`class`的定義中，定義了`name, hp`這個兩個變數，並將其設定預設值，而在第4行的`new_circle`實例便會自動擁有這個類別變數，之後在程式中，若要使用這個變數，只要使用`.`來取得即可。使用方法與一般變數相同。



















## 💻練習

{% hint style="info" %}
* [ ] 參考上面的說明，撰寫一個名為`Song`的類別
* [ ] 為他加上`name`, `artist`, `album`三個屬性
* [ ] 創造一個實例，取名`new_song`
{% endhint %}

{% tabs %}
{% tab title="First Tab" %}

{% endtab %}

{% tab title="參考答案" %}
```python
class Song:
    name = "song name"
    artist = "artist name"
    album = "album name"
    
new_song = Song()
```
{% endtab %}
{% endtabs %}

