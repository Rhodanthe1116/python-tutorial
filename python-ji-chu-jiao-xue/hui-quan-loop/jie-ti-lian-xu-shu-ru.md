# 解題連續輸入

在解題的時候常常會遇到「連續輸入」、「您共輸出 1 行」...... 其實都是因為需要迴圈去讓他跑很多次

有兩種方法：

## while True:

```python
while True:
    try:
        s = input()
        ...
    except:
        break
```

這裡用的是例外處理的方法，試試看有沒有輸入，也就是`try:`，如果有，就做`...`；如果沒有，就`break`

## import sys

```python
import sys
for ss in sys.stdin:
    print(ss)
```

ss是一個字串，需要另外處理，`split()`或`int()`或`map()`

## 結論

兩種方法各有優缺，看情況使用





