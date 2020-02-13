# 輸出 Print

## 註解

`#`之後的文字是註解，之後會常用到

```python
# 在此為註解，電腦不會處理
print("hello, world")            
```

詳細可見「註解」篇

## 輸出（print）

```python
print("想要輸出的文字")
```

```python
print("Hello, world")
```

{% hint style="warning" %}
記得要打雙引號「"」
{% endhint %}

只輸出「數字」

```python
print(100)
```

{% hint style="warning" %}
文字和數字是不一樣的！
{% endhint %}

```python
print("100")        # 文字         
print(100)          # 數字 
print("文字100")     # 文字
```

{% hint style="danger" %}
```python
print(輸出100)        
# 不行！因為沒有「""」會被認為是數字
# 但「輸出」兩字不是數字
```
{% endhint %}

## 空行

```python
print(1)
# !!
print()    
print(2)
```

{% hint style="info" %}
所以我們知道`print()`之後都會自動換行，那不換行呢？
{% endhint %}

## 不換行

```python
print(1, end="")
print(2, end="")
```

注意有沒有換行的差別，因為預設的print\(\)會在「結尾 」加上「換行」，所以若不想換行，必須設定「結尾」為「空」。

{% hint style="info" %}
這樣數字會黏在一起，不好看
{% endhint %}

## 不換行並空一格

```python
print(1, end=" ")
print(2, end=" ")
```

這裡設定「結尾」為「一格空白」，所以1後面會緊接著一個空白鍵，2也是。

## 分隔 Seperate

可以設定結尾，也可以設定分隔。

```python
print(1, 2, 3)
print(1, 2, 3, sep="|")
print(1, 2, 3, sep="")
```



