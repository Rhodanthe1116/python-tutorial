# 平均的危機

**除以零的錯誤**

```python
print('計算平均的程式')
total = int(input('請輸入總和> '))
count = int(input('請輸入個數> '))
print('答案是', total/count)
```

```bash
計算平均的程式
請輸入總和> 100
請輸入個數> 0
```

{% hint style="danger" %}
**ZeroDivisionError: division by zero**
{% endhint %}

## **修改程式**

```python
print('計算平均的程式')
total = int(input('請輸入總和>'))
count = int(input('請輸入個數>'))
if count > 0:
	print('答案是',total/count)
```

## 如果有其他

```python
print('計算平均的程式')
total = int(input('請輸入總和>'))
count = int(input('請輸入個數>'))
if count > 0:
	print('答案是',total/count)
else:
	print(‘無法計算---個數需為正整數')

```

