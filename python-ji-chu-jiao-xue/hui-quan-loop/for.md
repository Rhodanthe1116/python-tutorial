# for 迴圈



![](<../../.gitbook/assets/image (58).png>)

![](<../../.gitbook/assets/image (54).png>)

## **while到for**

![](<../../.gitbook/assets/image (55).png>)

![](<../../.gitbook/assets/image (56).png>)

## 簡單範例

```python
for i in range(6):
    print(i)
```

## 實際範例

### **數數小生，從 1 數到 10 :**

```python
for count in range(1, 10  , 1):
    print(count , end=' ')
print('!')
```

```bash
# 輸出
1 2 3 4 5 6 7 8 9 10 !
```

### **數數能手，從 10 數到 1 :**

```python
for count in range(10, 1  ,-1):
    print(count , end=' ')
print('!')
```

```bash
# 輸出
10 9 8 7 6 5 4 3 2 1 !
```

## **練習 : 數數大師**

**請試著使用 for … in range(x, y, z) : 來數數**

1. **請印出 0 1 2 3 4 5 6 7 8 9 !**
2. **請印出 1 3 5 7 9 11 13 15 17 19 !**

{% hint style="info" %}
&#x20;**range(x, y, z)， x 是開頭、 y 是結尾( 不含 y )、z 是公差**
{% endhint %}
