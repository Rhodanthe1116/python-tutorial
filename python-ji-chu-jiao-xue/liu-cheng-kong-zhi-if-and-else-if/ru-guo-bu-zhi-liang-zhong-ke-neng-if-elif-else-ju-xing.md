# 如果不只兩種可能 if … elif … else 句型

![](<../../.gitbook/assets/image (62).png>)

![](<../../.gitbook/assets/image (63).png>)

## 實際例子一

```python
grade = int(input('你的年級 >'))
if grade == 1:
	print('一年級')
elif grade == 2:
	print('二年級')
elif grade == 3:
	print('三年級')
else:
	print('大大級')
```

## 實際例子二

```python
blood = input('你的血型 > ')
if blood == 'O':
	print('O型人')
elif blood == 'A':
	print('A型人')
elif blood == 'B':
	print('B型人')
elif blood == 'AB':
	print('AB型人')
else:
	print('外星人')
```

{% hint style="info" %}
**雖然 if 句型不一定要有 else ，但建議保留作為檢查是否有漏洞**
{% endhint %}

實際例子三 區間判斷 – 動物園門票


**20人以上，打八折**\
**19-10人，打九折**\
**9-2人，打九五折**\
**1人，不打折**

```python
price = 20
number = int(input('購買張數 >'))
if number >= 20:
	price = price*number*0.8
elif number >= 10:
	price = price*number*0.9
elif number >= 2:
	price = price*number*0.95
else:
	price = price*number
print(price)
```

{% hint style="info" %}
**注意判斷順序 "由上而下"**
{% endhint %}

## **練習 : 成績判定**

**請撰寫一個程式，輸入一個分數後，會依照下列區間輸出等第**

| **分數區間**    | **等第** |
| ----------- | ------ |
| **90\~100** | **A**  |
| **80\~89**  | **B**  |
| **70\~79**  | **C**  |
| **60\~69**  | **D**  |
| **0\~59**   | **F**  |

**注意判斷的順序，還有超出判定範圍的成績ex : 599 or -1**

****
