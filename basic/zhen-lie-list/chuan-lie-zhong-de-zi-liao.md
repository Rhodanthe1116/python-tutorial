# 串列中的資料

**在 list 型態中，可以使用 \[ ]來找出指定的元素**

* **串列的元素從0開始**

![](<../../.gitbook/assets/image (101).png>)

```python
print(data[0], data[3]) 
# 輸出 a d
print(data[4])
# error!
```

## **串列的索引值**

* 索引值須為整數(int)型態
* 索引值的大小需在串列長度範圍內

### 範例 

![](<../../.gitbook/assets/image (99).png>)

```python
print(data[2]) 
# 🡪 從0開始數到2，所以是第3個!
print(data[1.5])
# 🡪 error
print(data[-2])
# 🡪 reverse (反轉)
print(data[5])
# 🡪 list index out of range (超出串列範圍)
print(data['first'])
# 🡪 error
num = 3
print(data[num])
# 因為num = 3，型態為整數(int)，	等同於print(data[3])
```

## **修改串列中的資料**

透過他們的索引值，可以找到串列中指定的資料，並對他進行修改\


例如原本的串列：

![](<../../.gitbook/assets/image (86).png>)

經過：

```python
data = input().split()
data[2] = 22
```

會變成：

![](<../../.gitbook/assets/image (92).png>)
