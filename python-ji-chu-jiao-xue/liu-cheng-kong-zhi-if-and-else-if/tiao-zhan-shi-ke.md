# 挑戰時刻

## **修改「求平均」程式以達下述功能**

* **如果使用者第一次輸入的個數為正，計算並列印平均。**
* **如果使用者第一次輸入的個數不為正，提示使用者並讓其再輸入一次個數。**
  * **如果使用者第二次輸入的個數為正，計算並列印平均。**

    **如果使用者第二次輸入的個數不為正，提示使用者並結束程式。**

### **參考解答**

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

缺點: 

1. 有重複的片段      

2. 控制結構複雜 \(兩層\)

### **範例解答**

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

精簡的程式碼 : 

1. 沒有重複的片段      

2. 控制結構要簡單\(一層\)  


