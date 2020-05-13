# 資料型態

資料型態影響了

* 資料表示法
* 記憶體佔用空間
* 合法的運算子
* 運算結果

## 資料型態有哪些？

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x8CC7;&#x6599;&#x578B;&#x614B;</th>
      <th style="text-align:left">&#x8A9E;&#x6CD5;</th>
      <th style="text-align:left">&#x8AAA;&#x660E;</th>
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
</table>## 運算範例

| **Python程式碼** | **說明** | **運算結果** |
| :--- | :--- | :--- |
| **12 + 2** | **整數加法** | **14** |
| **'12' + '2'** | **字串加法** | **'122'** |
| **'12' + 2** | **整數與字串不能相加** | **error** |
| **12 \* 2** | **整數乘法** | **24** |
| **'12' \* 2** | **字串乘法** | **'1212'** |

## **讀入資料**

以字串型態取得使用者輸入的資料

```python
x = input('請輸入一個整數值> ')
print(x*2)
```

```bash
# 輸出
請輸入一個整數值>10
1010
```

## 強制轉型

```python
x = input('請輸入一個整數值> ')
x = int(x)
print(x*2)
```

```python
x = int(input('請輸入一個整數值> '))
print(x*2)
```

```python
x = input('請輸入一個整數值> ')
print(int(x)*2)
```

```bash
# 輸出
請輸入一個整數值>10
20
```

