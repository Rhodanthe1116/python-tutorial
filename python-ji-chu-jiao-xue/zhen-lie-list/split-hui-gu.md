# split( )回顧

## 回顧

輸入3個整數並輸出 Ex: **17  36  48**

**Before**

```python
a, b, c = input().split()
print(a, b, c)
# 17 36 48
```

**Now**

```python
a = input().split()
print(a)
# ['17', '36', '48']
```

## **split( )轉型**

![](<../../.gitbook/assets/image (66).png>)

### **範例**

```python
data = input().split()
print(data)

# 輸入整數(int):  2020 3 29
# 輸出: ['2020', '3', '29']

# 輸入浮點數(float):  1.0  3.14  -0.2
# 輸出: ['1.0', '3.14', '-0.2']

# 輸入字串(str):  Hello world
# 輸出: ['Hello', 'world']
```

## **split( )切割**

* split()可用來切割字串
* input().split()得到的資料為字串串列
* 可依據括號內的字串進行切割

### 範例

![](<../../.gitbook/assets/image (67).png>)

```python
a = input().split()
# a = ['a,-b,', 'c']
b = input().split(',')
# b = ['a', '-b', ' c']
c = input().split('-')
# c = ['a,', 'b, c']
```

## **任務: split()應用**

### **任務一**

* 輸入:  a,b,c,d,e             &#x20;
* 輸出: **** \['a', 'b', 'c', 'd', 'e']

### 任務二

* 輸入:  123456789     &#x20;
* 輸出:   \['1234', '6789']

### 任務三

小明今天要登錄自己的Gmail，可是小明常常忘記@後面要打甚麼，請你寫一個程式幫幫他，把他的輸入用@分成兩堆

* 輸入: aaaaa@gmiil.com          &#x20;
* 輸出:  \['aaaaa', 'gmiil.com']    &#x20;



* 輸入: abc123@.com.tw            &#x20;
* 輸出:  \['abc123', '.com.tw']
