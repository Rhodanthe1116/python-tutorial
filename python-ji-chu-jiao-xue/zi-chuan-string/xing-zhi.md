# String

## 多行字串

```python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
print(a)
```

## 類似 list 的 index

```python
str = "abcde"
print(str[0])
print(str[1])

print("---------------")

str = "a b c d e"
print(str[0])
print(str[1])
print(str[-1])
print(str[2:])
```

```python
str = "a b c d e"
print(str[::2])
print(str[1::2])
print(str[::-1])
```

```python
s = 'abcdefghijklm'

print(s[0:10:2])

print("---------------")

for i in range(0, 10, 2):
    print(i, s[i])
```

{% hint style="danger" %}
特別注意！string 是不可變的，不像list 是可變的，例如：

```python
l = [0, 1, 2, 3, 4]
# OK
l[0] = 999

s = "abcde"
# Error
s[0] = "X"
```
{% endhint %}

## 長度 len\(\)

```python
str = "abcde"
print(len(str))
```

## 乘法

```python
str = "~"
print(str * 5)
```

## 檢查 Check

```python
txt = "The rain in Spain stays mainly in the plain"
x = "ain" in txt
print(x)
```

