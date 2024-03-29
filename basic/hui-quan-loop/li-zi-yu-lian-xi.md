# 例子與練習

## **使用者輸入例子**&#x20;

**算 a 到 b 之間的數的總和**

```python
print('請輸入兩個數')
a = int(input('請輸入數字 a > '))
b = int(input('請輸入數字 b > '))
sum = 0

for i in range(a,b+1):
	sum += i

print('a ~ b 的總和是',sum)
```

## **練習 : 數數特級大師**

* **請試著使用 for … in range(x, y, z) : 來數數**
* **請讓使用者輸入 “開頭”與“結尾”**
* **然後依序從開頭數到結尾(含結尾)**

```bash
# 輸入
1
10

# 輸出
1 2 3 4 5 6 7 8 9 10

# 輸入
10
1

# 輸出
10 9 8 7 6 5 4 3 2 1
```

**思考流程圖**

**（**請先思考後，畫出流程圖）

## **練習 : 九九乘法表**

**請試著使用迴圈印出九九乘法表**

```bash
# 輸入

# 輸出
1*1=1 1*2=2 1*3=3 1*4=4 1*5=5 1*6=6 1*7=7 1*8=8 1*9=9 
2*1=2 2*2=4 2*3=6 2*4=8 2*5=10 2*6=12 2*7=14 2*8=16 2*9=18 
3*1=3 3*2=6 3*3=9 3*4=12 3*5=15 3*6=18 3*7=21 3*8=24 3*9=27 
4*1=4 4*2=8 4*3=12 4*4=16 4*5=20 4*6=24 4*7=28 4*8=32 4*9=36 
5*1=5 5*2=10 5*3=15 5*4=20 5*5=25 5*6=30 5*7=35 5*8=40 5*9=45 
6*1=6 6*2=12 6*3=18 6*4=24 6*5=30 6*6=36 6*7=42 6*8=48 6*9=54 
7*1=7 7*2=14 7*3=21 7*4=28 7*5=35 7*6=42 7*7=49 7*8=56 7*9=63 
8*1=8 8*2=16 8*3=24 8*4=32 8*5=40 8*6=48 8*7=56 8*8=64 8*9=72 
9*1=9 9*2=18 9*3=27 9*4=36 9*5=45 9*6=54 9*7=63 9*8=72 9*9=81 
```

想想看



![](<../../.gitbook/assets/image (16).png>)

**1. 每一個大框框內哪一個數字都不會動呢?**

**2. 每個大框框之間有甚麼是相似的呢?**\
