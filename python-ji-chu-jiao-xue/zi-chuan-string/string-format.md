# String Format 字串格式化

之前都會用+來連接字串，但如果要內插變數的話，便很不方便，如下：

{% hint style="warning" %}
```python
age = "36"
print("My name is John, and I am " + age + ".")
```
{% endhint %}

甚至不能合併非字串：

{% hint style="danger" %}
```python
# age is integer
age = 36
print("My name is John, and I am " + age + ".")
# TypeError: can only concatenate str (not "int") to str
```
{% endhint %}

在此介紹比較好的方法，叫做**字串格式化**，在有些語言中也稱作**內插（interpolation）**

## 字串格式化

{% hint style="success" %}
```python
age = 36
print("My name is John, and I am {}.".format(age))
```
{% endhint %}

等同於

```python
age = 36
txt = "My name is John, and I am {}"
print(txt.format(age))
```

## 多重參數

```python
quantity = 3
itemID = 567
price = 4999
myorder = "I want {} pieces of item {} for {} dollars."
print(myorder.format(quantity, itemID, price))
```

## 多重參數加標籤

```python
quantity = 3
itemID = 567
price = 4999
myorder = "I want to pay {2} dollars for {0} pieces of item {1}."
print(myorder.format(quantity, itemID, price))
```

## 控制精度

會自動四捨五入

```python
pi = 3.14159265359
print(pi)
print("輸出pi到小數點後第2位 {:.2f}".format(pi))
print("輸出pi到小數點後第4位 {:.4f}".format(pi))
print("輸出pi到小數點後第6位 {:.6f}".format(pi))
```

也可同時利用標籤：

```python
quantity = 3
itemID = 567
price = 4999.1267
myorder = "I want to pay {2:.2f} dollars for {0} pieces of item {1}."
print(myorder.format(quantity, itemID, price))
```

## 利用關鍵字

```python
latitude = input()
longitude = input()

print('座標: {latitude}, {longitude}'.format(
    latitude=latitude,
    longitude=longitude
))
```

## 進階用法

```python
coord = {'latitude': '37.24N', 'longitude': '-115.81W'}
print('座標: {latitude}, {longitude}'.format(**coord))
```
