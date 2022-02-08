# 串列與for迴圈

```python
num_list = [1, 2, 3, 4, 5]
for num in num_list:
    print('before', num_list)
    num_list.pop()
    print('after', num_list)
```

```bash
# 輸出
before [1, 2, 3, 4, 5]
after [1, 2, 3, 4]
before [1, 2, 3, 4]
after [1, 2, 3]
before [1, 2, 3]
after [1, 2]
```

## 練習用for寫出一個無限迴圈試試看

```python
a = [1]
for d in a:
    a.append(2*d)
    print(a)
```

```bash
# 輸出
[1, 2]
[1, 2, 4]
[1, 2, 4, 8]
[1, 2, 4, 8, 16]
[1, 2, 4, 8, 16, 32]
……
……
```
