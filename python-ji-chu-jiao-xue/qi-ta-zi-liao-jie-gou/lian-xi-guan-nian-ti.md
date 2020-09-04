# ⚡ 練習：觀念題

## 請問下列對於Python中Tuple的敘述，何者錯誤？

1. 與 list 相似，但其內部資訊為不可更改資料
2. 只有一個元素時須以T = \(1, \)的形式指定，
3. 適合用來維護不需變動的資料
4. 對Tuple使用len\(\)函式會出錯

4

tuple也可以使用len\(\)，一般可以套用在list上的函式幾乎都可以套在tuple，如max\(\), min\(\)，這些函式幾乎都可以接收一個序列，如string, bytes, tuple, list, or range 或是之後會此章教到的  dictionary, set等

## 請問下列程式會輸出什麼？

```python
t1 = (1, 2, 3)
t2 = (4, 5, 6)

prevId = id(t1)
t1 += t2
currId = id(t1)

print(prevId == currId, end=' ')

l1 = [1, 2, 3]
l2 = [4, 5, 6]

prevId = id(l1)
l1 += l2
currId = id(l1)

print(prevId == currId)
```

1. True True
2. True False
3. False True
4. True False

3

Tuple為不可變的，因此若其指定的元素改變了，代表換了一個新的記憶體位置，而非像list一樣在同記憶體位置再新增元素

## Python中有個很方便的功能，叫做包裝\(pack\)與拆解\(unpack\)，請問下列程式會輸出什麼？

```python
my_input = "5 3 0 1 2 3 4"
n, a, *l = list(map(int, my_input.split()))

l = list(map(lambda x: x + a, l))
print(*l)
```

1. 0 1 2 3 4
2. \[3, 4 ,5, 6, 7\]
3. 3 4 5 6 7
4. \[3, 3, 4, 5, 6, 7\]

3

第二行n = 5, a = 3，剩下的元素將由l包裝起來，l = \[0, 1, 2, 3, 4\]，經過map後會將元素+=a 也就是+= 3，因此l = \[3, 4, 5, 6, 7\]，最後輸出的時候使用了\*拆解，因此會輸出3 4 5 6 7而非\[3, 4, 5, 6, 7\]

## 運用map函式可以簡化很多程式碼，請問下列程式會輸出什麼？

```python
my_input = "-2 -1 0 1 2"
l = list(map(int, my_input.split()))
print(l[3], end=' ')

def ReLU(x):
    return max(0, x)

l = list(map(ReLU, l))
print(l)
```

1. 1 \[0, 0, 0, 1, 2\]
2. '1' \[-2, -1, 0, 1, 2\]
3. '1' \[0, 0, 0, 1, 2\]
4. 1 \[-2, -1, 0, 0, 0\]

1

第二行的my\_input.split\(\)後的元素經過了map\(int, \)轉變成int型態，再經由list\(\)轉變為list，於是l = \[-2, -1, 0, 1, 2\]，因此可以知道第三行會輸出1。而第五行的ReLU函數，根據其內容，可以推知此函數會將負數回傳0，而正數則原封不動回傳，因此第五行l將變成\[0, 0, 0, 1, 2\]，故選1。

## 請問下列程式會輸出什麼？

```python
from math import sqrt

l = [1, 2, 3 ,4, 5, 6, 7, 8, 9]

def my_filter(x):
    return sqrt(x) == int(sqrt(x))

filtered = list(filter(my_filter, l))
print(filtered)
```

1. \[0, 1, 4\]
2. \[1, 4, 9\]
3. \[2, 4, 8\]
4. \[1, 3, 9\]

2

此題的my\_filter為尋找完全平方數，如1\(1\*1\), 4\(2\*2\), 9\(3\*3\)，完全平方數經過開根號後不會有小數點，因此第6行等式會成立，剩下只要知道filter的用法，即可知道答案會是\[1, 4, 9\]

## 請問下列程式會輸出什麼？

```python
my_input = "0 1 2 3 4"
l = map(int, my_input.split())
print(type(l))
```

1. &lt;class 'tuple'&gt;
2. &lt;class 'list'&gt;
3. &lt;class 'map'&gt;
4. &lt;class 'int'&gt;

3

使用map時要注意，map後的結果是一個map，並不是list也不是tuple，此時若直接當成list使用或出錯，必須要使用list\(\)轉換後才會是list，這個方法前面也很常出現！需要特別注意

## 請問下列程式會輸出什麼？

```python
l = [0, 1, 2, 3, 4]
s = list(map(lambda i:
    'id-{}'.format(i)
, l))
print(s[2])
```

1. 2
2. id-2
3. 1
4. id-1

2

map也可用來將數字批次處理成字串！

## 請問下列程式會輸出什麼？

```python
l0 = [-2, -1, 0, 1, 2]
def myfunc(x):
    return max(0, x)
l1 = list(map(myfunc, l0))
l2 = list(filter(myfunc, l0))

print(len(l1), end=' ')
print(len(l2))
```

1. 2 5
2. 5 5
3. 2 2
4. 5 2

4

第二行的myfunc跟第三題的ReLU一樣，會將負數回傳0，正數則回傳原本的值。

接下來，map會對原本list中的每一個元素做myfunc，因此map出來的長度不會改變，而l1 = \[0, 0, 0, 1, 2\]；另一方面，filter會將原本list中符合元素組成一個新元素，不符合的元素則拋棄，因此filter出來list長度有可能改變，此時l2 = \[1, 2\]。

其中值得注意的地方是，filter接收的函數需要回傳布林值（True或False），而0正好可以代表False，非0則是True，因此這裡的myfunc可以同時套用在map與filter中而不會出錯。

## 請問下列程式會輸出什麼？

```python
my_input = [3, 9, 4, 3, 6]

n = 10
cnt = []
for i in range(n):
    cnt.append([i, 0])
    
for num in my_input:
    cnt[num][1] += 1

cnt = list(filter(lambda x: x[1] > 1, cnt))

for pair in cnt:
    print(pair[0] , end=' ')
```

1. 9
2. 6
3. 3
4. 4

3

此題會將輸入的數字做出現頻率統計，並將出現頻率大於1的數字輸出出來。此題的list用法與未來將介紹的dictionary類似，之後學過dictionary後可以回來做個比較！

## 請問下列程式會輸出什麼？

```python
l = [0, 1, 2, 3, 4]
prev_id = id(l)

new_l = list(map(lambda x: x + 1, l))

curr_id = id(l)
new_id = id(new_l)

print(prev_id == curr_id)
print(prev_id == new_id)

```

1. False False
2. False True
3. True False
4. True True

3

被map後的list不會改變，list\(map\(\)\)會創造出一個新的list，因此第九行的兩個id會將相同。而新創造出來的new\_l自然就與l不同了。

