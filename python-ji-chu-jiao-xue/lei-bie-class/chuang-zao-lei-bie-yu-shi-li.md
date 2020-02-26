# 創造類別與實例

## 創造類別 Create a Class

Class 可以幫助我們創造物件的模板或原型

```python
class Charactor:
    hp = 100
```

上方利用`class`創造出一個叫`Charactor`的自訂資料型態，我們可以在裡面加上`hp`這個**屬性（attrtibute, property）**，或可稱**成員變數（member variable）**。屬性可以有很多個，例如也可以在角色身上增加mp：

```python
class Charactor:
    hp = 100
    mp = 50
```

{% hint style="info" %}
Magic point，常簡寫為「MP」，或稱「Mana」
{% endhint %}

注意在這裡我們只是撰寫模板，Charactor並不能當作變數使用，應該當成資料型態來看，所以我們不能直接對Charactor做操作，就像我們不會直接用int當變數名稱一樣。若要使用Charactor，我們需要創造出一個類別實例。

## 創造類別實例 Create Class Instance

只創造 Class 並不會創造出任何新的物件，因為Class只是一個模板而已，需要透過創造實例來創造新物件，就跟有了int，還要再給他一個數字一樣。 **實例 Instance** 是類別的實體化。

```python
class Charactor:
     hp = 100

# Create instance
new_charactor = Charactor()

print(type(new_charactor))
# <class '__main__.Charactor'>
```

在第 5 行利用`Charactor()`創造一個新的實例物件，再將`new_charactor`指定為他。若利用type\(\)會發現他的class為Charactor

## 💻練習

{% hint style="info" %}
* [ ] 參考上面的說明，撰寫一個名為song的類別
* [ ] 為他加上name, artist, album三個屬性
* [ ] 創造一個實例，取名new\_song
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

print(type(new_song))
```
{% endtab %}
{% endtabs %}





