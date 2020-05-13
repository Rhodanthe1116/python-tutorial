# 平均的危機

**除以零的錯誤**

```python
print('計算平均的程式')
total = int(input('請輸入總和> '))
count = int(input('請輸入個數> '))
print('答案是', total/count)
```

```bash
計算平均的程式
請輸入總和> 100
請輸入個數> 0
```

{% hint style="danger" %}
**ZeroDivisionError: division by zero**
{% endhint %}

**電腦在遇到除以零的運算時，通常都會以某種型式回報錯誤。**

**我們能否修改程式？**

