# While 重複的加總

迴圈，不斷執行相同或類似的東西

![](../../.gitbook/assets/image%20%2811%29.png)

```python
i = 1
if i < 6:
    print(i)
    i += 1
```

```bash
# 輸出
1 
2 
3 
```

**進階範例**

```python
print('計算總和的程式')
total = 0
cost = int(input('請輸入費用> ( 0為終止輸入 )'))
total = total + cost
while cost > 0:
	cost = int(input('請輸入費用> ( 0為終止輸入 )'))
	total += cost

print('總和是',total)
```

{% hint style="warning" %}
**大家來找碴**
{% endhint %}

![](../../.gitbook/assets/image%20%2855%29.png)

## **任務: 長方形**

* **每次輸入一行，包含3個值，每個值用空格間隔**
* **第一個值與第二個值，分別代表長\(橫\)、寬\(直\)**
* **第三個值代表印出的符號**

```bash
# 輸入
4 3 *

# 輸出
****
****
****

# 輸入
3 4 6 

# 輸出
666
666
666
666
```

## **其他例子：終極密碼，猜數字**

```python
print('終極密碼')
key = 99
guess = int(input('請輸入猜測> ( 1~100 )'))
count = 1
while guess != key and count < 5:
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

## \*\*\*\*

