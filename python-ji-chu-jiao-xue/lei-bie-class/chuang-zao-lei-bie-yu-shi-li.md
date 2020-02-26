# 實例 Instance

## 實例 Create Instance

只創造 Class 並不會創造出任何新的物件，因為Class只是一個模板而已，需要透過創造實例來創造新物件，就跟有了int，還要再給他一個數字一樣。 **實例 Instance** 是類別的具象化。**區別類別與實例非常重要！**

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





