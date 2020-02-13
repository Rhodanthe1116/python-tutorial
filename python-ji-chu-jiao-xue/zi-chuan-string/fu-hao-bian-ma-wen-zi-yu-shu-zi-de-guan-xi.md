# 符號編碼：文字與數字的關係

## ASCII 碼：早期提供英語的編碼

![ASCII &#x8868;](https://3.bp.blogspot.com/-EmmXIc6wNRI/WauyBOCusUI/AAAAAAAAAk8/Wodt0iDmaQowu3XuaHcIGCVes-75E7URgCLcBGAs/s1600/ASCII%2Bcode.png)

```python
print(ord("A"))
print(chr(65))
```

## Unicode 萬國碼：近代常用編碼

收集各國語言及符號，資料量龐大。

編號大體上是這樣安排：

```text
前128個編號，與ASCII完全相同。
再來到前65536 = 2byte個編號，是世界各國常見文字。
再來到前4294967296 = 4byte個編號，是世界各國罕見文字。
```

