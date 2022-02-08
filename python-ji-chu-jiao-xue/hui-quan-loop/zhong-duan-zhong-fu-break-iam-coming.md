# 中斷重複 break :  I am coming!!

## **簡單範例**

```python
i = 1
while i < 6:
	print(i)
	if i == 3:
		break
	i += 1
```

![](<../../.gitbook/assets/image (51).png>)

{% hint style="info" %}
**與 " 沒有 " break 句型比較 :**

```python
i = 1
while i < 6:
	print(i)
	i += 1
```
{% endhint %}

## **實際範例：終極密碼 ( break )**

```python
print('終極密碼')
key = 99
guess = int(input('請輸入猜測> ( 1~100 )'))
count = 1
while guess != key :
	if count >= 5 : break
	# 回答超過5次，break
	print('猜錯了')
	if guess > key:
		print('再小一點')
	else:
		print('再大一點')
	guess = int(input('請輸入猜測> ( 1~100 )'))
	count += 1
if guess == key:
	print('答對了')
else:
	print('猜錯了，遊戲結束')

```
