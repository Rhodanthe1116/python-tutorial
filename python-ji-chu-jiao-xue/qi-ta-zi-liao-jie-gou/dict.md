# 字典 Dictionary

假如要製作以下的表格，可以用字典：

| Name | Class | Age |
| :--- | :--- | :--- |
| Mandy | 4 | 15 |

程式碼實作如下：

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}
print(d)
```

有標籤的集合，無序、不重複、可以改變。

包含兩個東西

|  | Description | Example | Like |
| :--- | :--- | :--- | :--- |
| **Key** | 標籤 | name | Excel 的標題列 |
| **Value** | 值 | Mandy | Excel 的儲存格 |

## Create

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}
print(d)
```

#### 空 Dictionary

```python
d = {}
print(d)
print(type(d))
```

## Access

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}

print(d["name"])
# OR
print(d.get("name"))
```

## Change Values

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}

print(d["age"])
d["age"] = 16
print(d["age"])
```

## Loop Through

### key

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}

for key in d:
  print(key)
```

### value

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}

for value in d.values():
  print(value)
```

Or

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}

for key in d:
  print(d[key])
```

### key and value

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}

for key, value in d.items():
  print(key, value)
```

## Check

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}

if "name" in d:
    print("Yes")
```

## Length

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}

print(len(d))
```

## Add

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}

d["number"] = 10
print(d)
```

## Remove

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}
 
d.pop("class")
print(d)
# OR
del d["age"]
print(d)
```

## Clear

```python
d.clear()
```

```python
del d
```

## Copy

{% hint style="danger" %}
```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}
 
d_copy = d
d_copy["name"] = "Sean"
print(d)
print(d_copy)
```
{% endhint %}

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}

d_copy = d.copy()
d_copy["name"] = "Sean"
print(d)
print(d_copy)
```

Or

```python
d = {
    "name": "Mandy",
    "class": 4,
    "age": 15
}

d_copy = list(d)
d_copy["name"] = "Sean"
print(d)
print(d_copy)
```

## Nested Dictionary

```python
d = {
    "student1" : {
        "name" : "Mini",
        "age" : 19
    },
    "student2" : {
        "name" : "Sean",
        "age" : 18
    },
    "student3" : {
        "name" : "Brian",
        "age" : 20
    }
}

print(d["student1"]["name"])
```

## Sort

非常重要！非常常用！

```python
d = {"Sean": 18, "Mandy": 15, "Mini": 19}
l = sorted(d.items(), key= lambda t: t[1])
print(l)
```

`sorted()`會將`d.item()`做排序，並回傳一個 List。而排序的依據為`key`，這裡我們希望依照 value 來排，利用了一個較複雜的方法，在此只要知道可以這樣使用，若將`t[1]`改成`t[-1]`可做降序排序

```python
d = {"Sean": 18, "Mandy": 15, "Mini": 19}
l = sorted(d.items(), key= lambda t: -t[1])
print(l)
```

若要根據兩個key做排序，先比第一個key，若第一個key一樣的話，再比第二個key，可以這樣做：

```python
d = {"Benson": 18, "Dick": 15, "Cindy": 15}
l = sorted(d.items(), key= lambda t: (t[1], t[0]))
print(l)
```

## Others

### create

```python
d = dict(name="Mandy", c=4, age=15)
print(d)
```

 or

```python
d = dict([("name", "Mandy"), ("class", 4), ("age", 15)])
print(d)
```

