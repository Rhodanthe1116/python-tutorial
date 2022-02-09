# 輸出 Print

## 列印函式 print()

將想要印出的文字包含在print("裡面")

```python
print("想要輸出的文字")
```

```python
print("Hello, world")
```

{% hint style="warning" %}
用 ' 或 "" 包住文字
{% endhint %}

## **改變結尾 ( end )，不換行**

```python
print(1, end="")
print(2, end="")
```

{% hint style="info" %}
這樣數字會黏在一起，不好看
{% endhint %}

```python
print(1, end=" ") 
print(2, end=" ")
```

## 註解

`#`之後的文字是註解，之後會常用到

```python
# 在此為註解，電腦不會處理
print("hello, world") 
```

{% hint style="info" %}
比較

```python
print("hello,", end = ' ')
print("world")
```

v.s.

```python
print("hello,")
print("world")
```
{% endhint %}

{% hint style="info" %}
試試看

```python
print("hello,", end = ' ')
print()
print("world")
print("hello,")
```

v.s.

```python
print("hello,", end = ' ')
print(end = '')
print("world")
```
{% endhint %}
