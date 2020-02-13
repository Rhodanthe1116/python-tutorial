# List

變數是一個一個的，假如有 100 個變數，必須使用`a0、a1、a2、a3、a4......` 太多，改用 List 比較好，變成一個名叫 a 的 List ，每個元素有標籤，`a[0]、a[1]、a[2]、a[3]、a[4]......`

![](../../.gitbook/assets/image%20%2816%29.png)

## 創造 Create

```python
my_list = ["apple", "banana", "cherry"]
print(my_list)
```

#### 或利用`list()`指令

```python
my_list = list(("apple", "banana", "cherry")) # note the double round-brackets
print(my_list)
```

#### 創造空串列，之後可以新增元素

```python
my_empty_list = []
print(my_empty_list)
```

## 輸出但沒有中括號 Print without bracket

```python
my_list = ["apple", "banana", "cherry"]
print(*my_list)
```

## 取用 Access

```python
my_list = ["apple", "banana", "cherry"]
print(my_list[0])
print(my_list[1])
print(my_list[2])
```

## 改變 Change

```python
my_list = ["apple", "banana", "cherry"]
my_list[1] = "blackcurrant"
print(my_list)
```

## 遍歷 Loop trough

{% tabs %}
{% tab title="換行" %}
```python
my_list = ["apple", "banana", "cherry"]
for element in my_list:
    print(element)
```
{% endtab %}

{% tab title="不換行" %}
```python
my_list = ["apple", "banana", "cherry"]
for element in my_list:
    print(element, end=" ")
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
注意有沒有換行的差別，因為預設的`print()`會在「結尾」加上換行，所以若不想換行，必須設定「結尾」為「空白」
{% endhint %}

或利用`range()`

{% tabs %}
{% tab title="換行" %}
```python
my_list = ["apple", "banana", "cherry"]
for i in range(3):
    print(my_list[i])
```
{% endtab %}

{% tab title="沒換行" %}
```python
my_list = ["apple", "banana", "cherry"]
for i in range(3):
    print(my_list[i], end=" ")
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
再次提醒有沒有換行的差別
{% endhint %}

{% hint style="warning" %}
注意！這裡跟直接`print(my_list)有什麼差別？`
{% endhint %}

## 反向遍歷 Reversed loop trough

```python
my_list = [1, 2, 3, 4, 5]
for element in reversed(my_list):
    print(element, end=" ")
```

## 檢查 Check

```python
my_list = ["apple", "banana", "cherry"]
if "apple" in my_list:
     print("Yes")
```

```python
my_list = ["apple", "banana", "cherry"]
if "orange" not in my_list:
    print("Yes")
```

## 長度 List Length

```python
my_list = ["apple", "banana", "cherry"]
print(len(my_list))
```

## 新增 Add items

```python
my_list = ["apple", "banana", "cherry"]
my_list.append("orange")
print(my_list)
```

## 移除最後一項 Remove last item

```python
my_list = ["apple", "banana", "cherry"]
my_list.pop()
print(my_list)
```

## 複製 Copy

```python
my_list = ["apple", "banana", "cherry"]

my_copy_list = my_list.copy() 
my_copy_list[1] = "orange"
print(my_list)
print(my_copy_list)
```

{% hint style="danger" %}
以下為錯誤用法

```python
my_list = ["apple", "banana", "cherry"]

my_copy_list = my_list
my_copy_list[1] = "orange"
print(my_list)
print(my_copy_list)
```
{% endhint %}

或利用`list()`

```python
my_list = ["apple", "banana", "cherry"]
my_copy_list = list(my_list)
print(my_copy_list)
```

## 擷取 Slice

用法類似`range()`

```python
l = [0, 1, 2, 3, 4]
# left and right
print(l[1])
print(l[1:3])
# non-stop
print(l[1:])

# reverse
print(l[-1])
print(l[-2])

# step
print(l[0::2])
print(l[4::-2])
```

也可以用來替換

```python
l = [0, 1, 2, 3, 4]
l[2:4] = ["a", "b", "c"]
print(l)
```



## 加法 Add

```python
l = [0, 1, 2]
l += [3, 4]
print(l)
```



