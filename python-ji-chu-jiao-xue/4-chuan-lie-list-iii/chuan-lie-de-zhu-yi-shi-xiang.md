# 串列的注意事項

## 串列的等號

![](<../../.gitbook/assets/image (87).png>)

```python
a = 1
b = a
b = 2
print(a, b)
# 輸出: 1 2
```

```python
a = [1, 2, 3]
b = a
b[0] = 'z'
print(a, b)

# 輸出:
# ['z', 2, 3] ['z', 2, 3]
```

## 想一想

```python
a = ['a', 'b', 'c']
b = a
b = [1, 2, 3]
print(a, b)

# 輸出:
# ['a', 'b', 'c'] [1, 2, 3]
```

￼

![](<../../.gitbook/assets/image (88).png>)

### 比較

```python
a = 5
b = a
b = 7
print(a, b)
# 輸出: 5 7
```

## 串列的複製

### 串列切片

```python
a = [1, 2, 3]
b = a[:]
b[0] = 'z'
print(a, b)

# 輸出:
# [1, 2, 3] ['z', 2, 3]
```

![](<../../.gitbook/assets/image (89).png>)

