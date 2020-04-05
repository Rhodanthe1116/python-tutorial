# 變數 Variable

## 變數（variable）

變數是一個可以儲存數字的容器，顧名思義就是可以變動的數字。

生活中處處可見變數，如遊戲中的血量、電腦右下角的時間等。

如下圖：

![](../../.gitbook/assets/image%20%2814%29.png)

一個名為`hp`的變數，而`hp`中儲存`100`這個值。

每個變數有以下三種屬性：

* **變數名稱**：每個變數都需要有個名字，才知道誰是誰，如`hp`
* **資料型態**：有數字、文字等。不同類型不能互存，像剛剛的`hp`就只能存整數
* **變數的值**：變數所儲存的值，如`100`

在程式中若要創造一個`hp`並輸出可用以下語法：

```python
hp = 100
print(hp)
```

{% hint style="warning" %}
變數在第一次使用的時候要用`=`來給初始值！

這裡的`=`可以想成「設成」
{% endhint %}

## 資料型態

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x540D;&#x7A31;</th>
      <th style="text-align:left">&#x8A9E;&#x6CD5;</th>
      <th style="text-align:left">&#x8209;&#x4F8B;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>&#x6574;&#x6578;&#xFF08;Integer&#xFF09;</b>
      </td>
      <td style="text-align:left">
        <p></p>
        <p><code>int</code>
        </p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>&#x5982;<code>1</code>,<code>15</code>,<code>78</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&#x5C0F;&#x6578;&#xFF08;Float&#xFF09;</b>
      </td>
      <td style="text-align:left">
        <p></p>
        <p><code>float</code>
        </p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>&#x5982;<code>2.4</code>,<code>5.7</code>,<code>0.1</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&#x5B57;&#x4E32;&#xFF08;String&#xFF09;</b>
      </td>
      <td style="text-align:left">
        <p></p>
        <p><code>str</code>
        </p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>&#x4E5F;&#x5C31;&#x662F;&#x4E00;&#x6BB5;&#x6587;&#x5B57;&#x3002;&#x4F8B;&#x5982;&#xFF1A;<code>&quot;hello, world&quot;</code>&#xFF0C;&#x6CE8;&#x610F;&#x96D9;&#x5F15;&#x865F;<code>&quot;</code>&#x4E5F;&#x53EF;&#x4EE5;&#x662F;&#x55AE;&#x5F15;&#x865F;<code>&apos;&#xFF0C;</code>&#x6BD4;&#x5982;&#x8AAA;<code>&apos;hello, world&apos;</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&#x5E03;&#x6797;&#xFF08;Bool&#xFF09;</b>
      </td>
      <td style="text-align:left">
        <p></p>
        <p><code>bool</code>
        </p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>&#x53EA;&#x6709;&#x662F;&#x8DDF;&#x975E;&#xFF0C;&#x5C0D;&#x61C9;&#x70BA;<code>True</code>&#x8DDF;<code>False</code>
        </p>
      </td>
    </tr>
  </tbody>
</table>```python
int1 = 15
float1 = 2.4
str1 = "hello, world"

bool1 = True
bool1 = False
```

## 命名規則

變數的命名有一些規則：

* 允許字母及數字`a-z`, `A-z`, `0-9` 和`_` , 但是開頭必須是字母
* 變數區分大小寫
* 變數長度沒有限制

## 命名傳統

Python有一些命名傳統，主要是遵照PEP8：

{% embed url="https://www.python.org/dev/peps/pep-0008/" %}

目前不需要去讀文件，只需要知道以下：

* 如果變數名稱大於是多字節的話，採用小寫字母搭配底線\(lower\_case\_with\_underscores\)

{% hint style="success" %}
正確

```python
my_name = "benson"
```
{% endhint %}

{% hint style="danger" %}
錯誤

```text
myName = "benson"
MyName = "benson"
```
{% endhint %}

## 變數在電腦中的儲存方法

變數是儲存在電腦的記憶體中。記憶體就像人的短期記憶，當程式執行完，記憶體便會被釋放，不像一般資料是儲存在硬碟裡，這也就是為什麼，我們在編輯文件的時候，如果沒有存檔，紀錄就會不見，那是因為我們還沒有把資料從記憶體轉入到硬碟中。

