# 4️⃣ 排序 Sorting

就如同平常排序雜亂的撲克牌一樣，排序演算法將沒有排列好的資料照順序排好。

比如現在有一堆資料：

![](../.gitbook/assets/image%20%286%29.png)

排序後會變成：

![](../.gitbook/assets/image%20%2817%29.png)

雖然 Python 中已經有寫好的函數可以使用，不過還是必須了解重要的基礎理論。以下介紹幾個常見的排序演算法。

## 泡沫排序 Bubble Sort

很簡單想到又很好寫的排序法，直接看下面的動畫會比較好懂。

![wiki: Bubble-sort.gif](https://upload.wikimedia.org/wikipedia/commons/0/06/Bubble-sort.gif)

實際的運作方法是：兩兩比較，走過一次串列之後會發現最大的已經在最尾端，也就是說每走過一次串列就會將最大的放在最後面，此時可以分成左邊未排序的部分跟右邊已排序的部分。一直重複走過未排序的串列，便會完成排序。

![&#x4F7F;&#x7528;&#x6CE1;&#x6CAB;&#x6392;&#x5E8F;&#x70BA;&#x4E00;&#x5217;&#x6578;&#x5B57;&#x9032;&#x884C;&#x6392;&#x5E8F;&#x7684;&#x904E;&#x7A0B;](https://upload.wikimedia.org/wikipedia/commons/3/37/Bubble_sort_animation.gif)

### 複雜度分析

假設現在有 n 個數，第 1 次走串列會比較 n-1 次，第 2 次走串列會比較 n-2 次......第 n-1 次走串列會比較 1 次,，而總共會走 n 次串列 ，所以可以列出下列式子：

$$
T(n) = (n-1) + (n-2) +...+1 \\
= \frac{(n-1)n}{2} \\
= O(n^2)
$$

### 實作程式碼

```python
l = [3, 4, 1, 6, 2, 5, 9, 7, 8]
n = len(l)

for i in range(n):
    for j in range(n-1-i):
        if l[j] > l[j+1]:
            l[j], l[j+1] = l[j+1], l[j]
            
print(l)
```

## 選擇排序 Selection Sort

很直觀的排序法

![](https://upload.wikimedia.org/wikipedia/commons/9/94/Selection-Sort-Animation.gif)

每次從未排序的資料中選擇最小的，將其丟入已排序的資料中。用變數紀錄當前最小值（紅色），不斷與新進的數字（藍色）比較。

![&#x4F7F;&#x7528;&#x9078;&#x64C7;&#x6392;&#x5E8F;&#x70BA;&#x4E00;&#x5217;&#x6578;&#x5B57;&#x9032;&#x884C;&#x6392;&#x5E8F;&#x7684;&#x904E;&#x7A0B;](https://upload.wikimedia.org/wikipedia/commons/b/b0/Selection_sort_animation.gif)

### 複雜度分析

與泡沫排序相同，假設現在有 n 個數，第 1 次走串列會比較 n-1 次，第 2 次走串列會比較 n-2 次......第 n-1 次走串列會比較 1 次,，而總共會走 n-1 次串列 ，所以可以列出下列式子：

$$
T(n) = (n-1) + (n-2) +...+1 \\
= \frac{(n-1)n}{2} \\
= O(n^2)
$$

### 實作程式碼

```python
l = [8, 5, 2, 6, 9, 3, 1, 4, 0, 7]
n = len(l)

for i in range(n-1):
    minimum = l[i]
    for current in range(i+1, n-1):
        if l[current] < l[minimum]:
            minimum = current
    l[i], l[minimum] = l[minimum], l[i]
    
print(l)
```

每次都把最小值直接搬到序列最前面，交換次數變多，省下一個暫存變數，可實現比較簡單的寫法。

```python
l = [8, 5, 2, 6, 9, 3, 1, 4, 0, 7]
n = len(l)

for i in range(n):
    for j in range(i, n):
        if l[j] < l[i]:
            l[i], l[j] = l[j], l[i]
    
print(l)
```

## Insertion Sort

很直觀的排序法

![wiki: insertion sort.gif](https://upload.wikimedia.org/wikipedia/commons/0/0f/Insertion-sort-example-300px.gif)

每次從未排序的資料中選擇最小的，將其丟入已排序的料中。用變數紀錄當前最小值（紅色），不斷與新進的數字（藍色）比較。

![&#x4F7F;&#x7528;&#x9078;&#x64C7;&#x6392;&#x5E8F;&#x70BA;&#x4E00;&#x5217;&#x6578;&#x5B57;&#x9032;&#x884C;&#x6392;&#x5E8F;&#x7684;&#x904E;&#x7A0B;](https://upload.wikimedia.org/wikipedia/commons/b/b0/Selection_sort_animation.gif)

### 複雜度分析

與泡沫排序相同，假設現在有 n 個數，第 1 次走串列會比較 n-1 次，第 2 次走串列會比較 n-2 次......第 n-1 次走串列會比較 1 次,，而總共會走 n-1 次串列 ，所以可以列出下列式子：

$$
T(n) = (n-1) + (n-2) +...+1 \\
= \frac{(n-1)n}{2} \\
= O(n^2)
$$

### 實作程式碼

```python
l = [8, 5, 2, 6, 9, 3, 1, 4, 0, 7]
n = len(l)

for i in range(n-1):
    minimum = l[i]
    for current in range(i+1, n-1):
        if l[current] < l[minimum]:
            minimum = current
    l[i], l[minimum] = l[minimum], l[i]
    
print(l)
```

每次都把最小值直接搬到序列最前面，交換次數變多，省下一個暫存變數，可實現比較簡單的寫法。

## Quick Sort

## Python 中 Sort 函數的使用



