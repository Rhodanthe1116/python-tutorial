# 繼續的迴圈 continue

## continue

**可以跳過某些狀況，讓迴圈繼續做事**

## **簡單範例**

```python
i = 0
while i < 6:
    i += 1 
    if i == 3:
        continue
    print(i)
```

![](../../.gitbook/assets/image%20%282%29.png)

{% hint style="info" %}
**與 " 沒有 " continue 句型比較 :**

```python
i = 0
while i < 6:
	i += 1
	print(i)
```
{% endhint %}

## **範例: 挑出特定數**

**印出 1 ~  num 之間，可以被 7 整除的數**

```python
num = int(input('請輸入大於零的整數 >'))
count = 0
while count < num:
	count += 1
	if count % 7 != 0:
		continue
	print(count,'可以被 7 整除')
```

## **任務: 正三角形**

* **輸入一個數代表高度**
* **用\*符號，印出符合該高度的正三角形**

```bash
# 輸入
3

# 輸出
  *
 * *
* * *
```

```bash
# 輸入
0

# 輸出
 
```

