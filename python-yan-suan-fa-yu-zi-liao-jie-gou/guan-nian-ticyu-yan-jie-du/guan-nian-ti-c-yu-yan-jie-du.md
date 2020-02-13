# 觀念題 C 語言解讀

APCS 的觀念題是以 C 語言命題，因此對以 Python 入門的同學需要另外學習 C 語言的格式！

## 先看一段範例

來自 APCS 歷屆試題，可以發現在之前的觀念題練習中有出現過。

{% tabs %}
{% tab title="C" %}
```cpp
int main()
{
  int x = 0, n = 5;
  for (int i = 1; i <= n; i = i + 1)
    for (int j = 1; j <= n; j = j + 1)
    {
      if ((i + j) == 2)
        x = x + 2;
      if ((i + j) == 3)
        x = x + 3;
      if ((i + j) == 4)
        x = x + 4;
    }
  printf("%d\n", x);
  return 0;
}
```
{% endtab %}

{% tab title="Python" %}
```python
x = 0; n = 5
for i in range(1, n+1):
    for j in range(1, n+1):
        if i + j == 2:
            x = x + 2
        if i + j == 3:
            x = x + 3
        if i + j == 4: 
            x = x + 4
print(x)
```
{% endtab %}
{% endtabs %}

可以發現大致上差不多，但有些細節不太一樣。

## 整體語法差異

{% tabs %}
{% tab title="C" %}
```cpp
int function()
{
  printf("this is a function\n");
}

int main()
{
  printf("this is a C program\n");

  return 0;
}
```
{% endtab %}

{% tab title="Python" %}
```python
def function():
    print("this is a function")

print("this is a Python program")
```
{% endtab %}
{% endtabs %}

1. C 的主程式寫在`main()`函數裡，Python 不用特別寫主函數。
2. `printf()`類似`print()`。
3. `"\n"`代表換行
4. C 以大括號標示範圍，Python 以縮排及冒號標示範圍。
5. C 的函數寫法跟 Python 有不同格式，稍後介紹。
6. `return 0`在現今大多數編輯器中可有可無

## 變數使用

### 宣告

{% tabs %}
{% tab title="C" %}
```cpp
int main()
{
  int x = 0;

  return 0;
}
```
{% endtab %}

{% tab title="Python" %}
```python
x = 0
```
{% endtab %}
{% endtabs %}

C++ 在宣告時要在前面加上變數型態。

### 使用

{% tabs %}
{% tab title="C" %}
```cpp
int main()
{
  int x = 0;
  x = 5;
  printf("%d", x);
}
```
{% endtab %}

{% tab title="Python" %}
```python
x = 0
x = 5
print("{}".format(x))
```
{% endtab %}
{% endtabs %}

與Python類似。

1. `%d`代表整數型態，跟`{}`類似，但`{}`不需要指明型態。

### 型態

| C | 描述 | 對應 Python |
| :--- | :--- | :--- |
| int | 整數 | int |
| float | 小數 | float |
| double | 比較大的小數 | float |
| char | 字元，代表一個字母 | 一個字元的 string |
| string | 字串，代表一段文字 | string |

大部分 Python 型態所佔的記憶體大小都比 C 還要大，也因此 Python 常常被說太肥大

## 輸入

{% tabs %}
{% tab title="C" %}
```c
int x;
scanf("%d", &x);
printf("%d", x);
```
{% endtab %}

{% tab title="Python" %}
```python
x = 0
x = int(input())
print(x)
```
{% endtab %}
{% endtabs %}

注意`&`符號，不需要知道太清楚，在 Python 不會出現這種用法。

## For 迴圈

{% tabs %}
{% tab title="C" %}
```cpp
int main()
{
  int n = 5;
  for (int i = 0; i < n; i = i + 1)
  {
    printf("%d", i);
  }
}
```
{% endtab %}

{% tab title="Python" %}
```python
n = 5
for i in range(0, n, 1):
    print(i)
```
{% endtab %}
{% endtabs %}

其實也是很類似

1. `i < n`代表他成立的時候才執行迴圈

## 一些符號差異

{% tabs %}
{% tab title="C" %}
```cpp
a && b
a || b

i ++     // i += 1
i --     // i -= 1
```
{% endtab %}

{% tab title="Python" %}
```python
a and b
a or b 
```
{% endtab %}
{% endtabs %}

## List 

{% tabs %}
{% tab title="C" %}
```cpp
int main()
{
  int arr[5] = {0, 1, 2, 3, 4};
  printf("%d", arr[1]);
}
```
{% endtab %}

{% tab title="Python" %}
```python
l = [0, 1, 2, 3, 4]
print(l[1])
```
{% endtab %}
{% endtabs %}

1. C 的 List 稱作 **陣列 Array**。
2. 陣列在宣告時必須指明大小，且後續不能隨意更改大小

## 函數

{% tabs %}
{% tab title="C" %}
```cpp
void my_function(int a, double b)
{
  printf("%f", a * b);
}

int main()
{
  my_function(5, 8.7);

  return 0;
}
```
{% endtab %}

{% tab title="Python" %}
```python
def my_function(a, b):
    print(a * b)

my_function(5, 8.7)
```
{% endtab %}
{% endtabs %}

C 的函數參數都要指明變數型態，包括回傳變數的型態，甚至連主函數都要，若不需要回傳，可以`void`代替，`void`代表**空、沒有或什麼都不是**



