# 挑戰時刻

**修改「求平均」程式**

```python
print('計算平均的程式')
total = int(input('請輸入總和> '))
count = int(input('請輸入個數> '))
if count > 0:
	print('答案是',total/count)
else : 
	int(input('個數需為正值，請輸入個數> ')) 	
	if count > 0:
		print('答案是',total/count)
	else:
		print('無法計算---個數需為正',total/count)
```

**缺點:** 

**1. 有重複的片段**      

**2. 控制結構複雜 \(兩層\)**

## **範例解答**

```python
print('計算平均的程式')
total = int(input('請輸入總和> '))
count = int(input('請輸入個數> '))
if count <= 0:
	 int(input('個數需為正值，請輸入個數> '))

if count > 0:
	print('答案是',total/count)
else:
	print('無法計算---個數需為正',total/count)
```

