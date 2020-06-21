# 實作題

### 

### 非作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e787" %}

二維陣列

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e839" %}

簡單map





## 字串處理

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e975" %}

字串處理，需要熟悉內建函數如len\(\), find\(\), ord\(\), chr\(\), isalpha\(\), 字串拼接等，和判斷邊界條件，需要注意Python不像C++一樣可以用=來指定字串中的字元，也不能直接對字元做加減。

```python
import sys
for encoded_letter in sys.stdin:

    k = 0
    while True:
        is_love_found = encoded_letter.find('love') != -1 or \
            encoded_letter.find('Love') != -1
        if is_love_found:
            break
        else:
            decoded_letter = ''
            for char in encoded_letter:
                if char.isalpha():
                    decoded_char = chr(ord(char) + 1)
                    if decoded_char == chr(ord('z') + 1):
                        decoded_char = 'a'
                    elif decoded_char == chr(ord('Z') + 1):
                        decoded_char = 'A'
                    decoded_letter += decoded_char
                else:
                    decoded_letter += char
            encoded_letter = decoded_letter
            k += 1
    print(k)
```



