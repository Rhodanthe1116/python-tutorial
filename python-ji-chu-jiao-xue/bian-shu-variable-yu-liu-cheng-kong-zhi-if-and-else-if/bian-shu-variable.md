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
        <p>&#x4E5F;&#x5C31;&#x662F;&#x4E00;&#x6BB5;&#x6587;&#x5B57;&#x3002;&#x4F8B;&#x5982;&#xFF1A;<code>&quot;hello, world&quot;</code>&#xFF0C;&#x6CE8;&#x610F;&#x96D9;&#x5F15;&#x865F;<code>&quot;</code>
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

## 

