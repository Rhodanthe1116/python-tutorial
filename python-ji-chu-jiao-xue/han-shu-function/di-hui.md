# 遞迴 Recursion

一個函數又呼叫自己稱作**遞迴 Recursion**

例子：費波那契數列

$$
f(1) = 1\\
f(2) = 1 \\
f(n) = f(n-1) +f(n-2), n>=2
$$

如果實際程式碼運作會**類似**於：

![](../../.gitbook/assets/r.gif)

```python
def f(n):
    if n == 1:
        return 1
    elif n == 2:
        return 1
    else: 
        return f(n-1) + f(n-2)
        
print(f(4))
```



