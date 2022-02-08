# ⚡ 練習：觀念題

## Python 有下列哪一項特色？

1. 執行速度快
2. 編寫容易
3. 適合用來操控硬體

2

1.Python為了讓程式方便撰寫，犧牲了執行速度，Python的執行速度可能是其他語言（C++、Java等）的好幾倍或甚至好幾十倍

3.目前主要用來操控硬體的語言多為與C類似語言，比如Arduino、Arm等嵌入式系統。不過近期似乎有些人開始在開發硬體的相關套件。

## 若要在 Python 中輸出字串，可用以下哪一個指令？

1. print()
2. printf()
3. cout
4. scanf()

1

其餘皆為c, c++語法

## 若要在 Python 中輸出後「不」換行，可用以下哪一個指令？

1. `print("str", end="")`
2. `printf("str", end="")`
3. `print("str", sep="")`
4. `print("str", end="\n")`

### 答案

1

### 詳解

2.printf應改為print

3.sep代表分隔，並非結尾

4.\n在字串中代表換行

### 出題

C

## 請問 Python 中如何宣告變數？

1. `int x = 0`
2. `x = 0`
3. `float = 0`

2

## 請問下列哪個不是 Python 中有的資料型態？

1. float
2. bool
3. double

3

在python中沒有double。在有些程式語言中，double作為容量比float還要大的小數型態。在Python中float已經足夠大了

## 以下哪個是整數型態？

1. `"999"`
2. `999`
3. `'999'`
4. `[999]`

2

1.3.皆為字串，因為它們都被引號包起來。

4.\[]代表一種叫做list的資料型態，將在未來的課程中介紹

## 請問若要輸入一個數字進變數 x，不能用下列哪一個指令？

1. `x = input()`
2. `input(x)`
3. `x = input("x")`

2



## 若要將一個字串轉換成整數，該用哪一個指令？

1. `int("123")`
2. `str(123)`
3. `str(int("123"))`
4. `int(123)`

1

2.整數轉字串

3.字串轉整數再轉字串

4.整數轉整數

## 若要在一行同時輸入3個變數，該如何使用？

1. `x, y, z = input(), input(), input()`
2. `x, y, z = input().split()`
3. `x = input()`\
   `y = input()`\
   `z = input()`

2

1.等同於3.

3\.  需要分三行輸入（案三次enter）

## x = x // 3 等同於

1. `x // 3`
2. `x / 3`
3. `x //= 3`
4. `x = x / 3`

3

/為除法

//為除法後取商數

## 期中題庫

下列哪一項不是合法的Python變數名稱？

1. home\_address
2. 4square
3. route66
4. Age

下列哪一項是PEP8所推薦使用的變數命名規則？

1. DistanceToNearestTown
2. distance\_to\_nearest\_town
3. distanceToNearestTown

若 a, b, c, d, e 均為整數變數，下列哪個算式計算結果與 a+b\*c-e 計算結果相同？APCS1060304

1. (((a+b)\*c)-e)
2. ((a+b)\*(c-e))
3. ((a+(b\*c))-e)
4. (a+((b\*c)-e))

程式執行時，程式中的變數值是存放在

1. 記憶體
2. 硬碟
3. 輸出入裝置
4. 匯流排

若有三變數a, b, c，下列那個程式片段可以將a 和 b的內容交換？

1. a = b, b = a
2. c = a, a = b, b = c
3. b = a, c = b, a = c
4. 以上皆可
