# String 處理

## 分割 split\(\)

```python
str = "1 2 3 4 5"
print(str.split())
```

存進 list：

```python
str = "1 2 3 4 5"

list = str.split()
print(list)
```

存成 int list

```python
str = "1 2 3 4 5"

listStr = str.split()
listInt = list(map(int, listStr))
print(listInt)
```

## 尋找 find\(\) and rfind\(\)

find\(\)

```python
s = 'Hello'
print(s.find('e'))
print(s.find('ll'))
print(s.find('L'))
```

 rfind\(\)

```python
s = 'abracadabra'
print(s.find('b'))
# 1
print(s.rfind('b'))
# 8
```

邊界：左邊界和右邊界，英文是 left, right，分別是 l, r

find\(substring, left, right\)

```python
s = 'my name is bond, james bond, okay?'
print(s.find('bond'))
print(s.find('bond', 12))
```

## 取代 replace\(\)

```python
str = 'a bar is a bar, essentially'
print(str.replace('bar', 'pub'))
```

或是替換有限次數

```python
str = 'a bar is a bar, essentially'
print(str.replace('bar', 'pub', 1))
```

## 計數 count\(\)

```python
print('Abracadabra'.count('a'))
# 4
print(('aaaaaaaaaa').count('aa'))
# 5
```

  s.count\(substring, left, right\)

## 大小寫 lower\(\) and upper\(\)

```python
a = "Hello, World!"
print(a.lower())
print(a.upper())
```

## 去除前後 strip\(\)

r移除空格

```python
a = "    123    "
print(a.strip())
```

移除字元

```python
b = "00001230000"
print(b.strip("0"))
```

## 判斷字母數字 isalpha\(\) and isdigit\(\)

```python
print("abc".isalpha(), "abc".isdigit())
print("123".isalpha(), "123".isdigit())
```

```python
print("abc123".isalpha(), "abc123".isdigit())
```

## 參考 Reference

[https://www.w3schools.com/python/python\_ref\_string.asp](https://www.w3schools.com/python/python_ref_string.asp)

