# 取用變數屬性

在前個部分，創造出了一個類別與實例，也為他設定了屬性，但實際要如何使用呢？其實大致就跟一般使用變數一樣，只要利用`.`來表明屬性是屬於哪個物件的即可：

```python
class Charactor:
     hp = 100

new_charactor = Charactor()

# new_charactor.hp
print(new_charactor.hp)
# 100
```

在class的定義中，將定義了hp這個變數，並將其值設為100，而在new\_charactor時便會自動擁有這個變數，之後在程式中，若要使用這個變數，只要使用`.`來取得即可。使用方法與一般變數相同，設值也是：

```python
new_charactor.hp = 50
print(new_charactor.hp)
# 50
```

#### 不同的實例不共用屬性

假如今天有兩個實例，若做以下操作：

```python
class Charactor:
     hp = 100

charactor_1 = Charactor()
charactor_2 = Charactor()

charactor_1.hp = 70

print(charactor_1.hp)
print(charactor_2.hp)
# 70
# 100
```

可以發現兩者的hp不一樣，因為每個實例顯然需要是獨立的。

{% hint style="info" %}
試著創造一個學生Class，為其設定「名字」跟「號碼」兩個屬性。
{% endhint %}

## 💻練習

{% hint style="info" %}
* [ ] 將下列程式碼中new\_song的name, artist, album, year設定成任何你想要的
* [ ] 輸出四個變數
{% endhint %}

{% tabs %}
{% tab title="First Tab" %}
```python
class Song:
    name = "song name"
    artist = "artist name"
    album = "album name"
    year = 9999
    
new_song = Song()
```
{% endtab %}

{% tab title="參考答案" %}
```python
class Song:
    name = "song name"
    artist = "artist name"
    album = "album name"
    year = 9999
    
new_song = Song()

print(new_song.name)
print(new_song.artist)
print(new_song.album)
print(new_song.year)
```
{% endtab %}
{% endtabs %}



## 

