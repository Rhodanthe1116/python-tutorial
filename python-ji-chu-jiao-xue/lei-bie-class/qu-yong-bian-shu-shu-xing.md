# 實例變數 Instance Variable

類別與實例必須要區分開來，類別是模板，而實例是類別的具體化，但為什麼需要區分呢？因為每個實例可以擁有他特有的**實例變數 Instance Variable**，且只有在實例被實例化之後才會存在，相較於類別變數是所有類別實例所共有，實例變數可以只存在於特定變數，例如：

```python
class Circle:
  pi = 3.14

# Initialization
red_circle = Circle()
big_circle = Circle()

# Color and radius are both instance variables
red_circle.color = "red"
hollow_circle.type = "hollow"
```

在上例中，紅圓有color屬性，而空心圓有type屬性，兩個屬性都是圓所沒有的，兩者都是實例變數，在成為實例之後才出現的。

## 類別變數與實例變數

傳統上，會將每個實例共有且不會改變的性質設為類別變數，而每個實例都不同的性質設為實例變數，通常在初始化的時候進行實例變數的設值，來減少程式碼的重複。

但若是執行下列程式：

```python
class Circle:
  # Default color is red.
  color = "red"

red_circle = Circle()
green_circle = Circle()

# Overide the default color which is a class variable
green_circle.color = "green"
```

上列程式碼有個圓，並且有個color類別變數，但在第9行的地方，用了實例變數的方式設了值，這時候實例變數會覆蓋類別變數，讓green\_circle.color變成實例變數，一個獨特的屬性。

因為類別變數與實例變數的取用方式一樣，都是用`.`，所以以上程式碼不會發生任何錯誤。

## 💻練習

{% hint style="info" %}
* [ ] 將下列程式碼中new\_song的name, artist, album, year設定成任何你想要的
* [ ] 輸出四個變數
{% endhint %}

{% tabs %}
{% tab title="First Tab" %}
```python
class Song:
    name = ""
    artist = ""
    album = ""
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

