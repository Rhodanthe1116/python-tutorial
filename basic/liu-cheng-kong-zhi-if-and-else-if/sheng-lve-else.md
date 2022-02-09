# 省略else

## **例子 : 買電影票**

```python
print('買電影票的程式')
identity = input('請輸入身份> ')
count = int(input('請輸入人數> '))

price = count*320#全票票價 

if identity == '學生':
	price = price*0.8#學生打八折

print('總價', int(price), '元')
```

```bash
# 執行 1

買電影票的程式
請輸入身份> 學生
請輸入人數> 10
總價 2560 元
```

```bash
# 執行 2

買電影票的程式
請輸入身份> 一般人
請輸入人數> 10
總價 3200 元
```
