# 邏輯運算子

## and

![](<../../.gitbook/assets/image (45).png>)

```python
if month == 8 and day == 15:
	print('中秋節快樂')
else:
	print('平常日')
```

{% hint style="info" %}
**非 0 的數值會視為True**

```python
a = 3.14
if a :
	print('這行會印出來')
```
{% endhint %}

## **or**

![](<../../.gitbook/assets/image (46).png>)

```python
if score >= 60 or times_absence < 3:
	print('及格')
else:
	print('不及格')
```

## **not**

![](<../../.gitbook/assets/image (47).png>)

```python
if not (month == 8 and day == 15):
	print('平常日') 
else:
	print('中秋節快樂')
```

## **練習 : 座標判斷**

**請使用邏輯運算子，寫出一個可以判斷一個點在直角座標上是第幾象限(請加入判斷 X軸、Y軸、與原點 )**

![](<../../.gitbook/assets/image (48).png>)
